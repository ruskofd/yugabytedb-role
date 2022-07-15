<p><img src="https://upload.wikimedia.org/wikipedia/en/d/d2/YugabyteLogo.png" alt="yugabyte-logo" title="yugabyte" align="top" height=160 /></p>

***YugabyteDB** is a high-performance, cloud-native distributed SQL database that aims to support all PostgreSQL features. It is best to fit for cloud-native OLTP (i.e. real-time, business-critical) applications that need absolute data correctness and require at least one of the following: scalability, high tolerance to failures, or globally-distributed deployments.*

### General informations

This Ansible role is designed to deploy and manage YugabyteDB database cluster(s).

**Table of Contents**

  - [Roles variables](#role-variables)
  - [Examples](#examples)
  - [Install and use this role](#install-and-use-this-role)

**Supported Platforms**

  - Fedora 36

**References**

  - YugabyteDB : https://github.com/yugabyte/yugabyte-db

### Role variables

The role variables are available [HERE](docs/variables.md)

### Examples

You can find some configurations examples [HERE](docs/examples.md)

### Install and use this role

* Install the role using the command-line :

  ```shell
  $ ansible-galaxy role install git+https://github.com/ruskofd/yugabytedb-role.git
  ```

* Install the collection in your projects using a `requirements.yml` file and `ansible-galaxy` command-line :

  ```YAML
  $ cat requirements.yml
  ---
  roles:
    - name: yugabytedb
      src: https://github.com/ruskofd/yugabyte-role.git
      scm: git
      version: '1.0.0'

  $ ansible-galaxy install-f -r requirements.yml
  ```

* Once the role is installed, you can use the roles in your playbooks :

  ```yaml
  - name: Install YugabyteDB cluser
    hosts: yugabyte
    roles:
      - role: yugabytedb
  ```
