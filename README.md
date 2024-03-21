# Overview
sample playbook

# Environment
*  RHEL 7.8 (Maipo)
*  Install application
   - httpd 2.4.6-93
   - postgresql-server 9.2.24
   - tomcat 7.0.76


# Directory
```
.
├── ansible.cfg
├── hosts
│   └── inventory
├── httpd.yml
├── postgres.yml
├── README.md
├── roles
│   ├── httpd
│   │   ├── defaults
│   │   │   └── main.yml
│   │   ├── tasks
│   │   │   ├── httpd_install.yml
│   │   │   ├── main.yml
│   │   │   └── pre_value_check.yml
│   │   └── templates
│   │       └── index.html.j2
│   ├── postgres
│   │   ├── defaults
│   │   │   └── main
│   │   │       ├── vars.yml
│   │   │       └── vault.yml
│   │   ├── tasks
│   │   │   ├── main.yml
│   │   │   ├── postgres_install.yml
│   │   │   └── pre_value_check.yml
│   │   └── templates
│   │       └── postgresql.conf.j2
│   └── tomcat
│       ├── defaults
│       │   └── main.yml
│       └── tasks
│           ├── main.yml
│           ├── pre_value_check.yml
│           └── tomcat_install.yml
├── site.yml
└── tomcat.yml

14 directories, 22 files
```

# Syntax check
 *  yamllint
 ```
pip3 install yamllint
yamllint .
 ```

 *  ansible lint
```
pip3 install ansible-lint
ansible-lint site.yml
```

# Test
 *  Molecule
 ```
# install 
pip3 install molecule
```

# Servers
*  GPS common server
   - https://docs.google.com/document/d/1KnTfZSd2UfgvxAB3RgiZoH9MI6zPnslgPEaFwgOp6Js/edit
*  KVMs
   - manakamu-work  <-- development
   - manakamu-cw    <-- Target server


