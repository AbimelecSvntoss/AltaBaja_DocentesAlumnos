Título: Aplicación de consola VB.NET para gestión CRUD de Docente y Alumno con persistencia en texto plano.
Descripción Proyecto de ejemplo en VB.NET (aplicación de consola) que implementa un CLI para administrar entidades Persona → Docente / Alumno. Persistencia por línea en archivos docentes.txt y alumnos.txt, parseo delimitado por ", ".

Tecnología
•	Lenguaje: VB.NET (Framework/.NET compatible con Visual Studio)
•	Persistencia: archivos de texto plano

Estructura principal
•	Program.vb — menú CLI y orquestación CRUD
•	Persona.vb — clase base (propiedades y ToString())
•	Docente.vb — hereda Persona, atributos Especialidad, Materia
•	Alumno.vb — hereda Persona, atributos Especialidad, Matricula
•	Archivos.vb — funciones GuardarDocentes, ImportarDocentes, GuardarAlumnos, ImportarAlumnos

Formato de datos (ejemplo de línea) ID: 1, Nombre: Juan, Apellidos: Pérez, Teléfono: 123456789, Especialidad: Ingeniería, Matrícula: 2021001

Instrucciones de compilación y ejecución
1.	Abrir la solución/proyecto en Visual Studio.
2.	Compilar (Build → Build Solution).
3.	Ejecutar (Start/Debug o ejecutar el .exe en la carpeta bin\Debug).
4.	Colocar docentes.txt y/o alumnos.txt en el directorio de ejecución si se desea precargar datos.

Limitaciones y recomendaciones técnicas
•	Parsing frágil: depende del formato exacto ", "; no maneja comas internas.
•	Sin validación robusta ni manejo avanzado de excepciones.
•	Recomendación: migrar a JSON/CSV o base de datos para escalabilidad y robustez; extraer y probar el parsing en funciones unitarias.

Sugerencias para próximas mejoras
•	Validación y manejo de errores en entrada y E/S.
•	Soporte para formatos estructurados (JSON).
•	Unit tests para parsing y Archivos.vb.

Mensajes de commit sugeridos
•	feat: agregar estructura de modelos Persona, Docente, Alumno y CLI inicial
•	feat: implementar persistencia docente en Archivos.vb
•	feat: implementar GuardarAlumnos / ImportarAlumnos
•	fix: corregir carga de alumnos (nombre de archivo) y llamadas a Archivos
•	refactor: extraer lógica de parseo en Archivos.vb
•	docs: agregar README técnico con formato de datos y recomendaciones
