BEERVPN
=========

Install beervpn backend.

After run this role just write to your bot:

- /start
- /init PASSWORD
- /generate

After last command you will recive .ovpn cerificates as telegram files.

When users will write to bot you (as admin) will be recive notify with actions:

- /allow ${user_id} || Allow user to recive generate and recive configuration
- /block ${user_id} || blacklist user
- /clear || ignore

Requirements
------------

Tested on Debian 9 stretch, but must work on all systemd/debian based system.

Role Variables
--------------

- tg_bot_password: Password to auth user
- tg_bot_token: Token from t.me/botfather

Dependencies
------------

- egeneralov.iptables
- egeneralov.base
- egeneralov.openvpn

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      vars:
        tg_bot_password: BeerVPN
        tg_bot_token: 000000000:AAAAAAAAAAAAAAAAAAAAAAAA-AAAAAAAAAA
      roles:
         - { role: username.rolename, x: 42 }

License
-------

MIT

Author Information
------------------

Eduard Generalov <eduard@generalov.net>
