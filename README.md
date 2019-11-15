acme-sh
=========

Installs acme.sh for managing Let's Encrypt certificates

Requirements
------------

None.

Role Variables
--------------

| Variable Name | Default value | Description |
----------------|---------------|--------------
`acme_sh_user` | `"acme"` | User to run as
`acme_sh_staging` | true | Whether to use the Let's Encrypt staging API
`acme_sh_version` | "master" | Revision to check out
`acme_sh_certificates` | [] | Certificates to fetch, currently only HTTP
validation supported. See `defaults/main.yml` for more information

Dependencies
------------

None.

Example Playbook
----------------


    - hosts: servers
      roles:
         - role: acme-sh
           vars:
             acme_sh_user: myacmeshuser
             acme_sh_certificates:
               - primary_domain: example.org
                 webroot: /var/www/some/webroot

License
-------

BSD

Author Information
------------------

Find me on [GitHub](https://github.com/ThreeFx).
