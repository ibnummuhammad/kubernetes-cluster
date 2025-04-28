- Install K3S by using this command

    curl -sfL <https://get.k3s.io> | sh -

- adjust k3s creds from /etc/rancher/k3s/k3s.yaml to ~/.kube/config

- Edit /etc/systemd/system/k3s.service and add below command line to disable traefik and metrics-server as ExecStart input argument

    --disable=traefik \
    --disable=metrics-server \
