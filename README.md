# Monitor Wall Ansible Playbook

This repo contains the Ansible Playbook used to provision all machines within the ACM Monitor Wall setup. This is a 20-monitor wall located in the ACM@UIC.


## Dev environment setup

We assume you have the following packages installed:

* Python 3
* Molecule (`python3 -m pip install --user molecule`)
* Docker (https://docs.docker.com/engine/install/)


## Testing locally

We utilize Molecule to test our Ansible playbook changes locally. Instead of having to be physically at the machine, we can virtualize most of the environment setup.

Use `molecule list` to see the available scenarios for the project. In general, we have two main scenarios: `head` and `display`.

**head** - This is responsible for coodinating all the display nodes.

**display** - This is responsible for showing and rendering a picture to an attached screen.

Use `molecule create -s {head,display}` to start creating a local environment.

Once created, you can use `molecule login -s {head,display}` to login to each respective scenario.

After you are done, you can destroy the local environment to using `molecule destory -s {head,display}`. It is encouraged to recreate scenarios often to ensure you are always making changes via code.

## How to start contributing?

Start by taking a look at any of the available issues on our Github project. You may need to be familiar with writing Infrastructure as Code using Ansible. SIG SysAdmin has prior presentations that you can check out. If you have specific questions, we invite you to ask your questions in the #💻sig-sysadmin channel on the ACM@UIC Discord server. See the ACM@UIC website for the most up-to-date details on how to join.
