Gmail as an email client
========================

We are all used to using our webmail portals to access one account. I log into [Yahoo! Mail](https://mail.yahoo.com/) to see my Yahoo! emails. I log into [Gmail](https://gmail.com/) to see my Gmail emails. A little known feature of Gmail is the ability to sign into other emails using the webportal! This feature is found in the *Accounts* tab in your settings under [Send mail as](https://support.google.com/mail/answer/22370?hl=en).

When using a service like ForwardEmail, they have instructions on how to setup [Send mail as](https://forwardemail.net/en/guides/send-mail-as-gmail-custom-domain).

# Enable 2-step verification
With 2-step verification, it makes your account more secure by requiring an additional layer of security. In addition to your password, you will have to supply a code that is texted to you, a Google Prompt on your phone, or using an authenticator app. For more information see [Turn on 2-step verification](https://support.google.com/accounts/answer/185839)

Open your [Google Account](https://support.google.com/accounts/answer/185839?hl=en&co=GENIE.Platform%3DDesktop) settings.
Select __Security__ from the side navigation panel.
Navigate to __2-step verification__ under the "How you sign in to Google" section.
Follow the prompts.

# Generate app password
An app password allows you to sign into your Google account with on software that doesn't support the *Sign in with Google* feature. For more information see [Sign in with app passwords](https://support.google.com/accounts/answer/185833?hl=en).

You should put a memorable app name when generating an app password. In this instance put the email address you will be using to send mail as. Save the app password generated as you will not be able to view it a second time!

# Configure Send mail as
Name: Your name
Email: *The email you want to use*
Uncheck *Treat as an alias.*
Click *Next Step*
SMTP Server: smtp.gmail.com
Port: 587
Username: *Your Gmail username*
Password: *Your app password*
Select *Secured connection using TLS*

__Note__: If you want to remove the "via forwardemail dot net" you must upgrade your plan. Following the same steps as before: `SMTP Server: smtp.forwardemail.net`, `Username: *Full alias email*`, and `Password: *Alias password*`.
