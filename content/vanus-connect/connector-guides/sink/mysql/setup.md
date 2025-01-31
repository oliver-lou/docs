# MySQL

This guide contains information required in setting up an MySQL Sink in Vanus Connect.  

## Introduction  

MySQL is a popular open-source relational database management system used to store, organize, and retrieve data for websites, applications, and other software.

Vanus Connect's MySQL sink connector simplifies the process of transferring data/events from various sources to a MySQL database/table, with configurable filters and upsert/insert modes.
## Prerequisites

Before forwarding events to MySQL, you must have:

- A [**Vanus Cloud account**](https://cloud.vanus.ai)
- Have a running MySQL server.
- Have a Database and Table created.

**Perform the following steps to configure your MySQL Sink.**

### MySQL Connection Settings

Enter all the following information in Vanus Connect.

![](images/mysql-sink-1.webp)

- **Host**① - The IP address of your MySQL Server.
- **Port**② - The Port of your MySQL Server: 3306.
- **Username**③ - A Username with the following permissions INSERT, UPDATE, DELETE.
- **Password**④ - The user password.
- **Database**⑤ - The database name.
- **Table**⑥ - The table name.
- Choose the **insertion mode**⑦.
- Click on **Next**⑧ to continue the configuration.

## Custom Connection

The event data must be in JSON format and created following the structure of your database, here's an example:

```json
{
  "title": "value",
  "date": "value",
  "ect...": "value"
}
```
