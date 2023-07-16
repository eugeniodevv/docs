# DNS Setup

## 1. Log in to your DNS console
Login to your DNS provider and click on the domain you want to protect.
We will assume you are using [Cloudflare](https://dash.cloudflare.com) to manage your domain in this guide.

## 2. Remove existing DNS records
Please check your current DNS records for existing backend servers (real IP addresses).
You need to delete any record that points to one of your backend servers to avoid attacks, which are targeting your server IP directly.

If your backend server IP was public it is generally a good idea to request a new one from your provider
to keep your backend IP safe.

## 3. Create a protected DNS record
Login to our [Panel](https://panel.neoprotect.net) and go to the domain settings of your server.
There you can see the protected CNAME record of your server. Click on the copy button on the right to save it for the next step.

If you want to host your Minecraft server and website on the same domain/subdomain
you must use a SRV record instead of a CNAME record.
Otherwise, it is recommended to use a "CNAME" record for the next step.

### CNAME setup
- Create a new record with the type "CNAME".
- Enter your desired domain as the name of the record (like "mc.server.com", or "server.com")
- Use the protected CNAME you already copied and put it in the target field.
- Set the TTL to 1 or 2 minutes (if you're using Cloudflare select auto).
- Ensure that the Cloudflare proxy (orange cloud) is disabled!

### SRV setup
- Create a new record with the type "SRV"
- Enter your desired domain as the name of the record (like "mc.server.com", or "server.com")
- Set the following values:
- Service: _minecraft
- Protocol: TCP
- TTL: 1 or 2 minutes (if you're using Cloudflare select auto)
- Priority: 10
- Weight: 0
- Port: 25565
- Use the protected CNAME you already copied and put it in the target field.

After you filled out all the required details, click on **save**.
Now you can securely connect to your server using the domain, you just set up.

Please keep in mind that it can take some minutes before your DNS records are applied by your provider.

:::info

If you need any help with the setup you can contact our [Support](../support.md).

:::