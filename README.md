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
* check Docker-Content-Digest ID
```
curl -v --silent -H "Accept: application/vnd.docker.distribution.manifest.v2+json" -X GET http://192.168.1.120:5000/v2/k_nginx_custom/manifests/v001 2>&1 | grep Docker-Content-Digest | awk '{print ($3)}'
```
```
sha256:86e6808b4346205e71b8bbf0787e92f570ace6f08b0f6db242d706ecfd6d1740
```
