# vagrant_ansible_haproxy
Ejemplo vagrant+ansible+haproxy


# Descargo de responsabilidad

Este repositorio contiene pruebas realizadas a modo de hobby. Mis conocimientos de Vagrant y Ansible son prácticamente nulos.

Este contenido se basa en las siguientes referencias:

- https://fp.josedomingo.org/sri2122/u01/
- https://fp.josedomingo.org/sri2122/u06/ 
- https://www.rubydoc.info/gems/vagrant-libvirt/0.0.37

Utilizo el proveedor **libvirt** en lugar de **virtualbox**. Al parecer el primero es más eficiente.

## Prerequisitos

0. Instalar **qemu-kvm**, **virt-manager** y demás

```console
sudo apt install qemu-kvm  virt-manager
```

NOTA: puede ser que sea necesario instalar algún paquete adicional, por ejemplo: libvirt-dev


1. Instalar **vagrant**
   Ref: https://www.vagrantup.com/docs/installation

No instalar desde los repositorios de Ubuntu, sino con los siguientes comandos 

```console
curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo apt-key add -
sudo apt-add-repository "deb [arch=amd64] https://apt.releases.hashicorp.com $(lsb_release -cs) main"
sudo apt-get update && sudo apt-get install vagrant
```

2. Instalar el plugin **vagrant-libvirt**

```console
vagrant plugin install vagrant-libvirt
```

3. Instalar **ansible**

```console
sudo apt install ansible
```

## Ejecución

```console
git clone hthttps://github.com/jamj2000/vagrant_ansible_haproxy
cd vagrant_ansible_haproxy
vagrant up
```

Video: https://www.youtube.com/watch?v=eRgWCUcvzoA
