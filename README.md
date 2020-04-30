# Ansible role: octorpki

Install and configure [Cloudflare OctoRPKI](https://github.com/cloudflare/cfrpki) on Debian/Ubuntu servers.

## Requirements

No requirements, install and use.


## Role Variables

There are only one dictionary variable with lot of settings (see `defaults/main.yml`):
    
    octorpki: {}

All OctoRPKI settings in this dictionary variable, see descriptions in `defaults/main.yml`

_Note: If you use `hash_behaviour=replace` in your ansible.cnf, you need to replace all `octorpki` variable or only needed parameters, otherwice variable will be overwriten._

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: rpkiserver
      vars:
        octorpki:
          metrics.addr: "0.0.0.0:8080"

      roles:
         - { role: romchi.octorpki, tags: octorpki }

License
-------

MIT / BSD

Author Information
------------------

* [Roman Bulakh <bulah.roman@gmail.com>](https://github.com/romchi)
