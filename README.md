# Ansible-Grafana

## Inventory Changes

`vm2 ansible_host=192.168.1.1 ansible_user=user ansible_ssh_pass=pass ansible_become_pass=pass`
* Cambiar host a la IP donde se ejecutara ansible
* Cambiar user a donde sera ejecutado

## Docker compose Changes

`user: "1000"` Verfificar que el usuario usado sea donde se ejecutaran los contendedores.

## Como usar
* Iniciar 2VM
* En la Vm donde se alojara la app crear dentro de la carpeta docker la carpeta grafana y dentro la carpeta provisioning`mkdir -p grafana/provisioning`
* Abrir las 2VM y ejecutar en la que este ansible el comando `start_grafana.yml` para levantar los servicios
* Ejecutar `stop_grafana.yml` para bajar los servicios
