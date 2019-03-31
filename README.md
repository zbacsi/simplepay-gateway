# Readme

This plugin provides a payment gateway for OTP SimplePay.

## Configuration

Both the sandbox and production credentials are available on the SimplePay's admin site.
You may have access after you signed a valid contract with OTP SimplePay.

### Sandbox

The sandbox settings and credentials are located at [https://sandbox.simplepay.hu/admin/login](https://sandbox.simplepay.hu/admin/login).

#### Merchants

On SimplePay's admin panel you can access your merchant's ID (MERCHANT) and the secret key (SECRET_KEY).
Copy and paste the credentials to your WooCommerce shop's SimplePay settings page.

Be careful to paste the credentials to the correct currency.
Note, you can have more merchants set up and all of them can be stored in the plugin as well.

#### IPN/IRN URL

In the WooCommerce's SimplePay settings page, you need to copy the IPN/IRN URL and paste it to the SimplePay's admin panel,
under the technical details in your merchant. This URL will be responsible to handle requests that are being sent from SimpePay's end.
So please, copy carefully to make sure the URL is matching.

### Production

The production setup is totally the same like the sandbox, but your settings and credentials are located at
[https://admin.simplepay.hu/admin/login](https://admin.simplepay.hu/admin/login).

## Limitations

### Supported currencies

The supported currencies: `HUF`, `EUR` and `USD`.

### VAT handling

WooCommerce handles VAT differently than SimplePay.
To prevent price conflicts, prices will be passed as gross values and VAT will be 0.

### Discount handling

WooCommerce handles discounts differently than SimplePay.
Woo reduces the discount from the prodocut prices direcly.
Because of this, SimplePay will get the reduces price.
To prevent double price reduction, the discounted amount will be 0.

## Refunds

Redunds can be performed both from WooCommerce's and SimplePay's side.
Be sure, your configuration – including the IPN/IRN URL – is correct.