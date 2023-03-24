<div align="center">

![PHP IMAP2](docs/logo.png)
![PHP IMAP2](docs/acmarkLogo.png)

# PHP IMAP2

</div>

## Requirements

- PHP >= 7.0

## Install

```shell
composer require javanile/php-imap2:dev-acmark
```

## Usage

```php
$mbh = imap2_open($server, $username, $token, OP_XOAUTH2);
if (! $mbh) {
    error_log(imap2_last_error());
    throw new \RuntimeException('Unable to open the INBOX');
}
```

## Gmail OAuth2

Scope: https://mail.google.com/

## Sandbox

- [Gmail Demo](https://replit.com/@frabik/PHP-IMAP2-Google-Demo?v=1#main.php)
- Outlook Demo - **COMING SOON**


## Contributors

- [dicode-nl](https://github.com/dicode-nl)
- [glensc](https://github.com/glensc)
- [bago](https://github.com/bago)

## Other links 

- <https://php.libhunt.com/php-imap2-alternatives>

## Reference

### Microsoft Outlook

- <http://wiki.canfigure.net/en/guides/exchange-oauth2>

### IMAP & OAUTH

- <https://www.atmail.com/blog/imap-commands/>
- <https://developers.google.com/gmail/imap/xoauth2-protocol>
- <https://github.com/ddeboer/imap/issues/443#issuecomment-1172158902>

### Modified fork of javanile/php-imap2 by kovarjan

- added support for flags in imap2_fetch_overview() (FT_PEEK, FT_UID) - overview will not set all mail as read
