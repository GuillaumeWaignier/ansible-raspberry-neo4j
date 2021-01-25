# ansible-raspberry-neo4j
Ansible playbook used to install Neo4J on a Raspberry Pi


To install neo4j do:

```bash
ansible-playbook exposed-play.yml --ask-pass
```

To change parameters, such as version, create the file as

```yaml
- name: Install neo4j
  hosts: neo4j
  roles:
    - role: neo4j
      tags: neo4j
      vars:
        - version: "4.1.2"

```

The host(s) of the PI are in file _inventory_.

