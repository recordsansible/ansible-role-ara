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

The default parameters of the role will install ARA and configure a persistent
systemd service to run the embedded development server::

    mkdir roles
    git clone https://git.openstack.org/openstack/ansible-role-ara roles/ara
    cat << EOF > playbook.yml
    - name: Install ARA with default settings
      hosts: localhost
      roles:
        - ara
    EOF
    ansible-playbook playbook.yml

For more configuration and deployment examples, please refer to the
``example-playbooks`` directory.

Contributors
============
See contributors on GitHub_.

.. _GitHub: https://github.com/openstack/ansible-role-ara/graphs/contributors

Copyright
=========

::

    Copyright (c) 2018 Red Hat, Inc.

    ARA is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    ARA is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with ARA.  If not, see <http://www.gnu.org/licenses/>.
