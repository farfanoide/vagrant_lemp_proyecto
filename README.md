# Maquina virtual con stack LEMP

Esto es una maquina virtual preparada para correr una aplicacion web.

Incluye:

  - php
  - nginx
  - mysql
  - phpmyadmin

## Requerimientos:


- [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
- [Vagrant](https://www.vagrantup.com/downloads.html)


## Modo de uso:

1. Clonar este repositorio

  ```console
  git clone https://github.com/farfanoide/vagrant_lemp_proyecto
  ```
2. Ingresar al directorio creado

  ```console
  cd vagrant_lemp_proyecto
  ```

3. Colocar la aplicacion a correr dentro de una carpeta `app` dentro del repositorio clonado

  ```console
  ln -s path_a_mi_applicacion app
  ```

4. Inicializar la maquina virtual

  ```console
  vagrant up
  ```

  > Nota: este paso puede llevar bastante tiempo dependiendo de la conexion a
  > internet ya que debe bajar una imagen de ubuntu server e instalar los
  > paquetes necesarios.

## Acceso

Una vez inicializada la maquina se puede acceder a la aplicacion mediante un
navegador en http://localhost:8080

Para acceder a phpmyadmin tambien lo hacen por le navegador en la direccion
http://localhost:8080/phpmyadmin con el usuario root y sin contraseña

## Consideraciones y configuraciones:

La maquina virtual es un ubuntu server de 64bits, para cambiarla por uno de
32bits solo deben modificar el archivo `Vagrantfile` y donde dice
`ubuntu/trusty64` reelmplazar por `ubuntu/trusty32`
