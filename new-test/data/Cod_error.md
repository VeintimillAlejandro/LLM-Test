                Pag. 1 

# Instrucción Técnica Placa Electrónica Elevador 2 columnas sin base  
 
 
Al poner en marcha la placa de control se visualiza inmediatamente la altura  en centímetros  a la que está  el carro en la columna. Esta altura se actualiza automáticamente conforme se hace subir o bajar el elevador, poniéndose a 0 cada vez  que se actúan los finales de carrera inferiores.  (la primera vez que se da alimentación, la lectura no será la real, el operario hará bajar el elevador hasta tocar los dos finales de carrera inferiores)  
 
Si coinciden los pulsadores subir y bajar su queda todo parado.  
 
**Al bajar y llegar a la altura de 12cm se detendrá y comenzará a pitar a una frecuencia lenta, para poder seguir bajando se tendrá que soltar la tecla de bajar y volver a pulsar, entonces el sonido del zumbador será a mayor frecuencia.**
 
Si la placa electrónica detecta una **diferencia de altura de 3cm**  durante el movimiento de subida o bajada, esta misma realizará la corrección de altura para controlar que los dos carros estén alineados.  
 

##         ❖ ALARMAS DE INSPECCIÓN Y REVISIÓN  
 
El contador se incrementará en uno cada vez que las columnas lleguen abajo y se activen los dos finales de carrera inferiores. Cuando el contador de servicios alcanza los 1000 servicios (o múltiplos de 1000) aparece el mensaje **InS** (ver imagen "Cod-Eror-InS") indicando que es necesario realizar una inspección de mantenimiento del elevador, este mensaje desaparece en 30” pero vuelve a aparecer cuando el elevador llega abajo de nuevo o cuando se conecta la alimentación de la placa de control. Cuando se alcanzan 15000 servicios (o múltiplos de 15000) se visualiza el mensaje **rEu** (ver imagen "Cod-Eror-rEu"), indicando que es preciso realizar una revisión general del elevador, este mensaje es persistente, solo desaparece del display cuando el elevador está en movimiento reapareciendo a los 5 segundos de detenerse, también aparece inmediatamente al llegar el elevador abajo y al conectar la alimentación de la placa de control.  
 
Las alarmas de inspección y de revisión pueden borrarse desde el modo de test. El contador de servicios también puede ponerse a cero, eliminando así las alarmas que provoca, también desde el modo test. En todo caso, las alarmas de inspección y revisión son s ólo para informar y no afectan a la funcionalidad.  



                Pag. 2  


##          Tipos de sensores   
SQ1 → NO 
 
    -Placa modelo 005543  
SQ2, SQ3, SQ4 → NO 
 
    -Placa modelo 007994  
SQ2, SQ3, SQ4 → NC 
(ver imagen "Esquema-Sensores")


                Pag. 3  
 
 
##          ❖ MODO TEST  
 
Manteniendo pulsadas las teclas ( -, + y E) durante 5 segundos(ver imagen "Ejemplo-Activar-Mod-Mantenimiento"), el sistema entra en un modo especial de funcionamiento llamado Test. En este modo las operaciones de Subir y Bajar el elevador son completamente funcionales, pero además es posible acceder a cierta información que puede resultar útil a la hora de diagnosticar averías.Este modo lo utilizará el servicio de asistencia técnica normalmente  
 
Las funciones disponibles son:  
• EME(ver imagen "Funcion-EME"): Valores de las señales de emergencia. (SQ4)  
• dEt(ver imagen "Funcion-dEt"): Valores de los detectores. (SQ1)  
• FCA(ver imagen "Funcion-FCA"): Valores de los finales de carrera. (SQ2 y SQ3)  
• ALS(ver imagen "Funcion-ALS"): Alturas de las columnas de mando y auxiliar.  
• Con(ver imagen "Funcion-Con"): Contador servicios.  
• SAt(ver imagen "Funcion-SAt"): Borrado de alarmas de inspección -revisión y puesta a cero del contador de servicios.  
• APR(ver imagen "Funcion-APR"): Altura programada (de 0 a 200 cm)  
• rST(ver imagen "Funcion-rST"): Permite hacer un reset de todas las funciones del elevador, colocando las alturas de las columnas a 0.  
 
 
Si estamos visualizando la función EME(señales de emergencia) y pulsamos la tecla E para ver su valor, vamos a poder contemplar los niveles a los que se encuentran las señales de emergencia. Estas son:  

1. ME#: seguridad de la columna de mando  SQ4   
2. AE#: seguridad de la columna auxiliar  SQ4    
 
A ellas se accede de forma cíclica pulsando las teclas (+) o (-). La # toma el valor 0 o 1 según la señal esté en un estado inactivo (0) o activo (1). Para salir pulsar (E).
 
                Pag. 4 
 
Con la función dEt(ver imagen "Funcion-dEt") podemos ver los valores de los detectores inductivos. Se obtienen así las señales:  
1. MA#: detector  SQ1 de la columna de mando.    
2. AA#: detector SQ1 de la columna auxiliar. 
 
Igual que antes, estas señales se obtienen de forma cíclica al pulsar las teclas (+) o (-), y la # adopta los valores 0 ó 1 según sea el valor digital de salida del detector.  Para salir pulsar (E) (ver imagen "Rotacion-dEt"). 

Mediante la función FCA(ver imagen "Funcion-FCA") se accede a los valores de las señales de los finales de carrera:  
1. MS#: final de carrera superior SQ2 de la columna de mando.    
2. MI#: final de carrera inferior SQ3 de la columna de mando.    
3. AS#: final de carrera superior SQ2 de la columna auxiliar.    
4. AI#: final de carrera inferior SQ3 de la columna auxiliar.    
 
Al pulsar  o  se va cambiando de una señal a la siguiente o la anterior, respectivamente. La # se sustituye por el valor 0 ó 1 del final de carrera correspondiente, esto es, según est é en un estado inactivo (0) o activo (1) . Para salir pulsar (E) (ver imagen "Rotacion-FCA").
 
La función ALS(ver imagen "Funcion-ALS") permite visualizar la altura de la Columna De Mando y Auxiliar. Pulsando a continuación (+) o (-) se visualiza la altura de la Columna Auxiliar y así sucesivamente.  Para salir pulsar (E)


 
                Pag. 5  
 
Mediante la función Con(ver imagen "Funcion-Con") se accede al contador de servicios visualizándose centenares de servicios. El contador de servicios cuenta los servicios realizados por el elevador y se incrementa en una unidad cada vez que el elevador llega abajo y se activan los finales de carrera inferiores de ambas columnas. El contador de servicios comienza a contar desde 0 hasta un máximo de 65.535 servicios. Por lo tanto el rango de visualización será de 0 a 655. Si se excede este número máximo de servicios el contador vuelve  a 0. 
Para salir pulsar (E).
 
Con la función SAt(ver imagen "Funcion-SAt") podemos borrar las alarmas de inspección y revisión. Esta función está reservada a los operarios del servicio técnico para que hagan los ajustes necesarios tras la oportuna inspección de mantenimiento o revisión general.  
 
Pulsando la tecla (E) pasamos a visualizar  “---“. Ahora debemos pulsar una combinación de teclas para borrar la alarma. Con la combinación  "-++--E" se visualiza InS durante 1 segundo y se borra la alarma de inspección. Con la combinación -+--+E se visualiza rEu durante 1 segundo, se pone a cero el contador de servicios y se borran las alarmas de revisión y de inspección. Cualquier otra combinación provocará la visualización no y no alterara ninguna alarma ni contador (ver "Tabla-Comb").  
 
La función APR (ver imagen "Funcion-APR") permite programar una parada de servicio. Si el cliente tiene una altura de trabajo, por ejemplo para cambiar las ruedas, siempre en la misma posición, con este parámetro se puede programar una parada. Las paradas prefijadas trabajan tanto en la subida como en la bajada. Cuando el elevador se detiene, podemos soltar y pulsar de nuevo el botón hacia arriba o hacia abajo y el elevador se pondrá en funcionamiento.  
 
Pulsar (+) o (-) para ajustar la altura deseada.  
Para validar y salir pulsar (E). 
 
La altura programada es aquella a la que el elevador se detendrá al alcanzarla, si la altura programada se pone a 0 (que es el valor por defecto), el elevador subirá mientras se mantengan pulsadas las teclas subir y hasta tocar el final de carrera de altura máxima. 



                Pag. 6  
 
La función rSt(ver imagen "Funcion-rST"), finalmente, permite hacer un reset al elevador, inicializando todas sus funciones. Pulsando la tecla E se efectuará el reset y aparecerá la visualización SI durante 1 segundo, indicando que el reset se ha realizado correctamente. Esta función puede ser utilizada por el servicio técnico para poner de nuevo en marcha el control del elevador después de haberse producido un error.  
 
Es posible salir del modo de test para volver al modo normal de funcionamiento. Para ello basta con mantener pulsadas las teclas (-), (+) y (E) simultáneamente durante 5 segundos.  
 
##              ❖ ERRORES  
 
Cuando se produce alguna condición de avería  el sistema informa al usuario del hecho por medio de un mensaje intermitente en el visualizador. Este mensaje es del tipo A## o E##, donde la A significa aviso, la E significa error y la ## corresponde a un código 
numérico de dos dígitos que identifica el error concreto que se ha producido.  
 
Para detener la visualización intermitente del error hay que pulsar la tecla (E), después de lo cual se pasa a ver la altura de la columna de mando.  
 
Si el error se ha producido en el control del elevador, éste no podrá seguir funcionando. Para recuperar su funcionalidad, será preciso apagar la placa y volverla a encender. También es posible resetear el control utilizando para ello la función rSt del modo test visto anteriormente.  
 
Procedimiento de actuación ante un error:  

• E01 y E02: se ha activado la seguridad de la columna (se ha abierto el contacto normalmente cerrado de seguridad) debido a la rotura de tuerca. Para volver a funcionar se tiene que quitar y volver a dar la alimentación o hacer un reset. También se presenta cuando falla el fusible de 24Vac  
CAUSAS:  
- Tuerca de trabajo rota  
- Cableado sensor SQ4  
- Sensor SQ4 averiado  
 
• E07 a E 09: errores de movimiento del elevador. Se ha detectado un movimiento sin haber pulsado subido o bajada. En los E07 y E09, no podremos mover el elevador, el RESET se realizará cuando los finales de carrera  de parada inferiores  estén ambos activados. 

                Pag. 7  
 
• A08 y A10: fallo de lectura de los detectores de movimiento cuando se inicia la subida o la bajada (tensión de correas, conexión detector encoder, inversor, motor).  
CAUSAS:  
- Correa de transmisión  floja o  en mal estado  
- Sensor SQ1 averiado  
- Algún contacto r averiado  
 
• A18 y A20: fallo de lectura de los detectores de movimiento de las columnas.Puede deberse a una desconexión o a una avería de los detectores o la presencia de un obstáculo. Revisar estos elementos, apagar la placa y volver a encender (o hacer un reset).  
CAUSAS:  
- Obstáculo  durante la bajada  
- Correa de transmisión  floja o  en mal estado  
- Sensor SQ1 averiado  
- Algún contacto r averiado  
 
En caso de producirse de forma seguida sin tocar antes los finales de carrera inferiores y más de 3 veces los errores A08, A10, A18, A20, a la cuarta vez no nos dejará volverlo a resetear, apareciendo el texto NO, en este momento tendremos que bajar manualmente el elevador hasta tocar los dos finales de carrera inferiores.  
 
• E22: error de separación mayor o igual de 10cm entre columnas.  
 
Cuando se da este error se presenta el mensaje E22 de forma intermitente y no podremos mover el elevador, tendremos que hacer reset, entonces el texto E22 parpadeará más rápido y ahora si nos permitirá movernos aunque solo hacia abajo, cuando el elevador ya está tocando los dos finales de carrera inferiores, el texto E22 vuelve a  parpadear otra vez de forma lenta, ahora haremos otro reset y ya se nos 
presentará la altura.
Nota: el deslizamiento excesivo de las columnas puede acarrear consecuencias muy graves para la integridad del elevador y del vehículo elevado. Se deben de tomar las debidas precauciones . 
 
• E23: error en la medida de la altura. Al acumular 3 avisos del A08 al A20 se produce este error, que es persistente (vuelve a aparecer aunque se apague la placa y se vuelva a encender). Si es necesario alinear las columnas moviéndolas manualmente. Hacer un reset de la placa.  
 
Nota: una vez producido el E23, la placa considera que la medida que se tiene de las alturas de las columnas es incorrecta, por lo que se queda bloqueada para el funcionamiento. La única forma de desbloquearla consiste en restablecer la altura de las columnas, lo cual puede hacerse de dos maneras: 
    -Mediante un reset en la posición inferior, con lo que la altura de las columnas se pone a cero (alinear antes las columnas manualmente) -Bajando manualmente las columnas hasta debajo de forma que se activen los dos finales de carrera inferiores, apagar y volver a encender la placa. Esto también se aplica al error E22  



                Pag. 8

• E24 a E41: errores de los finales de carrera. Revisar la conexión de los finales de carrera, apagar la placa y volverla a encender (o hacer un reset). En algunos casos, si como resultado de este error quedan las columnas desalineadas, puede ser necesario alinearlas manualmente. Cuando se presentan los errores E40-41 de forma intermitente no podremos mover el elevador, tenemos que hacer un reset, entonces el texto E40-41 parpadeará más rápido y ahora sí nos permitirá movernos aunque sólo hacia abajo, cuando el elevador ya está tocando los dos finales de carrera inferiores, el texto E40 (E41) vuelve a parpadear de forma lenta, ahora haremos otra vez reset (rSt) y se nos presentará la altura.

• E51 a E55:  errores de comunicaciones internas de la placa y de checksum. Pulsar la tecla de función. Si el error persiste pulsar la tecla varias veces por si hay errores acumulados.  



                Pag. 9

##        LISTADO DE LOS CÓDIGOS DE ERROR  
 
-E01: Error de seguridad en la columna de mando  por una ruptura de tuerca  SQ4 Ppal. 

-E02: Error de seguridad en la columna auxiliar  por una ruptura de tuerca  SQ4 Aux.

-E07: Error al detectarse la columna de mando moviéndose  cuando debería estar parada.

-E09: Error al detectarse la columna auxiliar moviéndose cuando debería estar parada.

-A08: Error al detectarse la columna de mando parada cuando debería estar moviéndose.

-A10: Error al detectarse la columna auxiliar parada cuando debería estar moviéndose.

-A18: Detector encoder columna de mando no responde durante el movimiento.

-A20: Detector encoder columna auxiliar no responde durante el movimiento.

-E22: Error de separación mayor o igual a 10cm entre columnas.

-E23: Error en la medida de la altura al acumular demasiados errores en los detectores.

-A24: No se detecta  el final de carrera superior de la columna de mando  SQ2 M.

-A25: No se detecta  el final de carrera inferior de la columna de mando  SQ3 M.

-A26: No se detecta  el final de carrera superior de la columna auxiliar  SQ2 A.

-A27: No se detecta  el final de carrera inferior de la columna auxiliar  SQ3 A.

-A28: Final de carrera superior de la columna de mando permanentemente activado  SQ2 M.

-A29: Final de carrera inferior de la columna de mando permanentemente activado  SQ3 M.

-A30: Final de carrera superior de la columna auxiliar permanentemente activado  SQ2 A.

-A31: Final de carrera inferior de la columna auxiliar permanentemente activado  SQ3 A.

-A40: Señal del final de carrera inferior en la columna principal durante la marcha  SQ2 M.

-A41: Señal del final de carrera inferior en la columna auxiliar durante la marcha  SQ2 M.

-E51: Error al Acceder a Memoria Externa.  

-E55: Error de Verificación de Memoria.
