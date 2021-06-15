# kubernetes distcc

This is a tool that builds a distcc container and you can use kustomize to deploy it to your environment as a daemonset.

It runs on ubuntu gcc9 and distcc3.4

to use distcc, you need to gather the dns of all workers. distcc exposes hostport on all nodes to gain access to distcc