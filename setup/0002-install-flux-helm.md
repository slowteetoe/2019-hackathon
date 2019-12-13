Run this command, it will install FluxCD and Helm/Tiller into the cluster.

```bash
eksctl enable repo \
 --cluster=hackathon \
 --region=us-west-2 \
 --git-user="fluxcd" \
 --git-email="${GH_USER}@users.noreply.github.com" \
 --git-url="git@github.com:${GH_USER}/${GH_REPO}"

After it runs, take the Flux SSH key, go to the github repo and add a deploy key *with write access*
