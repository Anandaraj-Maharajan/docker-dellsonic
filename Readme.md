# Prebuilt Ansible container for Dell enterprise SONiC

To write and run the Ansible playbooks to automate the switch configuration, Dell enterprise SONiC has contributed wide variety of modules in the Ansible community under 'dellemc.enterprise_sonic' collection. 

There are few basic pre-requisites for Ansible and few modules for successful execution of scripts we write in Ansible. The pre-requisites are captured [here](https://github.com/ansible-collections/dellemc.enterprise_sonic)

To ease the experience to start with the process of automation, using the Dockerfile, Dell has containerized the necessary pre-requisite install.

The docker image can be downloaded from [here](https://hub.docker.com/r/anandrajm/ansible)

After downloading the docker image to local machine, make sure to run the container with following parameters for successful operation.

>docker run -dit -v /source/script/path/in/localMachine:/destination/script/path/in/container --network host --name <container-name> <docker-image-name>

### Example

>docker run -dit -v /home/anandraj/Projects/sonic-IaC:/opt/sonic-IaC --network host --name ansible dellsonic/ansible:1.1

## Container version info
    ansible [core 2.12.3]
      config file = None
      configured module search path = ['/root/.ansible/plugins/modules', '/usr/share/ansible/plugins/modules']
      ansible python module location = /usr/local/lib/python3.8/dist-packages/ansible
      ansible collection location = /root/.ansible/collections:/usr/share/ansible/collections
      executable location = /usr/local/bin/ansible
      python version = 3.8.10 (default, Nov 26 2021, 20:14:08) [GCC 9.3.0]
      jinja version = 3.0.3
      libyaml = True

