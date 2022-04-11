# Codigos de uso habitual para distintos lenguajes:

La siguiente es informacion que he recopilado a lo largo de los años, trabajando e investigando, descargando y editando, creando y mejorando codigo para analisis, tareas basicas, transformaciones, en distintos grupos de datos, relacionales y no relacionales.

##  Modo de uso
 Se puede buscar lo que se necesita, la mayoria del codigo esta bajo un boton (click para expandir)

### Nota Importante

*Algunas de las sintaxix, requieren librerias, o conocimiento previo, o en algunos casos que se cumplan ciertos requisitos o supuestos, trataré de dejarlos indicados con una nota en dicho comando. (*)


## Excel ( y VB)

<details><summary> mostrar </summary>
<p> 
 
 </p>
</details>

## R

<details><summary> mostrar </summary>
<p> 
 
 </p>
</details>

## Python

<details><summary> mostrar </summary>
<p> 
 
 </p>
</details>

## SQL (consultas)

<details><summary> mostrar </summary>
<p> 
 
 </p>
</details>

## STATA

<details><summary> mostrar </summary>
<p>
 
 </p>
</details>

## SPSS

<details><summary> mostrar </summary>
<p> 

 </p>
</details>

## MS-DOS Windows

<details><summary> mostrar </summary>
<p> 

  <details><summary>Usar MS-DOS (CMD) o command.com o consola de comandos.</summary>
  <p>

    - inicio
    - ejecutar o buscar

    - cmd

    - para ejecutarlo en modo administrador, segundo boton del mouse en el icono de la aplicacion, "ejecutar como administrador" 

  </p>
  </details>



  <details><summary>Como cambiar modo de disco duro a AHCI sin formatear:</summary>
  <p>

   - cmd (modo admin)
   - bcdedit /set {current} safeboot minimal
     #### reiniciar a la bios, activar modo ACHI y listo. entrar a windows de nuevo
   - cmd
   - bcdedit /deletevalue {current} safeboot
   - reiniciar

  </p>
  </details>


  <details><summary>crear .bat para cerrar programas que no se usan </summary>
  <p>
  (por ejemplo, antes de editar, o usar algun software muy pesado)

  - creamos un archivo de texto, lo renombramos a xxx.bat y escribimos lo siguiente:
  - echo off
  - taskkil /im nombredelproceso.exe /F
  - echo off
  - exit
  </p>
  </details>

  <details><summary>desactivar programas especificos o paquetes en windows10 (11)</summary>
  <p>

    listar aplicaciones

     - DISM /Online /Get–ProvisionedAppxPackages | select–string Packagename

    desinstalarlas (cambiando nombre del paquete)

     - DISM /Online /Remove–ProvisionedAppxPackage /PackageName:PACKAGENAME

  </p>
  </details>



  <details><summary>realizar escaneo, limpieza de estructura de SO windows en cmd</summary>
  <p>

  - sfc /scannow

  - DISM.exe /Online /Cleanup-image /Restorehealth

  </p>
  </details>

 </p>
</details>

 ## Bash Linux

<details><summary>mostrar</summary>
<p>
   <details><summary>herramientas para usar adb y fastboot en linux</summary>
  <p>

  - sudo apt-get install android-tools-adb 
  - sudo apt-get install android-tools-fastboot

  </p>
  </details>

 </p>
</details>

## Android

<details><summary>mostrar</summary>
<p>
  <details><summary>usar adb</summary>
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


  <details><summary>desbloquear bootloader (en modo fastboot)</summary>
  <p>

  - fastboot flashing unlock
  - fastboot flashin unlock_critical

  bloquear bootloader % ojo que al desbloquear o bloquear el bootloader el telefono se reinicia de fabrica %

  - fastboot flashing lock
  - fastboot flashing lock_critical


  </p>
  </details>



  <details><summary>otro</summary>
  <p>

    escribir aqui el texto a expandir.

  </p>
  </details>

</p>
</details>

##   Gitbhub pages 

<details><summary> mostrar </summary>
<p> 


  <details><summary>ocultar texto, para expandir al hacer click (collapse), (eliminar los espacios despues de cada < ) </summary>
  <p>


   </p>
  </details>

  <details>< summary>click para mostrar</summary>
  <p>
   < details>< summary>click para mostrar< / summary>
  < p>
   escribir aqui el texto a expandir. (sin espacios)
   < /p>
  < /details>

  </p>
  </details>



  <details><summary>usar themes en github</summary>
  <p>

  Para usar themes en github con Ruby, se necesita instalar antes de usar en Fedora usar el siguiente comando antes de realizar el bundle.
   - sudo dnf install ruby ruby-devel openssl-devel redhat-rpm-config @development-tools
   - fuente y otras distros: https://jekyllrb.com/docs/installation/other-linux/

  </p>
  </details>

 
 
 
   <details><summary>insertar imagenes em github (webpage):</summary>
  <p>
  usar ! [comentario] (url) sin espacios,  (el link entre parentesis)
  ejemplo (quitar espacio y se verá la imagen insertada: 

   \ ! [imagen de gatito] ( https:// ejemplo-el-meme-del-gato-en-la-mesa-portada.jpg )


   ![imagen de gatito](https://cdn2.actitudfem.com/media/files/styles/big_img/public/images/2019/08/de-donde-salio-el-meme-del-gato-en-la-mesa-portada.jpg)


    </p>
  </details>

 </p>
</details>
 
