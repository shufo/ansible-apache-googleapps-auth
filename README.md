ansible-apache-googleapps-auth
==============================

A playbook for Google Apps authentication with Apache.

## Overview

It will install Google Apps authentication to Apache. You can customize it by edit vars file.

## Usage

```bash
ansible-playbook site.yml
```

## vars

```vars/main.yml
# Google Apps Domain
google_apps_domain: example.com
# Append domain to username or not, `Always` always append domain. `None` append no domain.
# `Auto` append domain if username includes no `@` char.
google_apps_domain_append: Auto
# Credential cache time(sec).
google_apps_cache_creds_max: 3600
```

## Vagrant

You can test on Vagrant virtual machine.

```
vagrant up
```

## Note

This perl module uses Client Login API deprected in April 20, 2012, so it will unable login soon.
