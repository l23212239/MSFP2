\[!\[Open in MATLAB Online]

# Práctica 5.4: Modelado y control del sistema cardiovascular mediante el modelo Windkessel

## Información de la estudiante

Gabriel Fernando Trejo Paz \ 23212239; L23212239@tectijuana.edu.mx

Modelado de Sistemas Fisiológicos

Ingeniería Biomédica

## Docente

Dr. Paul Antonio Valle Trujillo; paul.valle@tectijuana.edu.mx

Departamento de Ingeniería Eléctrica y Electrónica, Tecnológico Nacional de México/IT Tijuana, Blvd. Alberto Limón Padilla s/n, Tijuana, C.P. 22454, B.C., México.

## Descripción de la asignatura

El modelizado de sistemas fisiológicos es una herramienta importante en Ingeniería Biomédica, permite comprender el funcionamiento del cuerpo humano, así como diseñar y evaluar terapias y dispositivos médicos; se define como el proceso de formular modelos matemáticos o computacionales que representan el comportamiento y la interacción de los sistemas biológicos y fisiológicos. Esta asignatura pretende aportar al perfil del Ingeniero Biomédico la capacidad de realizar investigación científica en el área de Biología de Sistemas con la finalidad de dirigir y participar en equipos de trabajo interdisciplinarios en contextos nacionales e internacionales, así como de proporcionar soluciones informáticas para resolver problemas en el campo de la Ingeniería Biomédica con ética profesional; lo anterior al proporcionar al estudiante bases sólidas para modelizar sistemas y diseñar controladores para la solución de problemas en las áreas de atención médica y del sector industrial médico. La construcción de analogías entre circuitos eléctricos y sistemas fisiológicos para la formulación de modelos matemáticos y el diseño de controladores mediante la experimentación in silico brindan herramientas de gran aplicación en el quehacer profesional del Ingeniero Biomédico.

La asignatura de Modelado de Sistemas Fisiológicos forma parte del plan de estudios de la carrera en Ingeniería Biomédica con la siguiente competencia general del curso: Utiliza analogías entre circuitos eléctricos, ecuaciones diferenciales ordinarias y sistemas fisiológicos para describir su dinámica, obtener modelos matemáticos y aplicar el control clásico, esto con el objetivo de integrar los principios de la Ingeniería de Control, la Electrónica Analógica y las Ciencias de la Computación con la Anatomía y Fisiología del cuerpo humano para proporcionar descripciones cuantitativas y cualitativas de sistemas fisiológicos complejos con el objetivo de modelizar, analizar, controlar, ilustrar y predecir su dinámica tanto en el corto como en el largo plazo.

## Objetivos

1. Calcular la función de transferencia.
2. Determinar el modelo de ecuaciones integro-diferenciales.
3. Analizar la estabilidad del sistema.
4. Determinar el error en estado estacionario.
5. Identificar los elementos fisiológicos y eléctricos equivalentes del modelo Windkessel.
5. Emular la respuesta del sistema cardiovascular en Simulink/Simscape para tres casos: normotenso, hipotenso, hipertenso.
6. Sintonizar las ganancias de dos controladores PID para los casos hipotenso e hipertenso, en Simulink/MATLAB para eliminar el error entre la entrada y la salida del sistema.
7. Simular la respuesta del sistema en lazo abierto y lazo cerrado en Simulink/MATLAB para los casos hipotenso e hipertenso.
8. Implementar en Python las comparativas de control para los casos hipotenso e hipertenso, y analizar la respuesta en lazo abierto de los estados normotenso, hipotenso e hipertenso.
9. Diseñar un diagrama biológico mediante BioRender equivalente a un diagrama del sistema cardiovascular y su relación con el circuito eléctrico de cuatro elementos.

## Descripción detallada del sistema

En esta práctica se modela el sistema cardiovascular mediante el modelo Windkessel de cuatro elementos, una analogía eléctrica del sistema cardiovascular. La resistencia periférica representa la oposición al flujo sanguíneo y la distensibilidad arterial representa la capacidad de las arterias para almacenar volumen, de forma análoga a un capacitor. La presión arterial se obtiene a partir del balance entre el flujo de entrada del corazón, el flujo de salida hacia la circulación periférica y el almacenamiento de volumen en el compartimento arterial.

Una diferencia respecto a la práctica anterior es que la dinámica del sistema se formula también mediante ecuaciones diferenciales ordinarias (EDO), en lugar de partir únicamente de un circuito RLC y su función de transferencia. La función de transferencia se utiliza como representación equivalente para el análisis de control, mientras que las EDOs relacionan el flujo de entrada con el almacenamiento y la salida del sistema.

Palabras clave: Modelo Windkessel; Sistema cardiovascular; Presión arterial; Flujo sanguíneo; Ecuaciones diferenciales ordinarias; Controlador PID; Simulaciones numéricas.

## Lista de archivos incluidos en el repositorio

1. Cuaderno computacional de MATLAB [.mlx].
2. Análisis matemático Función de transferencia, modelo de ecuaciones integro-diferenciales, estabilidad y error en estado estacionario.
3. Diagrama biológico desarrollado en BioRender.
4. Modelo de Simulink [ .slx].
5. Código fuente desarrollado en Python [ .py].
6. Imagen con los parámetros del controlador.
7. Imágenes de las simulaciones [.pdf y .png].
8. Archivo signal [ .xlsx].
## Referencias

\[1] P. A. Valle, Syllabus para Modelado de Sistemas Fisiológicos, Tecnológico Nacional de México / Instituto Tecnológico de Tijuana, Tijuana, B.C., México, 2025. Permalink: https://biomath.xyz/course/

\[2] M. C. Khoo, Physiological Control Systems Analysis Simulation, and Estimation, 2nd ed. Piscataway, New Jersey, USA: IEEE Press, 2018, Section 4, Page 93.

\[3] N. S. Nise, Control Systems Engineering, 8th ed. Hoboken, New Jersey, USA: John Wiley \& Sons, 2020.

