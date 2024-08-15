# adp-flux-core
Flux v2 configuration for ADP cluster core components amd services

## Introduction
This repository contains the Flux configuration for the ADP cluster core components and services. The repository is structured to support multiple environments (snd, dev, tst, pre, prd) and multiple clusters per environment. The repository is structured as follows:

## Repository Structure

* `clusters` - Flux configuration for the Flux System (controllers etc) per environment
* `infra` - Flux configuration for the core services e.g. Nginx Plus per environment
* `core` - Contains the manifests for the core service (HelmRelease, HelmRepository)
* `services` - Contains a GitRepository and Kustomization per environment that points to a path in the [adp-flux-services](https://github.com/DEFRA/adp-flux-services) repostory.
```

├── clusters
│   ├── snd      
│   │   └── 01/02
│   |── dev
│   |   └── 01/02    
│   |── tst
│       └── 01/02    
├── infra                                            
│   ├── snd                                          
│   │   ├── base
│   │   └── 01/02                                    
│   |── dev
│   |    ├── base
│   |    └── 01/02
│   └── tst
│       ├── base
│       └── 01/02
├── core
|   ├── app-config-service
|   ├── azure-service-operator
|   ├── calico    
|   ├── cert-mamaner
|   ├── grafana
|   ├── nginx-ingress
├── services
   ├── base
   ├── snd                                          
   |   ├── 01
   ├── dev                                          
   |   ├── 01
   ├── tst                                          
   |   ├── 01      
   ├── pre                                          
   |   ├── 01                              
   ├── prd                                          
   |   ├── 01
```
