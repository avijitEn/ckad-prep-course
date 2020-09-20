[Home](https://github.com/containersandcloud/ckad-prep-course)

# Core Concepts | Kubernetes API's



### List all the API resources that are available.

<details><summary>show</summary>
<p>

```bash
kubectl api-resources
```
</p>
</details>

### List the API versions that are available.

<details><summary>show</summary>
<p>

```bash
kubectl api-versions
```
</p>
</details>

### Get documentation of various resources. For instance pods, nodes, services, etc.

<details><summary>show</summary>
<p>

```bash
kubectl explain <<resource>>
Ex:
kubectl explain pod
```

To view inner tags use --recursive

```bash
kubectl explain pod --recursive
```
</p>
</details>

### Copy files and directories to and from containers.

<details><summary>show</summary>
<p>

To copy file from local to container. In case of multi container container argument is required.

```bash
kubectl cp /local/dir <pod:name>:/path/in/container -c <container-name>
```

To copy file from container to local. In case of multi container container argument is required.

```bash
$ kubectl cp <pod:name>:/path/in/container /local/dir -c <container-name>
```
</p>
</details>
