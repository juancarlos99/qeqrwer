<span id="anchor"></span>Información del sistema
------------------------------------------------

1.  **arch**: mostrar la arquitectura de la máquina (1).
2.  **uname -m**: mostrar la arquitectura de la máquina (2).
3.  **uname -r**: mostrar la versión del kernel usado.
4.  **dmidecode -q**: mostrar los componentes (hardware) del sistema.
5.  **hdparm -i /dev/hda**: mostrar las características de un disco duro.
6.  **hdparm -tT /dev/sda**: realizar prueba de lectura en un disco duro.
7.  **cat /proc/cpuinfo**: mostrar información de la CPU.
8.  **cat /proc/interrupts**: mostrar las interrupciones.
9.  **cat /proc/meminfo**: verificar el uso de memoria.
10. **cat /proc/swaps**: mostrar ficheros swap.
11. **cat /proc/version**: mostrar la versión del kernel.
12. **cat /proc/net/dev**: mostrar adaptadores de red y estadísticas.
13. **cat /proc/mounts**: mostrar el sistema de ficheros montado.
14. **lspci -tv**: mostrar los dispositivos PCI.
15. **lsusb -tv**: mostrar los dispositivos USB.
16. **date**: mostrar la fecha del sistema.
17. **cal 2011**: mostrar el almanaque de 2011.
18. **cal 07 2011**: mostrar el almanaque para el mes julio de 2011.
19. **date 041217002011.00**: colocar (declarar, ajustar) fecha y hora.
20. **clock -w**: guardar los cambios de fecha en la BIOS.

<span id="anchor-1"></span><span id="anchor-2"></span><span id="anchor-1"></span>Apagar (Reiniciar Sistema o Cerrar Sesión)
---------------------------------------------------------------------------------------------------------------------------

1.  **shutdown -h now**: apagar el sistema (1).
2.  **init 0**: apagar el sistema (2).
3.  **telinit 0**: apagar el sistema (3).
4.  **halt**: apagar el sistema (4).
5.  **shutdown -h hours:minutes &**: apagado planificado del sistema.
6.  **shutdown -c**: cancelar un apagado planificado del sistema.
7.  **shutdown -r now**: reiniciar (1).
8.  **reboot**: reiniciar (2).
9.  **logout**: cerrar sesión.

<span id="anchor-3"></span><span id="anchor-4"></span><span id="anchor-3"></span>Archivos y Directorios
-------------------------------------------------------------------------------------------------------

1.  **cd /home**: entrar en el directorio “home”.
2.  **cd ..**: retroceder un nivel.
3.  **cd ../..**: retroceder 2 niveles.
4.  **cd:** ir al directorio raíz.
5.  **cd ~user1**: ir al directorio user1.
6.  **cd –**: ir (regresar) al directorio anterior.
7.  **pwd**: mostrar el camino del directorio de trabajo.
8.  **ls**: ver los ficheros de un directorio.
9.  **ls -F**: ver los ficheros de un directorio.
10. **ls -l**: mostrar los detalles de ficheros y carpetas de un directorio.
11. **ls -a**: mostrar los ficheros ocultos.
12. **ls \*\[0-9\]**\*: mostrar los ficheros y carpetas que contienen números.
13. **tree**: mostrar los ficheros y carpetas en forma de árbol comenzando por la raíz.(1)
14. **lstree**: mostrar los ficheros y carpetas en forma de árbol comenzando por la raíz.(2)
15. **mkdir dir1**: crear una carpeta o directorio con nombre ‘dir1’.
16. **mkdir dir1 dir2**: crear dos carpetas o directorios simultáneamente (Crear dos directorios a la vez).
17. **mkdir -p /tmp/dir1/dir2**: crear un árbol de directorios.
18. **rm -f file1**: borrar el fichero llamado ‘file1’.
19. **rmdir dir1**: borrar la carpeta llamada ‘dir1’.
20. **rm -rf dir1**: eliminar una carpeta llamada ‘dir1’ con su contenido de forma recursiva. (Si lo borro recursivo estoy diciendo que es con su contenido).
21. **rm -rf dir1 dir2**: borrar dos carpetas (directorios) con su contenido de forma recursiva.
22. **mv dir1 new\_dir**: renombrar o mover un fichero o carpeta (directorio).
23. **cp file1**: copiar un fichero.
24. **cp file1 file2**: copiar dos ficheros al unísono.
25. **cp dir /\* .**: copiar todos los ficheros de un directorio dentro del directorio de trabajo actual.
26. **cp -a /tmp/dir1 .**: copiar un directorio dentro del directorio actual de trabajo.
27. **cp -a dir1**: copiar un directorio.
28. **cp -a dir1 dir2**: copiar dos directorio al unísono.
29. **ln -s file1 lnk1**: crear un enlace simbólico al fichero o directorio.
30. **ln file1 lnk1**: crear un enlace físico al fichero o directorio.
31. **touch -t 0712250000 file1**: modificar el tiempo real (tiempo de creación) de un fichero o directorio.
32. **file file1**: salida (volcado en pantalla) del tipo mime de un fichero texto.
33. **iconv -l**: listas de cifrados conocidos.
34. **iconv -f fromEncoding -t toEncoding inputFile &gt; outputFile**: crea una nueva forma del fichero de entrada asumiendo que está codificado en fromEncoding y convirtiéndolo a ToEncoding.
35. **find . -maxdepth 1 -name \*.jpg -print -exec convert ”{}” -resize 80×60 “thumbs/{}” \\;**: agrupar ficheros redimensionados en el directorio actual y enviarlos a directorios en vistas de miniaturas (requiere convertir desde ImagemagicK).

<span id="anchor-5"></span><span id="anchor-6"></span><span id="anchor-5"></span>Encontrar archivos
---------------------------------------------------------------------------------------------------

1.  **find / -name file1**: buscar fichero y directorio a partir de la raíz del sistema.
2.  **find / -user user1**: buscar ficheros y directorios pertenecientes al usuario ‘user1’.
3.  **find /home/user1 -name \\\*.bin**: buscar ficheros con extensión ‘. bin’ dentro del directorio ‘/ home/user1’.
4.  **find /usr/bin -type f -atime +100**: buscar ficheros binarios no usados en los últimos 100 días.
5.  **find /usr/bin -type f -mtime -10**: buscar ficheros creados o cambiados dentro de los últimos 10 días.
6.  **find / -name \\\*.rpm -exec chmod 755 ‘{}’ \\;**: buscar ficheros con extensión ‘.rpm’ y modificar permisos.
7.  **find / -xdev -name \\\*.rpm**: Buscar ficheros con extensión ‘.rpm’ ignorando los dispositivos removibles como cdrom, pen-drive, etc.…
8.  **locate \\\*.ps**: encuentra ficheros con extensión ‘.ps’ ejecutados primeramente con el command ‘updatedb’.
9.  **whereis halt**: mostrar la ubicación de un fichero binario, de ayuda o fuente. En este caso pregunta dónde está el comando ‘halt’.
10. **which halt**: mostrar la senda completa (el camino completo) a un binario / ejecutable.

<span id="anchor-7"></span><span id="anchor-8"></span><span id="anchor-7"></span>Montando un sistema de ficheros
----------------------------------------------------------------------------------------------------------------

1.  **mount /dev/hda2 /mnt/hda2**: montar un disco llamado hda2. Verifique primero la existencia del directorio ‘/ mnt/hda2’; si no está, debe crearlo.
2.  **umount /dev/hda2**: desmontar un disco llamado hda2. Salir primero desde el punto ‘/ mnt/hda2.
3.  **fuser -km /mnt/hda2**: forzar el desmontaje cuando el dispositivo está ocupado.
4.  **umount -n /mnt/hda2**: correr el desmontaje sin leer el fichero /etc/mtab. Útil cuando el fichero es de solo lectura o el disco duro está lleno.
5.  **mount /dev/fd0 /mnt/floppy**: montar un disco flexible (floppy).
6.  **mount /dev/cdrom /mnt/cdrom**: montar un cdrom / dvdrom.
7.  **mount /dev/hdc /mnt/cdrecorder**: montar un cd regrabable o un dvdrom.
8.  **mount /dev/hdb /mnt/cdrecorder**: montar un cd regrabable / dvdrom (un dvd).
9.  **mount -o loop file.iso /mnt/cdrom**: montar un fichero o una imagen iso.
10. **mount -t vfat /dev/hda5 /mnt/hda5**: montar un sistema de ficheros FAT32.
11. **mount /dev/sda1 /mnt/usbdisk**: montar un usb pen-drive o una memoria (sin especificar el tipo de sistema de ficheros).

<span id="anchor-9"></span><span id="anchor-10"></span><span id="anchor-9"></span>Espacio de Disco
--------------------------------------------------------------------------------------------------

1.  **df -h**: mostrar una lista de las particiones montadas.
2.  **ls -lSr |more**: mostrar el tamaño de los ficheros y directorios ordenados por tamaño.
3.  **du -sh dir1**: Estimar el espacio usado por el directorio ‘dir1’.
4.  **du -sk \* | sort -rn**: mostrar el tamaño de los ficheros y directorios ordenados por tamaño.
5.  **rpm -q -a –qf ‘%10{SIZE}t%{NAME}n’ | sort -k1,1n**: mostrar el espacio usado por los paquetes rpm instalados organizados por tamaño (Fedora, Redhat y otros).
6.  **dpkg-query -W -f=’${Installed-Size;10}t${Package}n’ | sort -k1,1n**: mostrar el espacio usado por los paquetes instalados, organizados por tamaño (Ubuntu, Debian y otros).

<span id="anchor-11"></span><span id="anchor-12"></span><span id="anchor-11"></span>Usuarios y Grupos
-----------------------------------------------------------------------------------------------------

1.  **groupadd nombre\_del\_grupo**: crear un nuevo grupo.
2.  **groupdel nombre\_del\_grupo**: borrar un grupo.
3.  **groupmod -n nuevo\_nombre\_del\_grupo viejo\_nombre\_del\_grupo**: renombrar un grupo.
4.  **useradd -c “Name Surname ” -g admin -d /home/user1 -s /bin/bash user1**: Crear un nuevo usuario perteneciente al grupo “admin”.
5.  **useradd user1**: crear un nuevo usuario.
6.  **userdel -r user1**: borrar un usuario (‘-r’ elimina el directorio Home).
7.  **usermod -c “User FTP” -g system -d /ftp/user1 -s /bin/nologin user1**: cambiar los atributos del usuario.
8.  **passwd**: cambiar contraseña.
9.  **passwd user1**: cambiar la contraseña de un usuario (solamente por root).
10. **chage -E 2011-12-31 user1**: colocar un plazo para la contraseña del usuario. En este caso dice que la clave expira el 31 de diciembre de 2011.
11. **pwck**: chequear la sintaxis correcta el formato de fichero de ‘/etc/passwd’ y la existencia de usuarios.
12. **grpck**: chequear la sintaxis correcta y el formato del fichero ‘/etc/group’ y la existencia de grupos.
13. **newgrp group\_name**: registra a un nuevo grupo para cambiar el grupo predeterminado de los ficheros creados recientemente.

<span id="anchor-13"></span><span id="anchor-14"></span><span id="anchor-13"></span>Permisos en Ficheros (Usa ”+” para colocar permisos y ”-” para eliminar)
------------------------------------------------------------------------------------------------------------------------------------------------------------

1.  **ls -lh**: Mostrar permisos.
2.  **ls /tmp | pr -T5 -W$COLUMNS**: dividir la terminal en 5 columnas.
3.  **chmod ugo+rwx directory1**: colocar permisos de lectura ®, escritura (w) y ejecución(x) al propietario (u), al grupo (g) y a otros (o) sobre el directorio ‘directory1’.
4.  **chmod go-rwx directory1**: quitar permiso de lectura ®, escritura (w) y (x) ejecución al grupo (g) y otros (o) sobre el directorio ‘directory1’.
5.  **chown user1 file1**: cambiar el dueño de un fichero.
6.  **chown -R user1 directory1**: cambiar el propietario de un directorio y de todos los ficheros y directorios contenidos dentro.
7.  **chgrp group1 file1**: cambiar grupo de ficheros.
8.  **chown user1:group1 file1**: cambiar usuario y el grupo propietario de un fichero.
9.  **find / -perm -u+s**: visualizar todos los ficheros del sistema con SUID configurado.
10. **chmod u+s /bin/file1**: colocar el bit SUID en un fichero binario. El usuario que corriendo ese fichero adquiere los mismos privilegios como dueño.
11. **chmod u-s /bin/file1**: deshabilitar el bit SUID en un fichero binario.
12. **chmod g+s /home/public**: colocar un bit SGID en un directorio –similar al SUID pero por directorio.
13. **chmod g-s /home/public**: desabilitar un bit SGID en un directorio.
14. **chmod o+t /home/public**: colocar un bit STIKY en un directorio. Permite el borrado de ficheros solamente a los dueños legítimos.
15. **chmod o-t /home/public**: desabilitar un bit STIKY en un directorio.<span id="anchor-15"></span>**chmod o-t /home/public**: desabilitar un bit STIKY en un directorio.<span id="anchor-16"></span>**chmod o-t /home/public**: desabilitar un bit STIKY en un directorio.<span id="anchor-15"></span>**chmod o-t /home/public**: desabilitar un bit STIKY en un directorio.

<span id="anchor-17"></span><span id="anchor-18"></span><span id="anchor-17"></span>Archivos y Ficheros comprimidos
-------------------------------------------------------------------------------------------------------------------

1.  **bunzip2 file1.bz2**: descomprime in fichero llamado ‘file1.bz2’.
2.  **bzip2 file1**: comprime un fichero llamado ‘file1’.
3.  **gunzip file1.gz**: descomprime un fichero llamado ‘file1.gz’.
4.  **gzip file1**: comprime un fichero llamado ‘file1’.
5.  **gzip -9 file1**: comprime con compresión máxima.
6.  **rar a file1.rar test\_file**: crear un fichero rar llamado ‘file1.rar’.
7.  **rar a file1.rar file1 file2 dir1**: comprimir ‘file1’, ‘file2’ y ‘dir1’ simultáneamente.
8.  **rar x file1.rar**: descomprimir archivo rar.
9.  **unrar x file1.rar**: descomprimir archivo rar.
10. **tar -cvf archive.tar file1**: crear un tarball descomprimido.
11. **tar -cvf archive.tar file1 file2 dir1**: crear un archivo conteniendo ‘file1’, ‘file2′ y’dir1’.
12. **tar -tf archive.tar**: mostrar los contenidos de un archivo.
13. **tar -xvf archive.tar**: extraer un tarball.
14. **tar -xvf archive.tar -C /tmp**: extraer un tarball en / tmp.
15. **tar -cvfj archive.tar.bz2 dir1**: crear un tarball comprimido dentro de bzip2.
16. **tar -xvfj archive.tar.bz2**: descomprimir un archivo tar comprimido en bzip2
17. **tar -cvfz archive.tar.gz dir1**: crear un tarball comprimido en gzip.
18. **tar -xvfz archive.tar.gz**: descomprimir un archive tar comprimido en gzip.
19. **zip file1.zip file1**: crear un archivo comprimido en zip.
20. **zip -r file1.zip file1 file2 dir1**: comprimir, en zip, varios archivos y directorios de forma simultánea.
21. **unzip file1.zip**: descomprimir un archivo zip.

<span id="anchor-19"></span><span id="anchor-20"></span><span id="anchor-19"></span>Paquetes Deb (Debian, Ubuntu y derivados)
-----------------------------------------------------------------------------------------------------------------------------

1.  **dpkg -i package.deb**: instalar / actualizar un paquete deb.
2.  **dpkg -r package\_name**: eliminar un paquete deb del sistema.
3.  **dpkg -l**: mostrar todos los paquetes deb instalados en el sistema.
4.  **dpkg -l | grep httpd**: mostrar todos los paquetes deb con el nombre “httpd”
5.  **dpkg -s package\_name**: obtener información en un paquete específico instalado en el sistema.
6.  **dpkg -L package\_name**: mostar lista de ficheros dados por un paquete instalado en el sistema.
7.  **dpkg –contents package.deb**: mostrar lista de ficheros dados por un paquete no instalado todavía.
8.  **dpkg -S /bin/ping**: verificar cuál paquete pertenece a un fichero dado.

<span id="anchor-21"></span><span id="anchor-22"></span><span id="anchor-21"></span>Actualizador de paquetes APT (Debian, Ubuntu y derivados)
---------------------------------------------------------------------------------------------------------------------------------------------

1.  **apt-get install package\_name**: instalar / actualizar un paquete deb.
2.  **apt-cdrom install package\_name**: instalar / actualizar un paquete deb desde un cdrom.
3.  **apt-get update**: actualizar la lista de paquetes.
4.  **apt-get upgrade**: actualizar todos los paquetes instalados.
5.  **apt-get remove package\_name**: eliminar un paquete deb del sistema.
6.  **apt-get check**: verificar la correcta resolución de las dependencias.
7.  **apt-get clean**: limpiar cache desde los paquetes descargados.
8.  **apt-cache search searched-package**: retorna lista de paquetes que corresponde a la serie «paquetes buscados».

<span id="anchor-23"></span><span id="anchor-24"></span><span id="anchor-23"></span>Ver el contenido de un fichero
------------------------------------------------------------------------------------------------------------------

1.  **cat file1**: ver los contenidos de un fichero comenzando desde la primera hilera.
2.  **tac file1**: ver los contenidos de un fichero comenzando desde la última línea.
3.  **more file1**: ver el contenido a lo largo de un fichero.
4.  **less file1**: parecido al commando ‘more’ pero permite salvar el movimiento en el fichero así como el movimiento hacia atrás.
5.  **head -2 file1**: ver las dos primeras líneas de un fichero.
6.  **tail -2 file1**: ver las dos últimas líneas de un fichero.
7.  **tail -f /var/log/messages**: ver en tiempo real qué ha sido añadido al fichero.

<span id="anchor-25"></span><span id="anchor-26"></span><span id="anchor-25"></span>Manipulación de texto
---------------------------------------------------------------------------------------------------------

1.  **cat file1 file2 .. | command &lt;&gt; file1\_in.txt\_or\_file1\_out.txt**: sintaxis general para la manipulación de texto utilizando PIPE, STDIN y STDOUT.
2.  **cat file1 | command( sed, grep, awk, grep, etc…) &gt; result.txt**: sintaxis general para manipular un texto de un fichero y escribir el resultado en un fichero nuevo.
3.  **cat file1 | command( sed, grep, awk, grep, etc…) » result.txt**: sintaxis general para manipular un texto de un fichero y añadir resultado en un fichero existente.
4.  **grep Aug /var/log/messages**: buscar palabras “Aug” en el fichero ‘/var/log/messages’.
5.  **grep ^Aug /var/log/messages**: buscar palabras que comienzan con “Aug” en fichero ‘/var/log/messages’
6.  **grep \[0-9\] /var/log/messages**: seleccionar todas las líneas del fichero ‘/var/log/messages’ que contienen números.
7.  **grep Aug -R /var/log/**\*: buscar la cadena “Aug” en el directorio ‘/var/log’ y debajo.
8.  **sed ‘s/stringa1/stringa2/g’ example.txt**: reubicar “string1” con “string2” en ejemplo.txt
9.  **sed ‘/^$/d’ example.txt**: eliminar todas las líneas en blanco desde el ejemplo.txt
10. **sed ‘/ \*\#/d; /^$/d’ example.txt**: eliminar comentarios y líneas en blanco de ejemplo.txt
11. **echo ‘esempio’ | tr ‘\[:lower:\]’ ‘\[:upper:\]’**: convertir minúsculas en mayúsculas.
12. **sed -e ‘1d’ result.txt**: elimina la primera línea del fichero ejemplo.txt
13. **sed -n ‘/stringa1/p’**: visualizar solamente las líneas que contienen la palabra “string1”.
