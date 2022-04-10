# Codigos de uso habitual para distintos lenguajes:

La siguiente es informacion que he recopilado a lo largo de los años, trabajando e investigando, descargando y editando, creando y mejorando codigo para analisis, tareas basicas, transformaciones, en distintos grupos de datos, relacionales y no relacionales.

##  Modo de uso
 Se puede buscar lo que se necesita, la mayoria del codigo esta bajo un boton (click para expandir)

### Nota Importante

*Algunas de las sintaxix, requieren librerias, o conocimiento previo, o en algunos casos que se cumplan ciertos requisitos o supuestos, trataré de dejarlos indicados con una nota en dicho comando. (*)


## Excel ( y VB)

## R

## Python

## SQL (consultas)

## STATA

## SPSS

## MS-DOS

Usar MS-DOS (CMD) o command.com o consola de comandos.

<details><summary>click para mostrar</summary>
<p>
  
  - inicio
  - ejecutar o buscar
  
  - cmd
  
  - para ejecutarlo en modo administrador, segundo boton del mouse en el icono de la aplicacion, "ejecutar como administrador" 
  
</p>
</details>

Como cambiar modo de disco duro a AHCI sin formatear:

<details><summary>click para mostrar</summary>
<p>

- cmd (modo admin)
- bcdedit /set {current} safeboot minimal
 #### reiniciar a la bios, activar modo ACHI y listo. entrar a windows de nuevo
- cmd
- bcdedit /deletevalue {current} safeboot
- reiniciar
 
</p>
</details>



## Bash Linux

## Android
usar adb


abrir cmd, navegar a la carpeta de ADB (se debe instalar), o abrir ventana de comandos en dicha carpeta, por ej: cd/adb
adb devices
si el dispositivo esta activo, y con modo de depuracion activado via usb, se vera su codigo. en caso contrario habilitarlo en android.

usar adb
adb restart bootloader
adb restart 

<details><summary>click para mostrar</summary>
<p>
 
desbloquear bootloader (en modo fastboot)
fastboot flashing unlock
fastboot flashin unlock_critical

bloquear bootloader % ojo que al desbloquear o bloquear el bootloader el telefono se reinicia de fabrica %

fastboot flashing lock
fastboot flashing lock_critical

 
</p>
</details>

otro

<details><summary>click para mostrar</summary>
<p>
 
  escribir aqui el texto a expandir.
 
</p>
</details>


## Gitbhub pages

ocultar texto, para expandir al hacer click (collapse), (eliminar los espacios despues de cada < ) 

<details><summary>click para mostrar</summary>
<p>

< details>< summary>click para mostrar< /summary>
< p>
 
  escribir aqui el texto a expandir.
 
< /p>
< /details>

  </p>
</details>


insertar imagenes:
usar ! [comentario] (url) sin espacios,  (el link entre parentesis)
ejemplo (quitar _ y se verá la imagen insertada: !_[imagen de gatito](https://cdn2.actitudfem.com/media/files/styles/big_img/public/images/2019/08/de-donde-salio-el-meme-del-gato-en-la-mesa-portada.jpg)
