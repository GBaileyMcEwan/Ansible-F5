For information on how to get started with Ansible and F5, go to: https://clouddocs.f5.com

There are 4 playbooks in this folder:
  1) installDocker.yaml         - This playbook works off a vanilla Ubuntu installation and installs all docker pre-requisites.  Then it 
                                  pulls a hackazon container and starts up 3 instances of it on the host.
  2) f5nodepoolvs.yaml          - This playbook manually (with static IP addresses - this could and should be done better with dynamic,
                                  but I used static for the purposes of proving a concept) adds the 3 containers to a F5 pool and creates                                   a VS with a SSL profile and preconfigured WAF profile.                       
  3) uninstallf5nodepoolvs.yaml - rolls back the f5nodepoolvs.yaml config on the F5
  4) uninstallDocker.yaml       - rolls back the installDocker.yaml config on the Ubuntu installation
                        
