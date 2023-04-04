---
title: create-use-or-delete-a-permanent-api-token
displayName: API tokens
published: true
order: 60
toc:
   --1--What is a permanent API token: "what-is-a-permanent-api-token-and-when-can-it-be-used"
   --1--Create: "create-a-permanent-api-token"
   --1--Delete: "delete-an-api-token"
   --1--API tokens section: "api-tokens-section"
   --1--API token expiration notifications: "api-token-expiration-notifications"
   --1--An API token and SSO: "an-api-token-and-sso"
---
  
  
  
  
  

What is a permanent API token and when can it be used
-----------------------------------------------------

An API token is a unique identifier of an application requesting access to your account via the API.

Our API documentation describes how to get a [standard authorization token](https://apidocs.gcore.com/account#section/Authentication) with a validity period of 1 hour, to update it, use the [Refresh token](https://apidocs.gcore.com/account#tag/Account/paths/~1auth~1jwt~1refresh/post) request with a validity period of 24 hours. Such validity periods can be helpful for one-time requests.

To set up an automated process for working with our CDN service (for example, automatic cache clearing), _use a permanent API token,_ which you can create in your personal account.

Please refer to the specific product  [API documentation](https://apidocs.gcore.com/account) to check if it supports permanent API tokens.

To manage services add your permanent API token after APIKey in the authorization header: _**'**Authorization: APIKey 7711$eyJ0eXAiOiJKV'_

Create a permanent API token
----------------------------

**Note!** There is currently a limit of 50 API tokens per account

<img src="https://support.gcore.com/hc/article_attachments/9001091335185/mceclip0.png" alt="mceclip0.png">

1\. In your Personal Account, go to Profile.

2\. Open the API tokens section.

3\. Click Create API token.

The form for an API token creation will be opened.  
  
<img src="https://support.gcore.com/hc/article_attachments/9001324248465/mceclip1.png" alt="mceclip1.png">

4\. In the Token name field, specify the token name.

5\. (optional) In the Description field, you can enter additional information about the token. This is an optional field.

6\. In the Role section, specify the rights that are assigned to the created token.

**Important!** A user can create a token with a role equal to or lower than their own. This means that a user with the User role cannot create a token with the Administrators role.

7\. In the Expiration section, select the expiration date of the token:

*   Never expire means that the validity period of the token is unlimited.
*   Set expiration date option choosing this option set the expiration date of the token in the field below.                    

8\. Click the **Create** button to generate the API token. 

A pop-up window with the API token will be opened.

9\. The generated token is not stored in the system**_._** You can view it in your Personal Account only once during its creation. Copy and save the token.

10\. After you have saved the generated token, click **OK, I've copied token**. Information about the token will be displayed in the API tokens section.<img src="https://support.gcore.com/hc/article_attachments/9001368504593/mceclip2.png" alt="mceclip2.png">

Delete an API token
-------------------

Only users with the Administrators role can delete any tokens issued for the account. Users with other roles can only delete tokens that were issued only by these users.

<img src="https://support.gcore.com/hc/article_attachments/9001794722577/mceclip4.png" alt="mceclip4.png">

1.  In your Personal Account, go to Profile.
2.  Open the API tokens section.
3.  Next to the required API token, click on the three dots sign and select **Delete API token**.

API tokens section
------------------

This section displays all issued API tokens, as well as information about who issued the token,  token role, last usage, expiration date, and status.

**Important!** Only users with the Administrators role can see and manage _all tokens_ issued for the account. Users with other roles can _only see and manage the tokens that were issued by these users._

For a quick search, use :

*   Issued by filter for filtering by a user who issued a token
*   Role filter for filtering by the role assigned to the token
*   Status filter for filtering by token status: active/expired/deleted-filter

<img src="https://support.gcore.com/hc/article_attachments/9001840191505/mceclip6.png" alt="mceclip6.png">
----------------------------------------------------------------------------------------------------------

API token expiration notifications
----------------------------------

API token expiration notifications are displayed in your personal account and are sent by default to users who have issued a token and to users with the Administrators role.

You [can configure](https://support.gcorelabs.com/hc/en-us/articles/115004740445) notifications in the Notifications section of the Profile tab.  
  
<img src="https://support.gcore.com/hc/article_attachments/360018342877/notifications.png" alt="notifications.png">

Users are notified by email:

*   7 days before the token expires.
*   1 day before the token expires.

The API Tokens section will be marked with an exclamation mark if there are tokens that expire in 7 days or less.

An API token and SSO
--------------------

When logging in via SAML SSO, our system does not have information about the status of the permissions granted to the user by the provider.

Even if the provider revoked the user's access rights, their tokens will remain active for account management.

**Important!** If you need to restrict access via a permanent API token for a user with SSO authorization, delete the required token from your Personal Account.