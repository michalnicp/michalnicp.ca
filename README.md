# Personal Blog - michalnicp.ca

## Setup

1. Buy a domain on namecheap.
2. Add site to cloudflare.
3. Add dns records on cloudflare.

    ```
    A      michalnicp.ca  159.203.2.17
    CNAME  www            michalnicp.ca
    ```

4. Add page rules on cloudflare. Make sure crypto page shows "Status: Active Certificate" before proceeding.

    ```
    www.michalnicp.ca/*
    Forwarding URL: (Status Code: 301 - Permanent Redirect, Url: https://michalnicp.ca/$1)

    http://michalnicp.ca/*
    Always Use HTTPS
    ```

5. Update nameservers on namecheap.

    ```
    Custom DNS

    norman.ns.cloudflare.com
    sue.ns.cloudflare.com
    ```
