---
title: Messenger OKTA configuration via ADMIN UI
order: 5
---

## Purpose

This page explains the steps that the developers should follow to **Integrate Messenger** with the **Identity Providers-OKTA** via Admin UI.

:::info
Messenger adapts **OKTA** for Authorization, which follows **OAuth2.0** protocol.
:::

## Integration Steps

1. Login to **OKTA** and create necessary Client Credentials.
2. Configure ADMIN UI to integrate with those Client Credentials.
3. Messenger Configuration.

## Step 1:

- Create an Okta developer account from https://developer.okta.com/signup/ (opens new window)
- In the left panel select Applications → Applications. Select 'Create App Integration'.
- On the Create a new app integration page, select OpenID Connect in the Sign-in method section.
- Choose, **Web Application** in Application Type and click next.
- In the **New web app Integration page**, fill App integration name, Grant type, Sign-in redirect URIs(http://{local_domain_name}) and Sign-out redirect URIs(http://{local_domain_name}) .

![OKTA Application](./images/OKTA.png "OKTA Apllication page")

- In Assignments, leave the Everyone default and click Save. This creates the client credentials.
- Store the Client credentials safely for later use.

## Step 2:

- In ADMIN UI → Integrations, select **+Integrations** button are the right corner. Install **OpenID Connect Messenger Configuration**.
  ![ADMIN UI Integration page](./images/Install_integration.png "ADMIN UI Integration page")
  ![ADMIN UI Integration page](./images/integration.png "ADMIN UI Integration page")
- In Configuration section, place the Discovery Uri - https://accounts.google.com/.well-known/openid-configuration.
  ![ADMIN UI Integration page](./images/Integration_properties.png "ADMIN UI Integration page")
- In Credentials section, click Configure and fill your client credentials created in Step 1. Click save.

## Step 3:

- In ADMIN UI → Messenger Configuration, enable Messenger configuration for Authenticated session.
- Select the OAuth integration created from ADMIN UI Integration from the dropdown.
  ![ADMIN UI Integration page](./images/Messenger-Okta-configuration.png "ADMIN UI Integration page")
- Now you are ready with **OKTA** set-up.
