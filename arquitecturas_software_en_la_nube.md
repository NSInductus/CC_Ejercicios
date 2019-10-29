# Ejercicio 1

**Buscar una aplicación de ejemplo, preferiblemente propia, y deducir qué patrón es el que usa. ¿Qué habría que hacer para evolucionar a un patrón tipo microservicios?**

Se ha seleccionado como aplicación de ejemplo la que yo creé durante mi TFG, la aplicación se puede encontrar en el siguiente repositorio de github: [repositorio_TFG](https://github.com/NSInductus/TFG_V_0.0). La principal funcionalidad de esta aplicación es analizar las emociones de personas en vídeos. La aplicación está realizada completamente en Java y tiene una arquitectura de microkernel.

Para poder evolucionar a un patrón de microservicios deberíamos separar la aplicación en pequeñas aplicaciones cada una dedicada a realizar un conjunto de funciones comunes, que serían los diferentes microservicios, en mi caso particular se debería de separar en: microservicio de fragmentación de vídeo, microservicio de análisis facial, microservicio de resultados y microservicio de creación de gráficas.

después tendríamos que desplegar cada uno de los microservicios en la nube y ya tendríamos mi aplicación desarrollada durante el TFG con un patrón tipo microservicios.

# Ejercicio 2

**En la aplicación que se ha usado como ejemplo en el ejercicio anterior, ¿podría usar diferentes lenguajes? ¿Qué almacenes de datos serían los más convenientes?**

Si se podrían utilizar en diferentes lenguajes de programación, es más en su día se vio que el uso de la API de reconocimiento facial que utiliza mi aplicación sería más sencillo si se utiliza python en lugar de Java. También creo que para la segmentación del vídeo en múltiples fotogramas se podría utilizar la biblioteca openCV en cualquiera de los lenguajes donde se pueda.

Esta aplicación no utiliza ninguna base de datos, en lugar de esto la aplicación grava los resultados en formato txt, pero si se diera la posibilidad de almacenar los resultados en la nube creo que los almacenes de datos más convenientes serían los SQL puesto que todos los datos almaenados tienen la misma estructura.
