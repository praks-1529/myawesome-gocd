## What is this repository about ?
Having a solid and extensible CI-CD pipeline is one of the core engineering strengths of any organization. We want developers to spend as much little time as possible on deployment procedures. This repo is used to demo usage of GoCD to build a pipeline from scratch. <br/> <br/> The full blog can be found [here](https://medium.com/@prakashshanbhag/going-great-guns-with-gocd-6d270f2d185d)

# Project structure

<pre>
.
├── README.md
├── elastic_agents			( Dockerfile for gocd elastic agents )
│   └── base_images
│       ├── java8			( elastic gocd agent for java-8 env )
│       │   ├── Dockerfile		( Dockerfile)
│       │   ├── agent.yaml
│       │   └── aws.credentials         ( Please replace your keys here. Better if you get this from seccret vault instead of check-in)
│       ├── kube			( gocd agent image with kubectl installed and configuered)
│       │   └── Dockerfile
│       └── terraform			( gocd agent with terraform installed and configuered)
│           ├── Dockerfile
│           └── aws.credentials		( Please replace your keys here. Better if you get this from seccret vault instead of check-in)
└── pipelines
    └── myawesome-service-1.yaml	( Sample pipeline for service myawesome-service [https://github.com/praks-1529/myawesome] )
