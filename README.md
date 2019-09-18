# EVALUACION-DEVOPS-1

el siguente codigo permite desplegar una VM, instalar ansible, docker y desplegar un servicio web, de la evaluacion asignada se cumplen los siguientes puntos.


A: creacion de una máquina virtual con Vagrant y provisionar un docker engine con Ansible usando ansible-playbook

B: Desplegar una aplicación dockerizada sobre la VM usando Ansible

C: Crear un repositorio en Github con todos los archivos necesarios para crear la infraestructura virtual y un README file con la documentación para replicar el escenario y un diagrama que explique el flujo.

#FLUJO DE EJECUCION

1.-	el archivo vagrantfile define las caracteristicas de la VM que se crearan sobre la virtual Box

2.- el archivo vagrantfile provisiona/instala ansible_local a la VM creada.

3.- el archivo vagranfile ejecuta un playbook de ansible llamado "playbook.yml" en la carpeta "ansible"