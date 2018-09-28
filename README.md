# About

Sample demo app with Jenkins X

# Useful commands

* create issue in git

```shell
$ jx create issue -t 'update readme'
```
* get build logs

```shell
$ jx get build logs
```

* get apps deployed in staging/production

```shell
$ jx get applications
```

* promote version to production

```shell
$ jx promote --version <version> --env production --timeout 1h
```

* find-out url from differed environments:

```shell
$ jx open --env <environment>
$ jx open --env staging
```
* export secrets and copy to other namespace

```shell
kubectl get secret gitlab-registry --namespace=source-ns --export -o yaml |\
kubectl apply --namespace=destination-ns -f -
```

