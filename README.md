# Ansible-Grafana

## Inventory Changes

`vm2 ansible_host=100.00.00 ansible_user=suser ansible_ssh_pass=pass ansible_become_pass=pass`
* Cambiar host a la IP donde se ejecutara ansible
* Cambiar user a donde sera ejecutado

## Docker compose Changes

`user: "1000"` Verfificar que el usuario usado sea donde se ejecutaran los contendedores.

## Como usar
* Abrir las 2VM y ejecutar en la que este ansible el comando `start_grafana.yml` para levantar los servicios
* Ejecutar `stop_grafana.yml` para bajar los servicios