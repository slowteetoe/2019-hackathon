Install AppMesh into the cluster:

```bash
eksctl enable profile appmesh \
--revision=demo \
--cluster=hackathon \
--region=us-west-2 \
--git-user="fluxcd" \
--git-email="${GH_USER}@users.noreply.github.com" \
--git-url="git@github.com:${GH_USER}/${GH_REPO}"
```

And then sync it manually:
```bash
fluxctl sync --k8s-fwd-ns flux
```
