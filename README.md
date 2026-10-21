\[!\[Open in MATLAB Online]

# Práctica 5.4: Modelado y control del sistema cardiovascular mediante el modelo Windkessel

## Información de la estudiante

Nombres y Apellidos \[No. Control]; correo institucional

Modelado de Sistemas Fisiológicos

Ingeniería Biomédica

## Docente

Dr. Paul Antonio Valle Trujillo; paul.valle@tectijuana.edu.mx

Departamento de Ingeniería Eléctrica y Electrónica, Tecnológico Nacional de México/IT Tijuana, Blvd. Alberto Limón Padilla s/n, Tijuana, C.P. 22454, B.C., México.

## Descripción de la asignatura

El modelizado de sistemas fisiológicos es una herramienta importante en Ingeniería Biomédica, permite comprender el funcionamiento del cuerpo humano, así como diseñar y evaluar terapias y dispositivos médicos; se define como el proceso de formular modelos matemáticos o computacionales que representan el comportamiento y la interacción de los sistemas biológicos y fisiológicos. Esta asignatura pretende aportar al perfil del Ingeniero Biomédico la capacidad de realizar investigación científica en el área de Biología de Sistemas con la finalidad de dirigir y participar en equipos de trabajo interdisciplinarios en contextos nacionales e internacionales, así como de proporcionar soluciones informáticas para resolver problemas en el campo de la Ingeniería Biomédica con ética profesional; lo anterior al proporcionar al estudiante bases sólidas para modelizar sistemas y diseñar controladores para la solución de problemas en las áreas de atención médica y del sector industrial médico. La construcción de analogías entre circuitos eléctricos y sistemas fisiológicos para la formulación de modelos matemáticos y el diseño de controladores mediante la experimentación in silico brindan herramientas de gran aplicación en el quehacer profesional del Ingeniero Biomédico.

La asignatura de Modelado de Sistemas Fisiológicos forma parte del plan de estudios de la carrera en Ingeniería Biomédica con la siguiente competencia general del curso: Utiliza analogías entre circuitos eléctricos, ecuaciones diferenciales ordinarias y sistemas fisiológicos para describir su dinámica, obtener modelos matemáticos y aplicar el control clásico, esto con el objetivo de integrar los principios de la Ingeniería de Control, la Electrónica Analógica y las Ciencias de la Computación con la Anatomía y Fisiología del cuerpo humano para proporcionar descripciones cuantitativas y cualitativas de sistemas fisiológicos complejos con el objetivo de modelizar, analizar, controlar, ilustrar y predecir su dinámica tanto en el corto como en el largo plazo.

## Objetivos

1. Identificar los elementos fisiológicos y eléctricos equivalentes del modelo Windkessel: flujo sanguíneo, resistencia vascular, distensibilidad arterial y presión arterial.
2. Formular la ecuación diferencial ordinaria que describe la dinámica de la presión arterial a partir del balance de flujo.
3. Obtener y analizar la función de transferencia del modelo Windkessel como representación complementaria de la ecuación diferencial ordinaria.
4. Analizar la estabilidad del sistema y determinar el error en estado estacionario para las entradas consideradas.
5. Simular la respuesta del sistema cardiovascular en Simulink/MATLAB ante cambios en el flujo de entrada y en los parámetros de resistencia y distensibilidad.
6. Diseñar y sintonizar un controlador PID para regular la presión arterial y reducir el error entre la presión de referencia y la presión medida.
7. Comparar la respuesta en lazo abierto y en lazo cerrado, considerando el transitorio, el tiempo de establecimiento, el sobreimpulso y el error en estado estacionario.
8. Implementar en Spyder/Python la solución numérica de la ecuación diferencial ordinaria y la simulación del controlador para validar los resultados obtenidos en Simulink/MATLAB.

## Descripción detallada del sistema

En esta práctica se modela el sistema cardiovascular mediante el modelo Windkessel, una analogía eléctrica de la circulación arterial. La resistencia vascular representa la oposición al flujo sanguíneo y la distensibilidad arterial representa la capacidad de las arterias para almacenar volumen, de forma análoga a un capacitor. La presión arterial se obtiene a partir del balance entre el flujo de entrada del corazón, el flujo de salida hacia la circulación periférica y el almacenamiento de volumen en el compartimento arterial.

La diferencia principal respecto a la práctica anterior es que la dinámica del sistema se formula directamente mediante ecuaciones diferenciales ordinarias (EDO), en lugar de partir únicamente de un circuito RLC y su función de transferencia. Para el modelo Windkessel de dos elementos, la ecuación de balance es

\[
C\frac{dP(t)}{dt}=Q_{in}(t)-\frac{P(t)}{R},
\]

donde \(P(t)\) es la presión arterial, \(Q_{in}(t)\) es el flujo sanguíneo de entrada, \(R\) es la resistencia vascular periférica y \(C\) es la distensibilidad arterial. Al despejar la derivada se obtiene la EDO en forma explícita:

\[
\frac{dP(t)}{dt}=\frac{1}{C}\left(Q_{in}(t)-\frac{P(t)}{R}\right).
\]

Esta ecuación permite calcular la evolución temporal de la presión a partir de una condición inicial y de una entrada de flujo. La constante de tiempo del sistema es \(\tau=RC\), por lo que un aumento de la resistencia o de la distensibilidad hace más lenta la respuesta. Para el modelo Windkessel de tres elementos puede incorporarse una resistencia característica \(R_c\), con \(P_a(t)=R_cQ_{in}(t)+P_c(t)\) y \(C\,dP_c(t)/dt=Q_{in}(t)-P_c(t)/R\). La función de transferencia se utiliza como representación equivalente para el análisis de control, mientras que la EDO conserva de manera explícita la variable de estado y facilita la simulación de entradas fisiológicas variables.

Palabras clave: Modelo Windkessel; Sistema cardiovascular; Presión arterial; Flujo sanguíneo; Ecuaciones diferenciales ordinarias; Controlador PID; Simulaciones numéricas.

## Lista de archivos incluidos en el repositorio

1. Cuaderno computacional de MATLAB \[.mlx].
2. Modelo de Simulink del sistema cardiovascular y del controlador \[.slx].
3. Archivos de Spyder/Python para resolver la ecuación diferencial ordinaria \[.py].
4. Imagen con los parámetros del modelo Windkessel y del controlador.
5. Imágenes de las simulaciones de presión y flujo \[.pdf y .png].
6. Análisis matemático: analogía Windkessel, ecuación diferencial ordinaria, función de transferencia, estabilidad, constante de tiempo y error en estado estacionario.

## Referencias

\[1] P. A. Valle, Syllabus para Modelado de Sistemas Fisiológicos, Tecnológico Nacional de México / Instituto Tecnológico de Tijuana, Tijuana, B.C., México, 2025. Permalink: https://biomath.xyz/course/

\[2] M. C. Khoo, Physiological Control Systems Analysis Simulation, and Estimation, 2nd ed. Piscataway, New Jersey, USA: IEEE Press, 2018, Section 4, Page 93.

\[3] N. S. Nise, Control Systems Engineering, 8th ed. Hoboken, New Jersey, USA: John Wiley \& Sons, 2020.

