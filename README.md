# `dhparam` Role

This is a simple little role to generate strong Diffie-Hellman key
exchange parameters for more secure SSL communications. It will ensure
that the latest OpenSSL package is installed, and then use it to generate
the parameters. Keep in mind that it will take a pretty good chunk of time
to run, but on the upside, it should only have to do so once, assuming
nothing deletes the file after it's generated.

Role Variables
--------------

    dhparam_directory: "/etc/ssl/certs"

Where the generated parameters file should live.

    dhparam_filename: "dhparam.pem"

The filename to save the parameters to.

Example Playbook
----------------

    - hosts: servers
      roles:
         - slaarti.dhparam

License
-------

Unlicense; see the LICENSE file.

Author Information
------------------

Chris Pinard <slaarti@gmail.com>
