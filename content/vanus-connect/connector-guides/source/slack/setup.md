# Slack

This guide contains information to set up a Slack Source in Vanus Connect.

## Introduction

Slack is a cloud-based team collaboration platform that allows users to communicate, share files, and integrate with other tools and services.

Our Slack Source connector, lets you receive events when users join, message, react etc... 

## Prerequisites

Before obtaining Slack events, you must have:
- Have a [Slack account](https://slack.com).
- A [Vanus Cloud account](https://cloud.vanus.ai).

## Getting Started

### Step 1: Create an app in Slack

1. Go to [Slack API](https://api.slack.com/apps), and click **Create New App**.
   ![](images/img.png)
2. Select **From Scratch.**
![](images/img_1.png)
3. Set the app name and Workspace.
![](images/img_2.png)

---

### Step 2: Get App Credentials

1. Go to **Basic Information**.
![](images/img_3.png)
2. Scroll down to **App Credentials** and copy the following credentials.
 - Verification Token
 - Signing Secret
![](images/img_4.png)
3. Don't close this page but continue in Vanus Connect.
4. Paste the two credentials from Slack as configurations.
      ![](images/token%20and%20secret.png)
5. Click **Next** and continue the configuration. 

---

### Step 3: Configure Event Subscription
1. Click the **copy icon** to copy the webhook URL.
![](images/img_10.png)
2. Go back to **Slack API**.
![](images/img_5.png)
3. Now click on **Event Subscriptions** in the side menu.
![](images/img_6.png)
4. **Enable Events** by turning on the switch.
![](images/img_7.png)
5. Use the URL we've previously copied and paste it into **Request URL**. You should see a green `Verified`, indicating our Source is verified by Slack.
![](images/img_8.png)

---

### Step 4: Subscribe to bot events

Generally speaking, Slack Source can subscribe to any events you need from Slack.

But, if you're using some **Vanus Templates** like `Send a custom greeting message when new members join the Slack channel`, then subscribe to `member_joined_channel`.

#### How to subscribe

1. Scroll down, click **Subscribe to bot events** and after, you will be able to click **Add Bot User Event**.
![](images/img_9.png)
2. Select the events you will like to receive.
![](images/member_joined.png)
3. Finally, you can **Save Changes** to complete your configuration.
![](images/save%20changes.png)

---

### Step 5: Install the Slack App to your Slack Workspace

1. Go to **Install Apps** from the side menu and click **Install to Workspace**.
   ![](images/img_13.png)
2. Allow it to be installed into your Workspace.
      ![](images/img_14.png)
3. Mention your bot in Slack and invite it to the channel.
   ![](images/add-to-channel.png)

---
