We need a lot of tools for all kinds of workflows. Here are som references in how to get them installed if you don't have them already. 
### kubectl
For documentation about kubectl see [Dockumentation](https://kubernetes.io/docs/reference/kubectl/)

Full description and additional Linux, MacOS and Windows options on [Kubernetes.io/docs](https://kubernetes.io/docs/tasks/tools/)

On x86-64 linux just getting the kubectl binary.
```bash
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
sudo mv kubectl /usr/local/bin/
```
### kustomize
For documentation about kustomize see [Dockumentation](https://kubectl.docs.kubernetes.io/references/kustomize/)
kustomize is one of many kustomization tools to bundle manifests and do some automation in handling kubernetes manifests

Full description and additional Linux, MacOS and Windows options on [kustomize github](https://github.com/kubernetes-sigs/kustomize?tab=readme-ov-file#kustomize)

On x86-64 linux just installing the kustomize binary.
```bash
curl -s "https://raw.githubusercontent.com/kubernetes-sigs/kustomize/master/hack/install_kustomize.sh"  | bash
sudo mv kustomize /usr/local/bin/
```

### helm
For documentation about helm see [Dockumentation](https://helm.sh/docs/)
Helm is a tool for bundeling kubernetes manifests into a single tarball that is kustomizable with a values file upon install, supports installation and removal hooks as well as dynamic configuration based on the installed environment.

Full description and additional Linux, MacOS and Windows options on [Installing Helm](https://helm.sh/docs/intro/install/)
On x86-64 linux just installing the helm binary.
```bash
curl -s https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3 |bash
```

### k9s
For documentation about k9s see [Dockumentation](https://github.com/derailed/k9s)
k9s is a small command line tool for navigating around your cluster. This can make it easier for beginners to get an overview until the CLI is enough for you.

Full description and additional Linux, MacOS and Windows options on [Installation defails](https://github.com/derailed/k9s?tab=readme-ov-file#installation)

On x86-64 linux just installing the k9s binary.
```bash
curl -sS https://webinstall.dev/k9s | bash
```
## Auto complete
Just because none of love to type out everything auto completion is available for most tools using `[toolname] completion [shell]` example for kubectl can be found in [kubectl Documentation](https://kubernetes.io/docs/reference/kubectl/generated/kubectl_completion/)

If on linux with bash here is a setup for all tools
```bash
sudo apt-get install bash-completion
kubectl completion bash |sudo tee /etc/bash_completion.d/kubectl
kustomize completion bash |sudo tee /etc/bash_completion.d/kustomize
helm completion bash |sudo tee /etc/bash_completion.d/helm
sudo curl https://raw.githubusercontent.com/git/git/master/contrib/completion/git-completion.bash -o /etc/bash_completion.d/git
```

other great tools to get
```bash
sudo apt-get install jq
sudo wget https://github.com/mikefarah/yq/releases/download/v4.44.5/yq_linux_amd64 -O /usr/bin/yq
```