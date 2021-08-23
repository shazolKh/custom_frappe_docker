### Introduction

- Fork this repo to build your own image with ERPNext and list of isppme Frappe apps.
- Change `nginx/Dockerfile` and add required apps. Refer comments in the file.
- Change `worker/Dockerfile` and add required apps.

This file uses following app(s):

- https://github.com/kingraphaii/isppme

### Build images

Execute from root of app repo

For nginx:

```shell
# For edge
docker build -t isppme-erpnext-nginx:latest nginx

# For version-12
docker build --build-arg=FRAPPE_BRANCH=version-12 -t isppme-erpnext-nginx:v12 nginx

# For version-13
docker build --build-arg=FRAPPE_BRANCH=version-13 -t isppme-erpnext-nginx:v13 nginx
```

For worker:

```shell
# For edge
docker build -t isppme-erpnext-worker:latest worker

# For version-12
docker build --build-arg=FRAPPE_BRANCH=version-12 -t isppme-erpnext-worker:v12 worker

# For version-13
docker build --build-arg=FRAPPE_BRANCH=version-13 -t isppme-erpnext-worker:v13 worker
```
