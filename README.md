DISCONTINUATION OF PROJECT

This project will no longer be maintained by Intel.

Intel has ceased development and contributions including, but not limited to, maintenance, bug fixes, new releases, or updates, to this project.  

Intel no longer accepts patches to this project.

If you have an ongoing need to use this project, are interested in independently developing it, or would like to maintain patches for the open source software community, please create your own fork of this project.  

Contact: webadmin@linux.intel.com
# DLRS template for OpenFaaS

## Description
Template for OpenFaaS deployments using DLRS.

[DLRS](https://github.com/intel/stacks/tree/master/dlrs) is highly-tuned and built for cloud native environments, the release enables developers to quickly prototype by reducing complexity associated with integrating multiple software components, while still giving users the flexibility to customize their solutions.

DLRS has several flavours, the one used for this template is dlrs-tensorflow-ubuntu:v0.7.0

## Usage

```bash
faas-cli new <project name> --lang python3-dlrs
faas-cli up -f <project name>.yml
```

faas-cli up will build the image for the function, push it to the specified container registry and deploy the function to the running OpenFaaS instance. You are now ready to interact with the function.

#### Sample function

This function does nothing more than return the OS information.

```bash
$ echo test | faas-cli invoke <project name> --gateway $<your gateway>
```

#### Pix2Pix usecase using DLRS template for OpenFaaS

A machine learning application using this template is available [here](https://github.com/intel/stacks-usecase/tree/master/pix2pix).

## License
This project is licensed under the MIT license, see LICENSE file for further details.
