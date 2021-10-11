# invoiceninja
Quick and dirty helm chart for invoiceninja V5, inspired by spacepluk https://github.com/invoiceninja/dockerfiles/issues/94 - not finished.

# Usage example 

1. Clone this repository
2. install dependencies
3. deploy on kubernetes

## Clone the repository

```shell
git clone <URL>
```
<URL>: cf the 'copy' button on top of the source code page in github

## Install dependencies

This helm chart has a dependency on MySQL (described in the Chart.yaml file). To automatically resolve this, run the following command:

```shell
helm dependency update
```

Afterwards you should see an additional folder (charts), containing the .tgz file for mysql.

Alternatively, you can create this folder manually and put the appropriate tgz file in there (mysql-8.4.4.tgz), if you already have it.

## Deploy on kubernetes

Make sure helm connects to the right cluster with the right credentials. Then, run:

```shell
helm install invoiceninja . -f values.yaml
```


