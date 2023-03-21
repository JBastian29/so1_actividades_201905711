# Systemd Service
Para crear un systemd unit de tipo servicio para ejecutar un script que imprima un saludo y la fecha actual, sigue estos pasos:

* Crea un archivo con extensión ".service" en la siguiente ruta:

      /etc/systemd/system/
    
* Abre el archivo y escribe el siguiente código:

      [Service]
      ExecStart=/ruta/al/script.sh

      [Install]
      WantedBy=multi-user.target

* En el campo *ExecStart* se debe colocar la ruta absoluta del script que quieres ejecutar. Asegúrate de que el script tenga permisos de ejecución.

* El campo *WantedBy* indica en qué nivel de ejecución del sistema debe iniciarse el servicio. En este caso, se ha indicado *multi-user.target*, lo que significa que el servicio se iniciará en el nivel de ejecución multiusuario.

* Guardar el archivo y cerrar.

* El script del saludo a ejecutar seria:

      #!/bin/bash
      echo "¡Hola usuario! La fecha actual es $(date)"
