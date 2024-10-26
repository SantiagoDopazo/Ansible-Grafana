# Ansible-Grafana

## Installation

Instalar docker en la VM deseada
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
<<<<<<< HEAD
* Abrir las 2VM y ejecutar en la que este ansible el comando `ansible-playbook deploy_monitoring.yml` para crear todo el entorno y levantarse
* `ansible-playbook stop_grafana.yml` para parar los servicios
* `ansible-playbook start_grafana.yml` para volverlos a levantar
=======
* Iniciar 2VM
* En la Vm donde se alojara la app crear dentro de la carpeta docker la carpeta grafana y dentro la carpeta provisioning`mkdir -p grafana/provisioning`
* Abrir las 2VM y ejecutar en la que este ansible el comando `start_grafana.yml` para levantar los servicios
* Ejecutar `stop_grafana.yml` para bajar los servicios
>>>>>>> 932d6053455b79a52197bfaf8070f0e09fefdd9e
