Deploy 3-node K8S on your Mac

1. vagrant up
2. ansible-playbook -i inventory/hosts roles/main.yml
3. vagrant ssh kc1
   1. sudo kubectl create -f https://docs.projectcalico.org/manifests/tigera-operator.yaml
   2. wget https://docs.projectcalico.org/manifests/custom-resources.yaml
   3. sed -i 's/192.168.0.0/10.10.0.0/g' custom-resources.yaml
   4. sudo kubectl apply -f customer-resources.yaml