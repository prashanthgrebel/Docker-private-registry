# Delete old images from registry
* list repos

```
curl http://192.168.1.120:5000/v2/_catalog
```
```
{"repositories":["centos","k_nginx_custom","mysql","mysql-app","nginx-pod","nginx_custom","notes","python_app-lvm","python_app-msql","python_app-mysql","spring-boot-app"]}
```
* list the takes of repo
```
curl http://192.168.1.120:5000/v2/k_nginx_custom/tags/list
```
```
{"name":"k_nginx_custom","tags":["v001","v003","v002"]}
```
