# adp-flux-core
Flux v2 configuration for ADP cluster core components amd services

## Repository Structure
The repository is structured as follows:

* `clusters` - Flux configuration for the Flux System (controllers etc) per environment
* `infra` - Flux configuration for the core services e.g. Nginx Plus per environment
* `core` - Contains the manifests for the core service (HelmRelease, HelmRepository)
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
│   ├── nginx-ingress                                
│ 
└── apps                                            
    └── snd                                         
        └── 01
```