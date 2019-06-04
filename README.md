# hawken-browser

Deployment of sane system wide defaults for firefox (and chromium later)

## Requirements

Tested on debian 10/buster and ubuntu 18.04

## Role Variables

```
hawken_browser_firefox_enabled: yes
hawken_browser_firefox_systemcerts: yes
hawken_browser_chromium_enabled: yes
#hawken_browser_chromium_realm: example.com
```

\*\_enabled means this browser will be installed and configured.

\*\_systemcerts: use system certificates

\*\_realm: if this is defined, where the browser will use kerberos auth

Each of the browsers will have more options coming as the role advances, but
they will probably differ. A goal is to try to make them as uniform as possible
but no guarantees can be made.

## Dependencies

None

## Example Playbook

```
- hosts: desktops
  roles:
    - hawken-browser
```

## License

GPLv2

## Extras

Some extensions everybody should have (firefox):

* https://addons.mozilla.org/en-US/firefox/addon/buster-captcha-solver/
* https://addons.mozilla.org/en-US/firefox/addon/ublock-origin/

## Author Information

Håkon Struijk Holmen
