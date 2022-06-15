# SendGrid

## To get started with Twilio SendGrid and Azure:


### ***Create Azure Subscription:***
1. visit the Azure Portal home page. 

2. select the Subscriptions icon under the Azure services menu.

3.  Select ***+Add*** to create a new subscription. 

4. A form will load with a Subscription Name field. You must add a name

5. Click Create.

### ***Create a Twillo SendGrid Account:***
1. From the Azure portal home page, select Marketplace under Azure services.

2. Click the Twilio SendGrid resource to load a page where you can select your account tier. 

3. Select Set up + subscribe. You will be taken to a page where you can assign your Twilio SendGrid account to an Azure Subscription and Resource Group.

4. Once you have completed the required fields, select Review + subscribe.

5. click the Configure account now button to be taken to the Twilio SendGrid App. 

### ***Twilio SendGrid account setup:***

1. Configure Two-factor authentication

2. Create an API key

3. Complete Sender Authentication

### ***Two-Factor Authentication:***

1. Navigate to Two-Factor Authentication in the Twilio SendGrid Settings menu

2. click Add Two-Factor Authentication.

3. A modal will open where you can complete the 2FA setup. Click Ok, Got it to continue.

4. Twilio SendGrid supports 2FA using either SMS or the Authy App. Select your preferred 2FA method, and click Next.

5. SMS users will be sent a confirmation code at the number they entered. Authy users will be sent instructions for downloading and completing the 2FA setup using the Authy app.

### API Keys

1. In the Twilio SendGrid App, navigate to API Keys in the Settings menu, and select Create API Key.

2. You must name the API key — we recommend something that will clearly differentiate the key from others you may create in the future.

3. You must also select the type of key you want to create.

        To keep your account secure, you should give each key the least privilege necessary. You can limit a key's capabilities by creating a Restricted Access key and selecting a subset of all the possible permissions.


### Sender Authentication 

Twilio SendGrid requires customers to complete Sender Authentication. This requirement protects your domain's reputation as an email sender and helps uphold legitimate sending behavior by Twilio SendGrid customers.

Setup includes domain authentication. Twilio SendGrid will provide DNS records that you must add to your domain.

### Change, unsubscribe, reactivate your Twilio SendGrid plan

You can upgrade or downgrade your Twilio SendGrid plan to accommodate your email sending needs as they change. If you no longer need the Twilio SendGrid service, you will aslo unsubscribe through the Azure portal.

1. From your Azure portal's Subscription overview page, select Resources and click your Twilio SendGrid resource

2. A detail page will load where you can modify your Twilio SendGrid subscription.

**To upgrade or downgrade your plan**

1. Change plan from the Twilio SendGrid resource detail page.

2. Change subscription will allow you to modify your Azure subscription, not your Twilio SendGrid plan.

3. Select a new plan, and click Change plan.

**To unsubscribe from Twilio SendGrid,**

1.  Unsubscribe from the Twilio SendGrid resource detail page.

2. Select an option that best describes your situation, and click Unsubscribe.
