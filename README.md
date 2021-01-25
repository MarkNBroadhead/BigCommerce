# BigCommerce
A collection of files that helped me customize BigCommerce

# Printable Templates
To customize the PrintableDetailedInvoice.html and PrintableInvoice.html files, you must deposit the template files onto the server via webdav. There is a skeleton template file referenced in the [BigCommerce documentation](https://developer.bigcommerce.com/stencil-docs/developing-further/customizing-invoices), however, this reduces you to less than what you get by default. [PrintableInvoice.html](./PrintableInvoice.html) aims to get you to a baseline with the ClassicNext theme. Find more [documentation here](https://support.bigcommerce.com/s/article/Customizing-the-Printable-Order-Invoice)

## Find WebDAV settings
1. Go to your site dashboard
2. Server Settings
3. File Access (WebDav)

## Upload template to site
To upload using linux util Cadaver
* Create ~/.netrc file, replacing values in ${} with actual values.  
  ```
  machine ${hostname}
  login ${username}
  password ${password}
  ```
* `cadaver ${webDavPath}` webdav path example: https://store-saklfj13423.mybigcommerce.com/dav
* `cd template`
* Backup existing templates `mget *` NOTE: Enter filenames for backups or your files will be overwritten.
* `put PrintableInvoice.html`



# API Credentials
To get API credentials, go to your Dashboard, Advanced Settings, API Accounts, then create an API account.
