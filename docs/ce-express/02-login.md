---
id: ce-express-login
title: Logging In to CE Express
product: CE Express
version: "7.3"
category: Getting Started
order: 2
related:
  - ce-express-introduction
  - ce-express-workspace
  - ce-express-admin-user-management
---

# Logging In to __S1__

## Accessing the Application

Open [CE Express](https+TLS+secure+protocol)://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform) by typing its URL in your web browser:

```
https://<yourdomain>/ceexp
```

The URL is configured by your administrator. [CE Express](https+TLS+secure+protocol)://www.google.com/search?q=Cellular+Expert+CE+Express+web+platform) **requires HTTPS** — HTTP is not supported.

## Login Methods

[CE Express](#ce-express-overview) offers two login options:

### 1. Login with __S2__ (Recommended)

Click **Login as ArcGIS+platform)** to authenticate with your ArcGIS Enterprise organization account.

**This gives access to:**
- Network Data Management view (database tables)
- Map view (RF calculations, analysis tools, visualization)

An ArcGIS Portal account is required. Contact your administrator if you do not have one.

### 2. Login with Express Account

Click **Login with Express account** to use a Cellular Expert Express local account.

**This gives access to:**
- Network Data Management view only
- Database tables, records, and data management

> To access the Map view with an Express account, you will need to also log in with ArcGIS Enterprise+platform)+Enterprise+server+GIS) credentials later.

## Password Management

- **Reset password:** Click **Reset password** on the login page. Requires the server to be configured as a mail server.
- **Forgot ArcGIS password:** Click **Forgot password** to recover via ArcGIS Enterprise.

> Contact your [CE Express](#ce-express-overview) administrator if you cannot log in or do not have credentials.

## After Login

After successful authentication, the **Network Data Management** view opens, showing all workspaces available to your user group.

To open the Map view: select a [workspace](#kw:creating-a-workspace:ce-express-workspace) from the list → the Map view loads with that [workspace](#kw:creating-a-workspace:ce-express-workspace) active.

## Logging Out

Click the **User menu** button (top right corner) → click **Logout**.

## Related Topics

- [Introduction to CE Express →](#ce-express-introduction)
- [Workspaces →](#ce-express-workspace)
- [User Management (Admin) →](#ce-express-admin-user-management)
