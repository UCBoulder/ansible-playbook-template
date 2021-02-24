Playbook Name
=========

A brief description of the unifying characteristic of the playbooks go here.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the playbooks should be mentioned here. For instance, if the playbooks use the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Playbook Variables
--------------

A description of the settable variables for the playbooks should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the playbooks. Any variables that are read from other playbooks and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Playbook Dependencies
------------

A list of other roles or collections hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Collection and role requirements are listed in their respective directories:
collections/requirements.yml
roles/requirements.yml

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }


Testing
-------

Because we use Red Hat it is best to try to test in as close to a redhat environment as possible. In that vein, the following environment variables are required for molecule testing to work out of the box, these can be exported as Github secrets, set locally or however you wish to bring them in:

 - RHSM_ORG_ID: The organization ID to register systems to RHSM under.
 - RHSM_POOL_ID: The pool ID to use once registered to RHSM.
 - RHSM_ACTIVATION_KEY: The activation key to use to register.

If you do not know these values, you can locate them [here](https://oit.colorado.edu/services/consulting-professional-services/systems-engineering/help/software/redhat-linux-license).

It is recommended that you create a molecule scenario per playbook, for example if you have an install playbook, create an install scenario and import the install playbook to test. A default molecule scenario has been provided for you in molecule/defaults, this can be used as a template to create alternate scenarios, copy the files into a new directory/scenario. For simple work the only adjustement needed should be changing the location if the playbook in the converge.yml file.

License
-------

AGPLv3

Author Information
------------------

Regents of the University of Colorado

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
