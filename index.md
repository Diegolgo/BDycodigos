# Codigos de uso habitual para distintos lenguajes:

La siguiente es informacion que he recopilado a lo largo de los años, trabajando e investigando, descargando y editando, creando y mejorando codigo para analisis, tareas basicas, transformaciones, en distintos grupos de datos, relacionales y no relacionales.

##  Modo de uso
 Se puede buscar lo que se necesita, la mayoria del codigo esta bajo un boton (click para expandir)

### Nota Importante

*Algunas de las sintaxix, requieren librerias, o conocimiento previo, o en algunos casos que se cumplan ciertos requisitos o supuestos, trataré de dejarlos indicados con una nota en dicho comando. ( *)
donaciones

<web> https://www.paypal.com/donate/?hosted_button_id=GY2TVWP39V952 </web>


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
   
  </p> </details>


 <details><summary> crear textos con detalle de contenido </summary>
<p> 

 
   - cmd
 
   - para ejecutarlo en modo administrador, segundo boton del mouse en el icono de la aplicacion, "ejecutar como administrador" 
 
   - entrar en el directorio que necesito mapear
 
   - <code> tree >nombredearchivo.txt /f /a </code>
 
   - <code> dir /s /w >nombrededirectorio.txt </code>
   
  </p> </details>
 
 
 
 
 

  <details><summary>Como cambiar modo de disco duro a AHCI sin formatear:</summary>
  <p>
   - cmd (modo admin)
   
   - <code> bcdedit /set {current} safeboot minimal </code>
   
     #### reiniciar a la bios, activar modo ACHI y listo. entrar a windows de nuevo
   
   - cmd
   
   - <code> bcdedit /deletevalue {current} safeboot </code>
   
   - reiniciar

  </p> </details>




  <details><summary>crear .bat para cerrar programas que no se usan </summary>
  <p>  
  (por ejemplo, antes de editar, o usar algun software muy pesado)

   - creamos un archivo de texto, lo renombramos a xxx.bat y escribimos lo siguiente:
   - echo off
   - taskkil /im nombredelproceso.exe /F
   - echo off
   - exit
   
  </p> </details>


  <details><summary>desactivar programas especificos o paquetes en windows10 (11)</summary>
  <p>  

   listar aplicaciones
   

   - <code> DISM /Online /Get–ProvisionedAppxPackages | select–string Packagename </code>
   
   
   desinstalarlas (cambiando nombre del paquete)
   
   - <code> DISM /Online /Remove–ProvisionedAppxPackage /PackageName:PACKAGENAME </code>
   

  </p> </details>




  <details><summary>realizar escaneo, limpieza de estructura de SO windows en cmd</summary>
  <p>  

     - <code> sfc /scannow </code>
     

     - <code> DISM.exe /Online /Cleanup-image /Restorehealth </code>
   
   
    ***otros codigos para lo mismo por parte:
     
     -DISM /Online /Cleanup /CheckHealth
     -DISM /Online /Cleanup /ScanHealth
     -DISM /Online /Cleanup /RestoreHealth
   
   
   
  </p> </details>


   <details><summary>quitar el bloatware de windows 10 o win11</summary>
  <p> 

   - abrir powershell como admin y ejecutar el siguiente codigo:
   
   - <code>  iwr -useb https://git.io/debloat|iex </code>

   - esto creará un punto de restauracion del sistema, y lanzara un script .bat (descrito en github) con el cual puedes quitar lo innecesario de windows 
   
   - acceso al proyecto en github <code> https://gist.github.com/jumarag/738fd121c8f3a37cc6240993853a6977 </code>

  </p>  </details>



  <details><summary>comando para reiniciar a la bios desde cmd</summary>
  <p>

   <code>  shutdown /r /fw /f /t 0  </code>
   
  </p> </details>




## Bash Linux

<details><summary>mostrar</summary>
<p>
    <details><summary>herramientas para usar adb y fastboot en linux</summary>
    </p>

        La mayor parte del tiempo he usado distribuciones basadas en debian, por lo que los comandos estan enfocados en ubuntu (probados 2022)
        - sudo apt-get update
        
        <code> sudo apt-get install android-tools-adb  </code>
        <code> sudo apt-get install android-tools-fastboot </code>
        
        maquina virtual MACOS:
        - descargar el paquete https://github.com/foxlet/macOS-Simple-KVM/archive/refs/heads/master.zip
        instalar:
        <code> sudo apt-get install qemu-system qemu-utils python3 python3-pip </code>
        crear una carpeta con espacio suficiente para la maquina virtual (64gb por defecto en estos comandos)
        abrir terminal en la carpeta descarga, ya descomprimida y ejecutar (Agregar --high-sierra, --mojave, por defecto baja catalina)
        <code> bash jumpstart.sh </code>
        el comando anterior descargará un archivo BaseSystem.img
        crear el archivo que contendrá la maquina virtual
        <code> qemu-img create -f qcow2 MyDisk.qcow2 64G </code>
        abrir con editor de texto el basic.sh y pegar las siguientes lineas al final (si cambiaron el nombre MyDisk poner el que corresponda:
        -drive id=SystemDisk,if=none,file=MyDisk.qcow2 \
        -device ide-hd,bus=sata.4,drive=SystemDisk \
        en el mismo archivo, se puede editar la memoria y la cantidad de nucleos, hilos.
    
    </p></details>

   
    <details><summary>VM ORACLE </summary>
    <p>
    
        iniciar servicio lincebi (en caso que no este funcionando)
        <code> sudo -u lincebi /opt/lincebi/start-pentaho.sh </code>
        <code> sudo docker run -d -p 8080:8080 repo.stratebi.com/lincebi/lincebi-cloud:8.3 </code>
        <code> lincebi </code>
        
    </p></details>
      
    
      <details><summary> **** instalar Rstudio server en linux ubuntu ARM (ampere) *****   </summary>
      <p>
      <code>
        - sudo apt install r-base
        - sudo apt install r-base-html
        - sudo apt install r-base
        - sudo apt install r-base-core
        - sudo apt install r-recommended
        - sudo apt install -y g++ gcc gfortran libreadline-dev libx11-dev libxt-dev                     libpng-dev libjpeg-dev libcairo2-dev xvfb                     libbz2-   dev libzstd-dev liblzma-dev libtiff5                     libssh-dev libgit2-dev libcurl4-openssl-dev                     libblas-dev liblapack-dev libopenblas-base                     zlib1g-dev openjdk-11-jdk                     texinfo texlive texlive-fonts-extra                     screen wget libpcre2-dev make 
        - cd /usr/local/src
        - sudo wget https://cran.rstudio.com/src/base/R-4/R-4.2.1.tar.gz
        - sudo su
        - tar zxvf R-4.2.1.tar.gz
        - cd R-4.2.1
        - ./configure --enable-R-shlib --with-blas --with-lapack #optional
        - make
        - make install
        - cd ..
        - rm -rf R-4.2.1*
        - exit
        - R
      </code>
    
      </p>  </details>    
   
   <details><summary> Iniciar Rstudio Server  adb</summary>
   <p> 
      iniciar R Studio Server en navegador http://IP:8787/auth-sign-in?appUri=%2F
            http://144.22.33.233:8787
            usar credenciales creadas durante la instalacion
      </p>  </details>   
      
    <details><summary>comando para iniciar jupyter notebook (hub) tiene spypark</summary>
    <p>
        
     -en terminal deberia bastar
        
     -  jupter hub
      y entrar al navegador desde cualquier equipo:
        http://144.22.33.233:8000/
   
  </p> </details>


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


  <details><summary>ocultar texto, para expandir al hacer click (collapse), (eliminar los espacios despues de cada <)</summary>
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
 
