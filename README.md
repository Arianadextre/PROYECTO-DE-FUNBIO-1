

Link del acta semanal: https://docs.google.com/spreadsheets/d/1fDX94h6qzCRgyG9p1WOzxmcj5gEM_vUs/edit?usp=drive_link&ouid=104110057600449291254&rtpof=true&sd=true


![image](https://github.com/Arianadextre/PROYECTO-DE-FUNBIO-1/assets/143019386/191b05a1-a2ed-410e-9169-e940617c5fef)


# ¡Bienvenidos al repositorio del Grupo 5 del curso de Fundamentos de biodiseño!
## Proyecto: Determinando el glaucoma 



## ¿Quiénes somos?

Somos estudiantes de la carrera de Ingeniería Biomedíca de Pontificia Universidad Católica del Perú (PUCP) en conjunto con la Universidad Peruana Cayetano Heredia (UPCH). Buscamos diseñar soluciones tecnológicas, las cuales sean capaces de antender una necesidad en el ámbito de la salud.

## Objetivo
Trabajar todos de manera colaborativa, para así poder encontrar la propuesta de solución más factible, y así, ser capaces de afrontar la enfermedad del *Glaucoma*, de la cual hablaremos más adelante y veremos cómo esta afecta tanto a nivel nacional como internacional.

##  El equipo 5

- Alexander Martinez (Colaborador - Encargado de investigación) - alexander.martinez@upch.pe
- Jairo Villalobos (Colaborador - Encargado de la página web) - jairo.villalobos@upch.pe
- Hudson Oliva (Colaborador - Encargado de investigación) - hudson.oliva@upch.pe
- Nicolas Herrera (Colaborador - Líder y encargado de software) - nicolas.herrera@upch.pe
- Ariana Dextre (Colaborador) - Encargado de software) - ariana.dextre@upch.pe

![image](https://github.com/Arianadextre/PROYECTO-DE-FUNBIO-1/assets/143018747/2fdf4355-d1e9-4c19-b177-c2106f5e71fb)




##### Producto comercial 1
![image](https://github.com/Arianadextre/PROYECTO-DE-FUNBIO-1/assets/143019275/5d339a51-50f4-4be7-9bc2-7a69ea940f28)



##### Producto comercial 2
![image](https://github.com/Arianadextre/PROYECTO-DE-FUNBIO-1/assets/143019275/425fa802-36ec-4b63-9ba2-8e693385ba93)



##### Producto comercial 3
![image](https://github.com/Arianadextre/PROYECTO-DE-FUNBIO-1/assets/143019275/dfcdc133-b694-471e-979e-4a49fa23f5a2)




 
### Funcionales ¿Qué debe hacer mi diseño?
- [X] Conexión con aplicativo, el cuál brinda información detallada de la evaluación de la hinchazón de la macula del usuario.
- [X] Procesador óptico de ondas infrarrojas para emitir ondas que detectan las venas. 
- [X] Lectura y proyección de venas en tiempo real, aún cuando el paciente se mueve.

### No Funcionales ¿Qué propiedades debe poseer nuestro diseño?
- [X] Transporte eficaz.
- [X] Instrucciones detalladas.
- [X] Batería duradera.


### Esquema de funciones (caja negra)
![image](https://github.com/Arianadextre/PROYECTO-DE-FUNBIO-1/assets/143019275/99070b5d-82ae-4be7-a2ec-7c3aeed3dd05)




regular:regular la energia eléctrica que ingresa a los componentes
accionar:esta funcion genera la acción necesaria para activar el dispositivo 
identificar: el dispositivo identifica  la imagen que recibe
procesar: esta funcion procesa los datos del sistema
medir: esta funcion mide los datos recibidos
mostrar: se muestran   de los datos obtenidos




### Tabla de valoracion
![image](https://github.com/Arianadextre/PROYECTO-DE-FUNBIO-1/assets/143018597/d3a57860-8887-476c-b80a-a55a2533b200)


### Conclusion
La propuesta número 2 fue la ganadora ya que a pesar de poseer un costo de ensamblaje mayor a otras opciones, su facilidad de uso y la seguridad que brinda al paciente, la hacen una buena opción de desarrollo para tratar la retinopatía diabética. Además sus características la hacen útil tanto para el uso de un ciudadano común como el de personal médico, por su tamaño pequeño y ser integrable a un aparato cotidiano como serian los celulares, tendría un fácil acceso al almacenamiento de la información recolectada.


### ENTREGABLE 4

### Boceto 1

![image](https://github.com/Arianadextre/PROYECTO-DE-FUNBIO-1/assets/143019386/078b0acf-27ca-40da-8c2c-dd2581c3f2e9)

![image](https://github.com/Arianadextre/PROYECTO-DE-FUNBIO-1/assets/143019386/3ae03ce5-c91e-4345-9bbe-1f0ad6114797)

*Funcionamiento*: En este dispositivo, se necesitarán de dos personas: un especialista el cual usará el lente y el paciente.
A través de las cámaras OV7670, las cuales contienen un sensor CMO cada una, se registrarán imágenes a profundidad de los ojos, las que serán procesadas por el arduino UNO; y este se encargará a través de la la computadora (y su programación) de encender los leds cuando se detecte la anomalía presente. Finalmente, una vez sean capturadas dichas fotografías, estas aparecerán en la computadora en blanco y negro, y así puedan ser estudiadas por el especialista.

### Boceto 2

![image](https://github.com/Arianadextre/PROYECTO-DE-FUNBIO-1/assets/143019275/823eaded-2b41-442c-af7a-22d2944e5a90)


*Boceto en conjunto*:

![image](https://github.com/Arianadextre/PROYECTO-DE-FUNBIO-1/assets/143019275/4df5882b-7aaa-4cce-8b41-cef1caca746b)


*Descripción del funcionamiento*:

El casco que diseñamos tiene como función principal recopilar imágenes del fondo de ojo de un paciente con glaucoma. La luz influye profundamente en observar y capturar a detalle el fondo de ojo, por lo cual el casco contiene 4 leds en cada ojo para  mejorar la iluminación y contraer la pupila para obtener una mejor captura, además usaremos una rueda que moverá el sensor CMO en los ángulos más indispensables mientras las imágenes son grabadas  y enviadas por bluetooth gracias a la conexión con el arduino, en un aplicativo en el celular obtendremos las imágenes del ojo que serán enviadas a un oftalmólogo y guardadas en su historia clínica.

*Lista de despiece*:

![image](https://github.com/Arianadextre/PROYECTO-DE-FUNBIO-1/assets/143019275/83f4beb9-c4c4-409c-b44d-f521dee311a3)

### Boceto 3
![image](https://github.com/Arianadextre/PROYECTO-DE-FUNBIO-1/assets/143018747/2e858a24-b982-44a6-b098-b593a5eec689)
![image](https://github.com/Arianadextre/PROYECTO-DE-FUNBIO-1/assets/143018747/c8d363bd-d438-4e7e-a8f9-81585d93db25)
*Descripción del funcionamiento*:
Para este dispositivo, se colocará la parte llamada “pieza de plástico cuadrangular hueco” frente al ojo que se desea analizar, una vez colocado en dicha posición procede a activar el botón de activación (naturalmente ya debe estar encendido el dispositivo) para que realice una serie de fotografías desde ángulos ligeramente diferentes a través de los dos sensores CMOS, para que luego dichas tomas se guarden en la memoria SD adicionada al Arduino y se pueda enviar a un respectivo personal de la salud. Todo esto realizado por la misma persona a la que se le realiza la revisión, pues el dispositivo toma varias fotos de diferentes ángulos para que en alguna de ellas encuentre el fondo de ojo sin necesidad de estar rebuscando con ayuda de una segunda persona.
![image](https://github.com/Arianadextre/PROYECTO-DE-FUNBIO-1/assets/143018747/486dae51-86c5-4ada-bcf9-707c06099c42)

### Tablas de Valoración Técnica y Económica:
![image](https://github.com/Arianadextre/PROYECTO-DE-FUNBIO-1/assets/143018597/127434c1-d99d-497f-828d-6107e673ee37)
![image](https://github.com/Arianadextre/PROYECTO-DE-FUNBIO-1/assets/143018597/874368ba-2fde-48c6-9376-a44929f02c9a)
![image](https://github.com/Arianadextre/PROYECTO-DE-FUNBIO-1/assets/143018597/d81559c6-c2a6-4e9d-b98f-41f3c46a1c33)




### Profesores del curso

- Paulo Camilo Alberto Vela Anton
- Umbert Lewis de la Cruz Rodriguez
- Eder Juárez
- Jose Alonso Cáceres del Aguila


### Bibliografía
1-	Yovera-Aldana, M., Velásquez-Rimachi, V., Huerta-Rosario, A., More-Yupanqui, M. D., Osores-Flores, M., Espinoza, R., Gil-Olivares, F., Quispe-Nolazco, C., Quea-Vélez, F., Morán-Mariños, C., Pinedo-Torres, I., Alva-Diaz, C., & Pacheco-Barrios, K. (2021). Prevalence and incidence of Diabetic peripheral Neuropathy in Latin America and the Caribbean: a systematic review and meta-analysis. PLOS ONE, 16(5), e0251642. https://doi.org/10.1371/journal.pone.0251642

2-	 Invitado, A. (2019). Día Mundial de la Diabetes: tres hallazgos que debes conocer sobre América Latina. Gente Saludable. https://blogs.iadb.org/salud/es/diabetes-2/

3-	Villena, J. (2015). Diabetes mellitus in Peru. Annals of global health, 81(6), 765-775.
https://doi.org/10.1016/j.aogh.2015.12.018

4-	Medicamentos para el glaucoma | National Eye Institute. (s. f.). https://www.nei.nih.gov/espanol/Glaucoma/medicamentos-para-el-glaucoma#:~:text=El%20tratamiento%20m%C3%A1s%20com%C3%BAn%20para,pero%20pueden%20evitar%20que%20empeore.

5-Glaucoma | Prevención, diagnóstico y tratamiento | CUN. (s. f.). https://www.cun.es. https://www.cun.es/enfermedades-tratamientos/enfermedades/glaucoma#:~:text=Las%20pruebas%20que%20se%20realizan,es%20necesario%20dilatar%20el%20ojo.

7- https://pdfs.semanticscholar.org/a638/9e311efcce207c99dd3eaa796beaa2fa8620.pdf?_gl=1*1a2un1e*_ga*MTM4Njk0MzQ4LjE2OTUwNjc0MDQ.*_ga_H7P4ZT52H5*MTY5NTA2NzQwMy4xLjEuMTY5NTA2OTMxNC4xMy4wLjA.

8- https://www.semanticscholar.org/paper/Factores-de-riesgo-de-retinopatía-diabética-en-tipo-Espinoza-Sota/a98fc51581b49a5ccdd06d9fc6e059e348c82558

9- Dulanto S. EL 50 % DE LOS PACIENTES QUE TIENEN GLAUCOMA NO LO SABEN – Instituto Nacional de Oftalmología “Dr. Francisco Contreras Campos”" [Internet]. Gob.pe. [citado el 17 de octubre de 2023]. Disponible en: https://www.ino.gob.pe/pacientes-glaucoma-nolosaben/

10- Current applications of machine learning in the screening and diagnosis of glaucoma: a systematic review and Meta-analysis- PDF
(G5_GLAUCOMA_04.pdf)

11- Campos B, Cerrate A, Montjoy E, Dulanto GV, Gonzales C, Tecse A, et al. National survey on the prevalence and causes of blindness in Peru. Rev Panam Salud Publica [Internet]. 2014 [citado el 17 de octubre de 2023];36(5). Disponible en: https://pubmed.ncbi.nlm.nih.gov/25604097/

12- 	Vleming EN, Castro M, López-Molina MI, Teus MA. Estudio de prevalencia de retinopatía diabética en pacientes diabéticos mediante retinógrafo no midriático. Arch Soc Esp Oftalmol [Internet]. 2009 [citado el 19 de septiembre de 2023];84(5):231–6. Disponible en: https://scielo.isciii.es/scielo.php?pid=S0365-66912009000500003&script=sci_arttext
13 . Rodríguez, L., & Herbania, Y. (2008). Evaluación de los factores de riesgo en el glaucoma primario de ángulo abierto. Revista cubana de oftalmología, 21(1), 0–0. http://scielo.sld.cu/scielo.php?pid=S0864-21762008000100013&script=sci_arttext&tlng=pt

14- Jürgens, I. (2013, noviembre 28). Glaucoma. ICR; Institut Català de Retina. https://icrcat.com/enfermedades-oculares/glaucoma/



