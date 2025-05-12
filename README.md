# Práctica Final Ansible

Este repositorio contiene los playbooks y los ficheros de configuración usados en la práctica final de Ansible.

## Requisitos

- Ansible 2.10+ instalado.
- Vagrant y dos máquinas virtuales ('vagrant1' y 'vagrant2') con CentOS.
- En '/etc/hosts' de la máquina host se debe incluir '192.168.10.20 vagrant1' y '192.168.10.30'

## Tarea 1

### Crear los usuarios 'Carlos' y 'Marta' en ambos hosts
    
    ansible-playbook -i inventory users.yml

### Comprobar si los usuarios han sido creados en los hosts 

    ansible-playbook -i inventory verify_users.yml --check

## Tarea 2

### Desplegar Apache y su VirtualHost

    ansible-playbook -i inventory dev_deploy.yml

### Verificar el contenido web

    ansible-playbook -i inventory get_web_content.yml

### Desplegar todo desde un playbook principal

    ansible-playbook -i inventory site.yml