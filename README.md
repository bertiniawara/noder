These are the proceedures i used

1.install ansible on the master server
2.then install openssh-server on all the servers using this cmd 'sudo apt update , sudo apt install openssh-server'
3.generate a key on the master using the cmd 'ssh-kengen -t  ed25519 -C 'ansible'
4.share the public key to the client servers
  to see the key used 'ls -la .ssh'
  then  'cat .ssh/ansible.pub '
5.to copy the keys to each server use 'ssh-copy-id  -i ~/.ssh/ansible.pub then the ip of remoteserver'
6. to connect to each now use 'ssh clientservername@ip_address ' eg ssh greatness@192.168.31.0
7. cmd to execeute ansible playbook = ansible-playbook --ask-become playbook

BONUS: to copy from files/folders used this cmd
  scp ~/Document/jenkins.ppt  greatness@192.168.31.0:~/
