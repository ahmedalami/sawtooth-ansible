This repository provides a set of generic Ansible playbooks that can be used as building blocks for creating a Hyperledger Sawtooth network targeting development or production environments. These playbooks also support adding and removing PBFT nodes and are conform to the 1.2.5 release and ahead.

Two vagrant files are provided for testing purposes, one with one node targeting a developement mode and another defining four nodes a production mode.

# Development environment
The provided playbook can set up a local Sawtooth node to test your application against. Once the node is running, you will be able to submit new transactions and fetch the resulting state and block data from the blockchain using HTTP and the Sawtooth REST API.

```shell
ansible-playbook -i vagrant/dev playbooks/setup.yaml -e "@vagrant/dev.yaml"
```

# Production environment
The provided playbook can to install, configure, and run Hyperledger Sawtooth on a Ubuntu system for proof-of-concept or production use in a Sawtooth network.          

```shell
ansible-playbook -i vagrant/network playbooks/setup.yaml -e "@vagrant/network.yaml"
```
