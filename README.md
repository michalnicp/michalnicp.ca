# Personal Blog - michalnicp.ca

## Setup

1. Buy a domain on Namecheap.
2. Create new site on Netlify. Click **New site from Git** and follow instructions.
3. Add dns records on Cloudflare. Under **DNS**, add

    ```
    CNAME  michalnicp.ca  blissful-goldwasser-0fb624.netlify.com
    CNAME  www            blissful-goldwasser-0fb624.netlify.com
    ```

4. Add page rules on Cloudflare. Make sure **Crypto** page shows "Status: Active Certificate" before proceeding. Under **Page Rules**, add

    ```
    michalnicp.ca/*
    Forwarding URL: (Status Code: 301 - Permanent Redirect, Url: https://michalnicp.ca/$1)

    http://michalnicp.ca/*
    Always Use HTTPS
    ```

5. Update nameservers on Namecheap. Under **Domain List &rarr; Nameservers**, select **Custom DNS** and add

    ```
    norman.ns.cloudflare.com
    sue.ns.cloudflare.com
    ```

6. Update custom domains on Netlify. Under **Domain management &rarr; Custom domains**, add

    ```
    www.michalnicp.ca
    michalnicp.ca
    ```
