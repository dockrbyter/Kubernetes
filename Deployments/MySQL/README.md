# MySQL Deployment
### PREPERATION

```bash
mkdir -p $HOME/kubernetes/manifests/mysql
cd $HOME/kubernetes/manifests/mysql
```
Copy the YAMLs into this directory.  

```bash
echo -n 'SUP3RST0NGP@ssW04D' | base64
```
Copy the output into `secret_mysql.yml` at `MYSQL_ROOT_PASSWORD`.  

Check the ports in `service_mysql.yml` to adjust them as you need it.  
Edit the resources spec in `deployment_fivem.yml` acording to your cluster.  
Edit also `pvc_mysql.yml` acording to your clusters storage system.

### APPLY FILES
```bash
kubectl apply -f secret_mysql.yml
kubectl apply -f pvc_mysql.yml
kubectl apply -f service_mysql.yml
kubectl apply -f deployment_mysql.yml
```

## LINKS
- Image MySQL: https://hub.docker.com/_/mysql  
