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

crear .bat para cerrar programas que no se usan 
<details><summary>click para mostrar</summary>
<p>
(por ejemplo, antes de editar, o usar algun software muy pesado)

- creamos un archivo de texto, lo renombramos a xxx.bat y escribimos lo siguiente:
- echo off
- taskkil /im nombredelproceso.exe /F
- echo off
- exit
</p>
</details>



desactivar programas especificos o paquetes en windows10 (11)

<details><summary>click para mostrar</summary>
<p>

  listar aplicaciones

   - DISM /Online /Get–ProvisionedAppxPackages | select–string Packagename

  desinstalarlas (cambiando nombre del paquete)

   - DISM /Online /Remove–ProvisionedAppxPackage /PackageName:PACKAGENAME

</p>
</details>

realizar escaneo, limpieza de estructura de SO windows en cmd
<details><summary>click para mostrar</summary>
<p>
 
- sfc /scannow
- DISM.exe /Online /Cleanup-image /Restorehealth
 
</p>
</details>

## Bash Linux

herramientas para usar adb y fastboot en linux
<details><summary>click para mostrar</summary>
<p>
 
- sudo apt-get install android-tools-adb 
- sudo apt-get install android-tools-fastboot
 
</p>
</details>
 
## Android
usar adb

<details><summary>click para mostrar</summary>
<p>
abrir cmd, navegar a la carpeta de ADB (se debe instalar), o abrir ventana de comandos en dicha carpeta, por ej: cd/adb
adb devices
si el dispositivo esta activo, y con modo de depuracion activado via usb, se vera su codigo. en caso contrario habilitarlo en android.

para iniciar el bootloader (desde android, conectado por usb)
- adb restart bootloader
 
para reiniciar el dispositivo
- adb restart 
</p>
</details>

desbloquear bootloader (en modo fastboot)
<details><summary>click para mostrar</summary>
<p>
 
- fastboot flashing unlock
- fastboot flashin unlock_critical

bloquear bootloader % ojo que al desbloquear o bloquear el bootloader el telefono se reinicia de fabrica %

- fastboot flashing lock
- fastboot flashing lock_critical

 
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


insertar imagenes em github (webpage):
 <details><summary>click para mostrar</summary>
<p>
usar ! [comentario] (url) sin espacios,  (el link entre parentesis)
ejemplo (quitar espacio y se verá la imagen insertada: 
 
 \ ! [imagen de gatito] ( https:// ejemplo-el-meme-del-gato-en-la-mesa-portada.jpg )
 
 
 ![imagen de gatito](https://cdn2.actitudfem.com/media/files/styles/big_img/public/images/2019/08/de-donde-salio-el-meme-del-gato-en-la-mesa-portada.jpg)
 
 
  </p>
</details>
