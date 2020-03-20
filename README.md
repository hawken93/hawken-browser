# hawken-browser

Deployment of sane system wide defaults for firefox (and chromium later)

## Requirements

Tested on debian 10/buster and ubuntu 18.04

## Role Variables

Examples:
```
hawken_browser_firefox_enabled: yes
hawken_browser_chromium_enabled: yes
#hawken_browser_chromium_realm: example.com
hawken_browser_ca_certificate: no
```


* `hawken_browser_*_enabled` --- this browser will be installed and configured.
* `hawken_browser_*_systemcerts` --- use system certificates for this browser
* `hawken_browser_*_realm` --- if this is defined, where the browser will use kerberos auth
* `hawken_browser_*_av` --- Enable browser use of webcam/audio, default no

Replace '*' with firefox or chromium.

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
