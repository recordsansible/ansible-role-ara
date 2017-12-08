ansible-role-ara
================

Ansible role to install and configure ARA on Fedora, RHEL, Fedora as well as
Debian and Ubuntu.

ARA_ (Ansible Run Analysis) records Ansible_ Playbook runs seamlessly to make
them easier to visualize, understand and troubleshoot. It integrates with
Ansible wherever you run it.

.. _ARA: https://github.com/openstack/ara
.. _Ansible: https://www.ansible.com/

Note
----

Please note that this role is still a work in progress and in development.

What the role does
------------------

By default, the role allows for the installation of ARA and the `configuration
of Ansible`_ to leverage the ARA callback.
It also allows for the configuration of the `different parameters`_ to customize
the behavior of ARA.

It provides installation and configuration of the web application under the
`embedded webserver or apache+mod_wsgi`_.

.. _configuration of Ansible: http://ara.readthedocs.io/en/latest/configuration.html#ansible
.. _different parameters: http://ara.readthedocs.io/en/latest/configuration.html#ara
.. _embedded webserver or apache+mod_wsgi: http://ara.readthedocs.io/en/latest/webserver.html

Using the role
--------------

You can get the role using the following commands:

::
    mkdir roles
    git clone https://git.openstack.org/openstack/ansible-role-ara roles/ara

By default, the embedded server will be use, you have to edit defaults/main.yaml to set
use_apache_server to True

Create a simple playbook to do the deployment:

::
    mkdir roles
    git clone https://git.openstack.org/openstack/ansible-role-ara roles/ara
    cat << EOF > playbook.yml
    - hosts: all
      roles:
        - ara
    EOF
    ansible-playbook playbook.yml

Contributors
============
See contributors on GitHub_.

.. _GitHub: https://github.com/openstack/ansible-role-ara/graphs/contributors

Copyright
=========
Copyright 2017 Red Hat, Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
