ec2_persistent_volume
=========

Read the list of volumes descriptions and create/remove them. Then do snapshot backup
and expiration on backup if required.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

- `ec2_persistent_volumes` - List of ec2 volumes to be created or delete

- `force_volume_creation` - Boolean - Optional - Default is False (not doing it)

  This enforce the volume to be removed and then created from the last known
  backup snapshot. The removal may fail if the volumes are still attached to
  ec2 instances which is a kind of protection.

Dependencies
------------


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
