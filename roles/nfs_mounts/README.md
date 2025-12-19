# NFS_MOUNTS

## Variables
| Variable | Desription | Required? |
| --- | --- | --- |
| host | The ip or hostname of the server that is hosting the nfs share | Yes |
| share | The specific shared folder you want to mount from the host | Yes |
| mount_path | The folder on the node that you want the nfs share to be mounted at | Yes |
| source | A combination of "host" and "share".  Can be used instead of the two separate variables | No |
| mount_options | The mount options.  Defaults to  "rw,sync,hard" | No |

## Examples
```
ansible-playbook -vv nfs_mounts.yml -e "host=192.168.1.10 share=/data mount_path=/data"
ansible-playbook -vv nfs_mounts.yml -e "source=192.168.1.10:/data mount_path=/data"
```
