

# Upgrading Flux

## Installing Flux

Install or Update the Flux CLI following the instruction on the [Flux website](https://fluxcd.io/flux/installation/)


## Upgrading flux v2

Run the  `flux` cli commands below locally

 ```bash

flux install --namespace=flux-system --azure-autologin-for-acr --export --components source-controller,kustomize-controller,helm-controller,notification-controller,image-reflector-controller,image-automation-controller > ./clusters/snd/base/flux-system/gotk-components.yaml

```


As Flux in PTL makes use of optional GOTK image automation components, we generate a second `gotk-components.yaml` file just for PTL. Information about Flux GOTK components can be found [here](https://fluxcd.io/flux/components/).


