TeXLive
=========

[![Build Status](https://travis-ci.org/y-yu/ansible-texlive.svg?branch=master)](https://travis-ci.org/y-yu/ansible-texlive)

TeXLive Install Role

## Requirements

- Ansible 2.0 or higher
- rsync (if you want to install full)

## Role Variables

```yaml
# TeXLive install directory
texlive_directory:
  /usr/local/texlive

# TeXLive mirror
texlive_mirror:
  http://ftp.jaist.ac.jp/pub/CTAN/systems/texlive/tlnet
  
# TeXLive rsync URL
# This is used if you want to install full TeXLive
texlive_rsync:
  rsync://ftp.jaist.ac.jp/pub/CTAN/systems/texlive/tlnet/

# TeXLive Scheme
# full > medium > small > basic
scheme:
  small
```

## Dependencies

None

## Example Playbook

```yaml
- hosts: all
  become: yes
  roles:
    - texlive
```

## License

MIT

## Author Information

Yuu YOSHIMURA
