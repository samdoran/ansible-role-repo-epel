EPEL Repo
=========

Install Extra Packages for Enterprise Linux (EPEL) repository.

Requirements
------------

RHEL or CentOS >= 5

Role Variables
--------------
| Name              | Default Value       | Description          |
|-------------------|---------------------|----------------------|
| `epel_enabled` | True | Whether or not EPEL repo is enabled |
| `epel_testing_enabled` | False | Whether or not EPEL Testing repo is enabled |



Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - epel-repo

License
-------

MIT
