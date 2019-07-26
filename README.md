With dramatically increasing demand of container orchestration specifically Kubernetes, demand to templatise K8S manifests also came to light. To handle increasing manifests, new CRDs(Custom resource definition), etc... it became obvious that we need a package manager somewhat like yum, apt, etc... However nature of Kubernetes manifest are very different than what one used to have with Yum and Apt. These manifests required a lot of templating which is now supported by Helm, a tool written in GoLang with templating feature.
### Neutral background on templating
Templating has been a driver for configuration management for a long time. While it may seem trivial for users coming from Ansible, Chef, Puppet, Salt, etc..., it is not. Once one moves to Kubernetes, first realisation is hard declarative approach that Kubernetes follows. It is difficult to make generic templating with declarative form since each application may have some unique feature and requirements. Users have been subjected to duplicate the manifests.

# Helm features
- Client side only
- Server side with tiller