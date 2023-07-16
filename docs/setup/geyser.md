# Geyser Setup

## 1. Log in to your DNS console
Login to your DNS provider and click on the domain you want to protect.
We will assume you are using [Cloudflare](https://dash.cloudflare.com) to manage your domain in this guide.

## 2. Create a bedrock subdomain record
Login to our [Panel](https://panel.neoprotect.net) and go to the domain settings of your server.
There you can see the protected CNAME record of your server. Click on the copy button on the right to save it for the next step.

It's not possible to serve your Geyser instance and Website on the same Domain Name.
Anyways it's possible to serve your Geyser instance and Java server on the same Domain Name. In this case, the Java DNS record has to be of the type [SRV](dns.md#srv-setup).

### CNAME setup
- Create a new record with the type "CNAME".
- Enter your desired domain as the name of the record (like "bedrock.server.com", or "server.com").
- Use the protected CNAME you already copied from the Panel on the Bedrock / Geyser Tab and put it in the target field.
- Set the TTL to 1 or 2 minutes (if you're using Cloudflare select auto).
- Ensure that the Cloudflare proxy (orange cloud) is disabled!

After you filled out all the required details, click on **save**.
Now you can securely connect to your server using the domain, you just set up.

Please keep in mind that it can take some minutes before your DNS records are applied by your provider.

## 3. Add your Geyser backend
On our panel, go to the `Backends` section and click on `Add Backend`. Select `Bedrock Version` and enter your Geyser's IP and Port.

## 4. Connecting using the Bedrock Edition
After finishing the Setup you will be able to connect with the Minecraft Bedrock Edition using the configured Domain and Protected Port shown in the panel. Due to high demand, getting the default Bedrock port `19132` can only be requested in a ticket on our Discord. You also need to have at least the `Neo Plan` to request the default port.

:::info

If you need any help with the setup you can contact our [Support](../support.md).

:::