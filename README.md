# Ansible-Grafana

## Installation

Instalar docker en la VM2
* Actualizar sistema
```
sudo dnf update -y
```
* Instalar Docker
```
sudo dnf install -y docker-ce
```
* Iniciar y habilitar docker
```
sudo systemctl start docker
sudo systemctl enable docker
```
* Verificar que Docker funcione
```
sudo docker run hello-world
```

## Inventory Changes

`vm2 ansible_host=192.168.1.1 ansible_user=user ansible_ssh_pass=pass ansible_become_pass=pass`
* Cambiar host a la IP donde se ejecutara ansible
* Cambiar user a donde sera ejecutado

## Como usar
* Abrir las 2VM y ejecutar en la que este ansible el comando `ansible-playbook deploy_monitoring.yml` para crear todo el entorno y levantarse
* `ansible-playbook stop_grafana.yml` para parar los servicios
* `ansible-playbook start_grafana.yml` para volverlos a levantar
