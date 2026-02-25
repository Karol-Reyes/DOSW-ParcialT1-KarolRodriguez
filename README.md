# DOSW-ParcialT1-KarolRodriguez
---
## PUNTO 1
El diagrama de contexto generado para este caso de estudio es el siguiente:

![Diagrama](DOSW-ParcialT1/docs/images/ContextDiagram.png)

En el cual, nos centramos en las funcionalidades generales de las que debe de encargarse en sistema completo para cumplir con las espectativas originadas por los usuarios funcionales

---
## PUNTO 2
Los patrones de diseño que pueden ser aplicados a este caso de estudio en especifico pueden ser los siguientes:

### 1er patrón

**Patrón seleccionado:** Adapter

**Tipo de patrón:** patrones estructurales

**Justificación:** la razón principal para escoger este patron como una de las formas de desarrollo para este caso de uso es por el formato que deben recibir los datos. Como tal, nos brindan especificaciones concretas sobre la información que solicita SILABINFO para generar la reserva, los cuales son muy detallados y en especial, necesitan de 1 solo dato como tal.
El mejor ejemplo de ello:
- Enlace envía una cadena de este tipo: 1_DOSW_Desarrollo y Operaciones Softwar y SILABINFO solo solicita la parte "DOSW"
- Recursos humanos brinda la información: 2083853,Laura Herrera,laura.herrera@escuelaing.edu.co y SILABINFO solo busca "laura.herrera@escuelaing.edu.co"

Por ello, es necesario que se presente una conversion entre clases, en donde por medio de un adaptador, generaríamos una extracción más limpia y precisa de los datos que realmente necesita SILABINFO y con ello podríamos enviar estos mismos directamente, en lugar de enviar datos innecesarios y/o no utilizables
### 2do patrón

**Patrón seleccionado:** Chain of Responsability

**Tipo de patrón:** patrones comportamentales

**Justificación:** la razón principal para la eleccion de este tipo de patron en específico son los diversos requerimientos y limitaciones que se pueden presentar a la hora de generar una reserva.
Los mejores ejemplos de ello:
- Tiempo máximo de reserva de sala/laboratorio
- Solo se puede generar la reserva de oficinas para los profesores
- La reserva necesita tener obligatoriamente una asociación a una materia

Por ello y mas limitaciones, es que la mejor manera de trabajar con este caso de uso es este patrón, ya que no solamente se encarga de verificar hermeticamente el cumplimiento de todas las posibles solicitudes con las que se esten trabajando, sino que tambien se secciona y delega la responsabilidad de paso a un solo lugar en específico sin la necesidad de exteneder innecesariamente 1 solo código

---
## PUNTO 3
### Requerimientos del Sistema

El sistema de SILABINFO, en terminos de requerimientos funcionales y NO funcionales, debe tener la capacidad de:

**Requerimientos Funcionales**

1. Verificar si un usuario es administrativo/docente o estudiante
2. Confirmar o denegar la reserva de los usuarios segun las reglas de cada tipo de recurso
3. Llevar una validación y disponibilidad actualizada sobre las diversas salas que pueden ser reservadas

**Requerimientos no Funcionales**

1. Mantener los colores alusivos al programa de Ingeniería de Sistemas
2. Ser responsive

---
## PUNTO 4
**Caso de Uso 1**
![UseCase1](DOSW-ParcialT1/docs/images/CasoUso1.png)

**Historias de Usuario 1**

***Usuario***

- **COMO:** usuario de la plataforma SILABINFO
- **QUIERO:** poder generar o eliminar reservas en la aplicación según diversos requerimientos necesarios para las actividades académicas a desarrollar a lo largo del semestre
- **PARA:** poder desarrollar y compartir diversas actividades académicas con mis compañeros de estudio en un ambiente más relajado, con todos los dispositivos necesarios para el desarrollo de las mismas y sin tanta contaminación audiovisual en el entorno

***Jefe Sistema***

- **COMO:** Jefe del sistema de la plataforma SILABINFO
- **QUIERO:** poder confirmar o denegar las reservas generadas por los usuarios a traves de la aplicación
- **PARA:** brindar un espacio de desarrollo académico más cómodo y util para los usuarios que cumplan con las restricciones y especificaciones de cada sala

**Caso de Uso 2**
![UseCase2](DOSW-ParcialT1/docs/images/CasoUso2.png)

**Historias de Usuario 2**

***Usuario***

- **COMO:** Usuario del sistema
- **QUIERO:** poder verificar la disponibilidad de las salas
- **PARA:** poder definir cuales salan estan disponibles y así, poder generar una reserva en la que sea más conveniente para las actividades que necesito realizar

***Jefe del Sistema***

- **COMO:** Jefe del sistema de la plataforma SILABINFO
- **QUIERO:** validar la disponibilidad de las diversas salas que pueden ser reservadas por los usuarios de la plataforma
- **PARA:** poder llevar un control actualizado y en tiempo real de las diversas reservas gestionadas hasta el momento y así, brindar la información a los usuarios de aquellas salas que aún presentan disponibilidad
