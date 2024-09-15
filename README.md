# Bad bots ASN list

A list of ASNs to block bad bot traffic on your Cloudflare firewall.

## Purpose
This repository provides a collection of ASNs (Autonomous System Numbers) that are commonly associated with malicious bots, crawlers, and other unwanted traffic sources.<br>
Blocking these ASNs can help reduce unwanted activity on your website and improve its overall security and performance.

## How to Use

### 1. Download the List
You can find the list of ASNs in the `ASN.txt` file in this repository.<br>
You can either download this file directly or copy the ASNs to use in your Cloudflare firewall.

### 2. Add to Cloudflare Firewall

To block traffic from these ASNs in Cloudflare:

1. Log into your [Cloudflare dashboard](https://dash.cloudflare.com/).
2. Select the website you want to protect.
3. Navigate to **Security** > **WAF** > **Tools**.
4. In the **IP Access Rules** section:
    - Select **ASN** from the dropdown menu under "IP, IP range, country name, or ASN".
    - Paste the ASN from the list into the **Value** field.
    - Under **Action**, select **Block** to prevent traffic from this ASN.
    - Under **Zone**, choose either **This website** to apply the block to the current website, or **All websites in account** to apply the block across all domains in your Cloudflare account.
    - (Optional) Add any relevant **Notes** to identify or describe the blocked ASN.
5. Click **Add** to implement the block.

### 3. Monitor and Adjust
While blocking ASNs from known bad bots can be effective, it's important to regularly monitor your site's traffic and firewall logs.<br>
Occasionally, legitimate users may share the same ASN as bad bots, so it’s a good idea to review and update the ASN list periodically to avoid blocking valid traffic.

## Contributing
If you have additional ASNs that are known to be associated with bad bots, feel free to contribute by submitting a pull request.<br>
Ensure that the ASNs are thoroughly tested and verified to avoid false positives.

## Disclaimer
This list is provided as a tool to help mitigate bad bot traffic, but it is not a comprehensive solution.<br>
Blocking by ASN is one layer of protection, and it’s recommended to use additional security measures for complete protection.
