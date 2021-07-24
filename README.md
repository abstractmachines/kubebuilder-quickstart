# Kubebuilder quickstart

  ```sh
  kubebuilder init --domain my.domain --repo my.domain/guestbook
  ```

## Create API (CR and Controller opts, yes)
```
kubebuilder create api --group webapp --version v1 --kind Guestbook
```

## Test it out: Install CRDs into cluster
```
make install
```

## Test it out: Run the Controller
```
make run
```

## In new tab, install instances of custom resources
```
kubectl apply -f config/samples/
```

## Run It On the Cluster
Build and push your image to the location specified by IMG:

```
make docker-build docker-push IMG=<some-registry>/<project-name>:tag
```

## Deploy the controller to the cluster with image specified by IMG:

```
make deploy IMG=<some-registry>/<project-name>:tag
```

## Operate the custom resource / get
```
kubectl get guestbook
```

## Get custom resource YAML
```
kubectl get guestbook -oyaml
```
- ... we could also add a shortname here and perform crud w kubectl api on that resource's shortname...
- ... we could add a label and select/delete/operate on, all custom resources which have that label ...

## Uninstall CRDs
```
make uninstall
```

## Undeploy Controller
```
make undeploy
```
