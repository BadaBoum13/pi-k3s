# pi-k3s
Deploy K3s on raspberry cluster

## testing
ansible -i inventory.yml -m ping all


## Set up:
pip3 install -r requirements.txt
ansible-galaxy install -r requirements.yml --roles-path ./roles

ansible-playbook -i inventory.yml playbook/bootstrap.yml --diff
## TODOs

- prometheus/graphana -> VictoriaMetrics – Alternative to Prometheus with lower resource usage.
- https://kubernetes.io/docs/tasks/access-application-cluster/web-ui-dashboard/
- home assistant
- next cloud
- cert-manager – Automated TLS certificates with Let's Encrypt.
- ArgoCD – GitOps continuous deployment for Kubernetes.
- vpn : https://www.wireguard.com/
- https://pi-hole.net/

## troubleshooting
- readonly system: `sudo mount -o remount,rw / && sudo systemctl daemon-reload`
