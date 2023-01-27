# Tipos de kernel

Los cuatro tipos de kernel que han sido desarrollados hasta el momento son:

#### Kernel monolíticos

Este tipo de núcleo es aquel que facilita la abstracción del hardware subyacente sin importar su grado de potencia o variedad. Para realizar una comparación objetiva, estos núcleos son bastante complejos en cuanto a su manejo, siendo comparados con los próximos que vamos a observar.

#### Microkernel

Mejor conocidos como micronúcleos, estos son aquellos que son catalogados como mejores en comparación con el kernel monolitico, debido a que el mismo cumple una serie de pequeñas abstracciones mucho más simples que las comúnmente observadas en el kernel monolítico, y su función principal es utilizar diversas aplicaciones para facilitar su funcionalidad. Su verdadero objetivo principal, es el de implementar estos servicios de forma separada en cuanto a la política de funcionamiento del sistema, se refiere. De este modo se busca que el núcleo funcione de maravilla y sea bastante simple y organizado de utilizar.


#### Núcleos híbridos

Este tipo de kernel, es aquel que se considera una gran modificación del microkernel, que si bien son bastante similares en cuanto a diversas características, se diferencian debido a que este cuenta con un espacio adicional que cumple la función de permitir que el mismo se ejecute de forma mucho más rápida y funcional. Sin embargo, cualquiera de estos dos núcleos es bastante funcional, incluso los micronúcleos comunes, los cuales tienen un excelente rendimiento. Muchos de los sistemas operativos que se aplican hoy en día, cuentan con estos dos tipos de núcleos ya que ambos funcionan muy bien.


#### Exonúcleos

Son aquellos que si bien no cuentan con ningún tipo de abstracción, son aquellos que permiten el uso de bibliotecas. Dicho de otro modo, son núcleos que funcionan de maravilla al momento de ofrecer mucha funcionalidad, gracias a que los mismos cuentan con un acceso directo al hardware del sistema. Esto quiere decir, que gracias a esta gran característica, el desarrollador podrá ser capaz de permitir todas esas decisiones importantes en cuanto al rendimiento del sistema se refiere. Además, se caracterizan gracias a que son muy pequeños y a que esto realmente no limita su gran funcionamiento. Sin embargo, se sigue prefiriendo el uso de los dos kernel anteriores para los diversos sistemas que se utilizan hoy en día.


# User vs Kernel mode

####  User mode

Cuando se inicia una aplicación en modo usuario, Windows crea un proceso para la aplicación. El proceso proporciona a la aplicación un espacio de direcciones virtual privado y una tabla de controladores privada. Dado que el espacio de direcciones virtual de una aplicación es privado, una aplicación no puede alterar los datos que pertenecen a otra aplicación. Cada aplicación se ejecuta de forma aislada, y si una aplicación se bloquea, el bloqueo se limita a esa aplicación. Las demás aplicaciones y el sistema operativo no se ven afectados por el fallo.


####  Kernel mode

Todo el código que se ejecuta en modo kernel comparte un único espacio de direcciones virtuales. Por lo tanto, un controlador en modo kernel no está aislado de otros controladores y del propio sistema operativo. Si un controlador en modo kernel escribe accidentalmente en la dirección virtual incorrecta, los datos que pertenecen al sistema operativo o a otro controlador podrían verse comprometidos. Si un controlador en modo kernel falla, todo el sistema operativo falla.
