# conditional_vars

### Steps:

 * Clone the repo
 * cd conditional_vars
 * Make any changes to you want to the files under (vi group_vars/<filename>
 * Run the playbook (only runs on the localhost)
 
 ````
 $ ansible-playbook run.yaml
[WARNING]: provided hosts list is empty, only localhost is available. Note that the implicit localhost does not match 'all'

PLAY [localhost] ************************************************************************************************************************

TASK [Include cloud conditional vars] ***************************************************************************************************
ok: [localhost]

TASK [Include Azure vars] ***************************************************************************************************************
ok: [localhost]

TASK [Create AZURE build config] ********************************************************************************************************
changed: [localhost]

TASK [Include Azure vars] ***************************************************************************************************************
ok: [localhost]

TASK [Create AWS build config] **********************************************************************************************************
changed: [localhost]

PLAY RECAP ******************************************************************************************************************************
localhost                  : ok=5    changed=2    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
````

 * Now check your template files have been created correctly.

````
$ ls -al /tmp/a*
-rw-rw-r-- 1 ubuntu ubuntu 627 May 15 15:55 /tmp/aws-ipi-install-config.yaml
-rw-rw-r-- 1 ubuntu ubuntu 955 May 15 15:55 /tmp/azure-ipi-install-config.yaml
````

