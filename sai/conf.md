Skip to:
Top Bar
Sidebar
Main Content



Search

Create

Ask Rovo

6




Back to top
How-to articles
Search by title

Show more below
Updated Jun 13, 2025
Amol Vitthal Raut

Share


:pencil:
ADM Account Creation



By Mark Evans Harris Jr (Deactivated)

5 min

Listen

242

Add a reaction
In an effort to migrate us from using NTID to authenticate to the Azure Portal, we are migrating folks to using their ADM accounts.

This document attempts to most directly help you along this process with as little middle-docs as possible. The idea is: click, submit, get account with as little document filler as possible.

Once you are done, please update the ADM-UserGroup-Mappings.xlsx document so we can keep track of those who have created their ADM accounts.

Create ADM Account
Reset ADM Password
Setup MFA for ADM Account
Troubleshooting
Create ADM Account
You can request your account here: Request an Elevated Account - Compass

This can take a few minutes to one business day. It is dependent on manager approval and helpdesk usually is pretty good about filling these out.

You’ll get an email confirmation when this is complete.

If you Don't Know your ADM Account:

That's "ADM_<First initial><first six letters of last name><TMO-Number>@T-Mobile.com"

The "TMO-Number" is whatever number normally suffixes your email. My example is 237 as my email is MarkEvans.HarrisJr237@T-Mobile.com. Since my last name is exactly 6 characters, my ADM account is "ADM_MHarris237@T-Mobile.com". If your last name is greater than 6 characters, it will be limited to just the first six.

Reset ADM Password
You can reset your password here: TESS Reset Password

image-20250522-165921.png
 

NOTE: If you run into issues accessing TESS/Service-Now, you can request access to TESS. This only applies if you’ve never accessed it before.

You’ll get an email when the request is “fulfilled”. You may get a few emails between creation and fulfillment (such as approved, etc).

It may take some time before your password is reset. Please be patient.

After submitting the request, it may be pending for a few minutes. Once fulfilled, you can retrieve your temporary password from TESS using this link (there are very helpful screenshots on this page to get you thru this process).

image-20250527-155405.png
If you get this, try going to the bare domain itself so the SAML authentication can catch up.

Once you get your temporary password, you can navigate to MySignins to reset your password, logging in with your ADM_* account.

On this page, you may be already signed in. Use the top-right navigation and click on the bubble with your name and "Switch to Another Account".

image-20250522-171523.png
On this Login screen, sign in with your ADM account.

You can use your temporary password to login to your ADM account from here.

After you use your temporary password, you should be prompted to reset your password.
Reset your password now to something you will remember.

🥳🥳🥳

Congratulations! You've successfully reset your password!

At this time, you may get a message saying "your login was successful, but..."

Microsoft will need a few minutes to finish setting up your account.

In the meantime, let's setup your MFA!

Setup MFA for ADM Account
Now that you have reset your password, you can setup MFA.

Let's navigate to CLEAR verification: https://magenta-mfa.t-mobile.com/

This is very straightforward. Just click the buttons and follow the prompts to associate your choice of MFA.

Be ready to take a selfie and have your government-issued ID ready as this process may require a photo of you and this document.

Near the end of this process, it'll give you a TAP or a Temporary Access Passcode.

Click the button and it will let you login with that TAP.

Heads up: This TAP process is how you can associate your MFA methods! If the system times out or you don’t associate a working MFA method, you can follow this again and it will let you back to the MS My Signins to reset your MFA.

Once you are signed in, you can click on "Add Sign-In Method". Just double-check to make sure you are logged in with your MFA account:

image-20250522-171815.png
Follow the prompts to associate your MFA and please be sure to use “Security Key”.

We have not seen success with the MFA method of “Microsoft Authenticator” nor the use of “Passkeys”. Please avoid these options and select the security key.

image-20250529-182112.png
 

Once you have successfully associated your desired MFA method to your account, navigate to the Azure Portal.

Login with your ADM account. If you are already signed in, add your ADM account.

If you see this, then you are good to go!

image-20250522-172344.png
🥳🥳🥳

Congratulations and thank you so much! You've accomplished the next steps of the ADM account migration!

Troubleshooting
If you run into issues, we’ve catalogued the issues here in hopes of resolving future cases with the same issues.

Problem: “I cannot find the password in TESS after requesting password reset.”

Solution: Make sure you have requested creation of your ADM account. If a password reset ticket was closed without resetting the password, it should include helpful comments. So do look into the details of the ticket to see why it was closed.

Problem: “I cannot access the Azure Portal after resetting my password. Here’s a screenshot of what I am seeing”

image-20250522-173239.png
Solution: You have not setup your MFA yet. The fact that you can authenticate with password says password reset was successful! So, you should be good to setup your MFA and you should be good to go after that!

Problem: “I go thru the MFA process, and I get an error.”

Solution: This one is tricky. Here’s screenshots of what I’ve seen:

image-20250522-173706.png
image-20250522-173803.png
You’ll need to create a Compass ticket using this link: CLEAR Enrollment Support Request - Compass

 This will have helpdesk send you a TAP token to your inbox. You will have half an hour from the arrival of this token to use it to access MySignins and change your MFA settings.

 

Related content

Azure: Active Directory New Z_Account
Tiffany Carmichael
ADM Virtual Machine Access -- User Guide
Atul Kumar
Azure Onboarding for Developer Portal for External Users
Greg Higgins
Onboarding
Andre Junior (Deactivated)
Cloud Access Portal Onboarding
Former user (Deleted)
Azure Onboarding - External User Issue Resolution
Greg Higgins






Add a comment

Add a reaction

