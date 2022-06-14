Esto es un trabajo practico dado en la materia Sistemas Operativos de la carrera Ingeniería en Sistemas de Información de la Universidad Tecnológica Nacional (UTN Facultad Regional de Buenos Aires). 
El enunciado del mismo se encuentra cargado en este repositorio (A-MongOs - v1.3.pdf), si querés saber a detalle el funcionamiento del mismo recomiendo que lo leas.

# tp-2021-1c-impOStor

El siguiente es un sistema distribuido que tiene 3 modulos distintos los cuales hacen alusión a una parte del funcionamiento de un Sistema Operativo

Un Tripulante = Un Hilo
Una Patota = Un proceso

# DISCORDIADOR
Hace alusion a un planificador. Según el algoritmo que se esté usando envía o no a un tripulante a ejecucion
Este planificador trabaja con Round Robin o FIFO

Este discordiador da inicio al sistema comunicandose con MI-RAM y MONGO-HQ.


# MI-RAM
Representa la memoria RAM en el sistema. Reserva memoria en el mismo según el algoritmo que use.
Esta RAM trabaja tanto con Segmentacion como Paginacion + SWAP(O memoria virtual).

Este modulo no recibe comandos, pues se comunica directamente con el discordiador quien le da indicaciones de cuanta memoria reservar
según el proceso que se está ejecutando.

# MONGO-HQ
Es el fileSystem y se encarga de guardar la informacion de forma persistente mediante varios archivos que se crean a la hora de iniciarlo

Este modulo tampoco recibe comandos, recibe indicaciones del discordiador.
