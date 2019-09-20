# EVALUACION-DEVOPS-1

el siguiente código permite desplegar una VM, instalar ansible, docker y desplegar un servicio web, de la evaluación asignada se cumplen los siguientes puntos.


A: creación de una máquina virtual con Vagrant y aprovisionar un docker engine con Ansible usando ansible-playbook

B: Desplegar una aplicación dockerizada sobre la VM usando Ansible

C: Crear un repositorio en Github con todos los archivos necesarios para crear la infraestructura virtual y un README file con la documentación para replicar el escenario y un diagrama que explique el flujo.

#FLUJO DE EJECUCIÓN

1.-	el archivo vagrantfile define las características de la VM que se crearan sobre la virtual Box

2.- el archivo vagrantfile aprovisiona/instala ansible_local a la VM creada.

3.- el archivo vagranfile ejecuta un playbook de ansible llamado "playbook.yml" en la carpeta "ansible"

4.- el archivo palybook.yml define cuales host son afectados y cuales roles serán ejecutados (init, docker, app).

5.- el rol init crea un usuario vagrant dentro de la vm e instala librerías

6.- el rol docker instala el servicio de docker en la vm

7.- el rol app desplega un contenedor con el servicio de nginx+php fpm partiendo de un archivo "dockerfile" ubicado en la carpeta app/nginx



luego de ejecutar "vagrant up" sobre la carpeta que contiene este proyecto podrá tener acceso al servidor de nginx desplegado viendo la pagina de php info a través de esta URL http://127.0.0.1:8080/

para iniciar el servidor de gitlab entrar a la carpeta "gitlab server" y ejecutar vagrant up este VM contiene el servicio de gitlab ce y gitlab ci para automatizar el despliegue y control de codigo, pendiente configuracion final del servicio. URL http://10.10.10.20

la carpeta k8s-vagrant contiene el proyecto para desplegar cluster de kubernetes sobre vagrant, la idea es sobre este cluster desplegar todos los servicio anteriores (server web, gitlab, CI) y crear un flujo completo sobre kubernetes, aun pendiente por terminar. para iniciar el cluster entrar a la carpeta k8s-vagrant y ejecutar vagrant up

Nota: este proyecto fue ejecutado bajo virtualBox 6.0


saludos