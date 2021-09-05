Deploy 3-node K8S on your Mac

1. vagrant up
2. ansible-playbook -i inventory/hosts roles/main.yml
3. vagrant ssh kc1
4. sudo -s
5. kubectl get no