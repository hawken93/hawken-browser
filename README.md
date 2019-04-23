# hawken-browser

Deployment of sane system wide defaults for firefox (and chromium later)

## Requirements

Tested on debian 10/buster and ubuntu 18.04

## TODO

* chromium hardening

## Role Variables

```
hawken_browser_certificates: []
hawken_browser_firefox:
  enabled: yes
  certificates:
    enabled: no
    names: []
hawken_browser_chromium:
  enabled: yes
```

hawken\_browser\_certificates are certificates on the destination that will be
copied into the browsers.

hawken\_browser\_\*.certificates.names are a list of certificates to import,
set this to the basenames of the hawken\_browser\_certificates

enabled means this browser will be installed and configured.

Each of the browsers will have more options coming as the role advances, but
they will probably differ. A goal is to try to make them as uniform as possible
but no guarantees can be made.

## Dependencies

Avoiding this.

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
