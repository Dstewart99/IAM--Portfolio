# Lab 01: Application Setup with OIN

## Objective
Add a pre-built app integration from the Okta Integration Network (OIN), configure SAML 2.0 sign-on, and assign a group to the application.

## Environment
- Okta Integrator Free Plan org
- Salesforce Developer Edition
- Admin Console

## Steps

### Add App from OIN
1. Go to **Admin Console → Applications → Applications**
2. Click **Browse App Catalog**
3. Search for **Salesforce.com**
4. Click **Add Integration**

### Configure General Settings
1. Set **Instance Type** to **Production**
2. Enter your **Salesforce Organization ID**
3. Click **Next**

### Configure Sign-On Options
1. Select **SAML 2.0** as the sign-on method
2. Click **Done**

### Set Up Lifecycle Management
1. Click the **Provisioning** tab
2. Click **Configure API Integration**
3. Check **Enable API Integration**
4. Click **Authenticate with Salesforce.com**
5. Click **To App** → **Edit**
6. Enable **Create Users**, **Update User Attributes**, **Deactivate Users**
7. Click **Save**

### Assign Group to Application
1. Click the **Assignments** tab
2. Click **Assign → Assign to Groups**
3. Select **IT Security Team**
4. Click **Done**

### Verify User Access
1. Click the **Assignments** tab
2. Click **People** filter
3. Confirm assigned users appear with **Active** status

## Screenshots
![Sign-On Options](sign-on-options.png)
![Group Assignment](group-assignment.png)


## Why This Matters
**IAM Relevance:** OIN integrations enable centralized SSO and provisioning across enterprise applications.

**Okta Platform Use:** SAML 2.0 allows Okta to act as the Identity Provider, controlling access to Salesforce without users needing separate credentials.

**Business Value:** Reduces credential sprawl, improves security posture, and simplifies access management at scale.
