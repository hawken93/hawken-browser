# hawken-browser

Deployment of sane system wide defaults for firefox (and chromium later)

## Requirements

Only tested on debian buster (10). Do other debian-based at your own risk.
But tell me if it worked or what you need for it to work.

## Role Variables

```
hawken_browser_firefox:
  enabled: yes
hawken_browser_chromium:
  enabled: yes
```

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
