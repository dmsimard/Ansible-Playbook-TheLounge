#### TheLounge Ansible Playbook  

Ansible playbook to deploy "The Lounge".

* This playbook has external role dependencies. These dependenvies can be resolved
with the ``ansible-galaxy`` command on the ``ansible-role-requirements.yml``
file.

``` bash
ansible-galaxy install -r ansible-role-requirements.yml
```

Once the dependencies have been resolved run the playbook.

* Example playbook execution

``` bash
ansible-playbook -i inventory.ini installTheLounge.yml
```

Inventory should be modified to meet the needs of the deployment. The local
inventory will deploy directly on `localhost`.

This playbook can deploy an example configuration file with sensible defaults.
To enable the provided example config set the variable
`thelounge_example_config` to `true` like so.

``` bash
ansible-playbook -i inventory.ini installTheLounge.yml -e thelounge_example_config=yes
```