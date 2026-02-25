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
