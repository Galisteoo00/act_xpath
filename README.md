1.	Nombre de la Universidad
/universidad/nombre
 
![1](https://user-images.githubusercontent.com/115107104/232501928-980ac6ae-8d85-4f9c-962b-4aa4a4b9a8b8.png)


2. País de la Universidad
/universidad/pais
 ![2](https://user-images.githubusercontent.com/115107104/232501955-235983cf-e88f-431b-8175-62155f45e272.png)


3. Nombres de las Carreras
//carrera/nombre
![3](https://user-images.githubusercontent.com/115107104/232502010-ef5c76b0-0536-42b5-804e-f7e2ee077934.png)

 

4. Años de plan de estudio de las carreras
//carrera/plan
 ![4](https://user-images.githubusercontent.com/115107104/232502033-f6a19d29-b961-4f48-8854-f0f696ce845f.png)

5. Nombres de todos los alumnos
//alumno/nombre
 ![5](https://user-images.githubusercontent.com/115107104/232502077-ece2d8af-6258-4117-af8f-734c7fade870.png)


6. Identificadores de todas las carreras
//carrera/@id
 ![6](https://user-images.githubusercontent.com/115107104/232502096-b4358452-bb27-4289-b357-895ea0fa28b0.png)

7. Datos de la carrera cuyo id es c01
//carrera[@id='c01']
 ![7](https://user-images.githubusercontent.com/115107104/232502137-9a48c4fd-87ce-4290-aa8a-d2c73075c6f3.png)


8. Centro en que se estudia de la carrera cuyo id es c02
//carrera[@id='c02']/centro
 ![8](https://user-images.githubusercontent.com/115107104/232502170-c4b9ed7b-b3d7-426e-bc5f-8421d30b9971.png)

9. Nombre de las carreras que tengan subdirector
//subdirector/../nombre
![9](https://user-images.githubusercontent.com/115107104/232502197-97bd044b-15b4-461d-af37-39e4e8c06cb6.png)

10.Nombre de los alumnos que están haciendo proyecto
//alumno//proyecto/../../nombre
![image](https://user-images.githubusercontent.com/115107104/232502819-e3cb3d99-1e12-4378-95fe-6fd0aeb416d6.png)

11.Códigos de las carreras en las que hay algún alumno matriculado
//alumno//carrera/@codigo
![image](https://user-images.githubusercontent.com/115107104/232503000-d21e3728-4234-465a-bb4f-fb363e0fa272.png)

12.Apellidos y Nombre de los alumnos con beca
//alumno[@beca]/concat(nombre,' ',apellido1,',',apellido2)
![image](https://user-images.githubusercontent.com/115107104/232505076-72b18c9d-1991-4a36-a57c-9ee862cb18c4.png)

13.Nombre de las asignaturas de la titulación c04
//asignatura[@titulacion='c04']/nombre
![image](https://user-images.githubusercontent.com/115107104/232505304-f461b863-3d8f-4a78-a879-adfdc7a902ca.png)

14.Nombre de las asignaturas de segundo trimestre
//asignatura[trimestre=2]/nombre
![image](https://user-images.githubusercontent.com/115107104/232505411-ba0f4abc-04f0-40c9-8714-efdc0784eeca.png)

15.Nombre de las asignaturas que no tienen 4 créditos teóricos
//asignatura[not(creditos_teoricos=4)]/nombre
![image](https://user-images.githubusercontent.com/115107104/232505565-80644480-58bb-4638-aa56-cb8ee6db437f.png)

16.Código de la carrera que estudia el último alumno
//alumno[last()]//carrera/@codigo
![image](https://user-images.githubusercontent.com/115107104/232505787-74a94a65-7fde-4680-983f-fa616273f553.png)

17.Código de las asignaturas que estudian mujeres
//alumno[sexo='Mujer']//asignatura/@codigo
![image](https://user-images.githubusercontent.com/115107104/232506907-21308565-343d-4b49-8a84-968463625392.png)

18.Nombre de los alumnos que matriculados en la asignatura a02:
//alumno[.//asignatura/@codigo='a02']/nombre
![image](https://user-images.githubusercontent.com/115107104/232507043-000924cd-53be-4b8f-8d61-4a190d3c2b36.png)

19.Códigos de las carreras que estudian los alumnos matriculados en alguna asignatura
//alumno//asignatura/../../carrera/@codigo
![image](https://user-images.githubusercontent.com/115107104/232507165-c6417024-6cfd-4b6e-962f-c771ec9fb6da.png)

20.Apellidos de todos los hombres
doc("universidad.xml")//alumno[sexo='Hombre']/apellido1 | doc("universidad.xml")//alumno[sexo='Hombre']/apellido2
![image](https://user-images.githubusercontent.com/115107104/232508298-65c068ac-1244-4c65-834e-65105097c2f5.png)

21.Nombre de la carrera que estudia Víctor Manuel:
//carrera[@id=//alumno[nombre='Víctor Manuel']//carrera/@codigo]/nombre
![image](https://user-images.githubusercontent.com/115107104/232508613-81932582-ddca-4edc-844b-dc59c1345ffd.png)

22.Nombre de las asignaturas que estudia Luisa
//asignatura[@id=//alumno[nombre='Luisa']//asignatura/@codigo]/nombre
![image](https://user-images.githubusercontent.com/115107104/232508764-33c6b5d7-c8c7-4f0a-a9c8-e7b0fcd4d5b7.png)

23.Primer apellido de los alumnos matriculados en Ingeniería del Software
//alumno[.//asignatura/@codigo=//asignatura[nombre='Ingeniería del Software']/@id]/apellido1
![image](https://user-images.githubusercontent.com/115107104/232508921-0ae99ea4-749b-4ddd-8938-cd15d0ebcef8.png)

24.Nombre de las carreras que estudian los alumnos matriculados en la asignatura Tecnología de los Alimentos:
//carrera[@id=//alumno[.//asignatura[@codigo=//asignatura[nombre='Tecnología de los Alimentos']/@id]]//carrera/@codigo]/nombre
![image](https://user-images.githubusercontent.com/115107104/232509128-c7c73c86-a8e9-4ffe-b660-53d8a6a3ba7d.png)

25.Nombre de los alumnos matriculados en carreras que no tienen subdirector
//alumno[not (.//carrera/@codigo=//carrera[subdirector]/@codigo)]/nombre
![image](https://user-images.githubusercontent.com/115107104/232509343-7eb0f634-2d66-49aa-9882-9652a074a5ff.png)
  
26.Nombre de las alumnos matriculados en asignaturas con 0 créditosprácticos y que estudien la carrera de I.T. Informática
//alumno[.//asignatura/@codigo=//asignatura[creditos_practicos=0]/@id][.//carrera/@codigo=//carrera[nombre='I.T. Informática']/@id]/nombre
![image](https://user-images.githubusercontent.com/115107104/232509519-31d3a6cc-65c0-4ef5-9890-7c85cb27046b.png)

27.Nombre de los alumnos que estudian carreras cuyos planes sonanteriores a 2002:
//alumno[.//carrera/@codigo=//carrera[not(plan>=2002)]/@id]/nombre
![image](https://user-images.githubusercontent.com/115107104/232509678-aa5621ba-7c00-4b1a-8526-e63b1ee4c64d.png)
