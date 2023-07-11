## **Proyecto Individual 02 - Data Analyst**

![Cobertura_01|=250x](/Src/cobertura%20internet_02.jpg)


### Contexto

Nos encontramos en un momento de la humanidad donde las telecomunicaciones se han vuelto una parte esencial de nuestro estilo de vida, facilitando el acceso a la información y permitiendo la comunicación entre personas quitando todos los obstáculos de distancia lo que nos permite ahora en pensar en trabajar de forma remota para empresas en otros países.
La transferencia de los datos se realiza en su mayoría a través de internet mediante líneas telefónicas fijas, fibra óptica y telefonía móvil, los cuales se encuentran en casi todo el mundo,  según los últimos datos generados por el Ente de Comunicaciones de Argentina ENACOM llega a los [10.378.022](http://datosabiertos.enacom.gob.ar/dataviews/240976/total-nacional-de-accesos-a-internet-fijo-por-banda-ancha-y-banda-angosta/) de usuarios activos para el segundo trimestre del 2022.

### Propuesta de Telecomunicaciones

Una empresa proveedora de servicios de telecomunicaciones pidió a la empresa en la que trabajo que realizara un análisis en profundidad para reconocer el comportamiento del sector a nivel nacional en este contexto. Además de proporcionar acceso a **Internet**, la empresa también ofrece otros **servicios**, que son importantes para tener en cuenta, posterior a este estudio.

---

### Fuente de datos

Este proyecto pretende tomar los dataset de la pagina del [ENACOM](https://datosabiertos.enacom.gob.ar/dashboards/20000/acceso-a-internet/) y hacer un analisis en profundidad de los datos sobre el acceso a internet en la Republica Argentina, con el fin de preoponer ciertos KPI's, entre las propuestas se encuentra aumentar el numero de hogares cada 100 con acceso a internet en un 3%. Para esto se tendran que seguir una serie de pasos, los cuales son ETL, para la limpieza de los datasets a utilizar y el EDA, en el cual se buscaran relaciones entre los datos, outliers y datos anormales.

---
# ETL
A fin de trabajar con los datasets provistos por ENACOM es necesario hacer una limpieza y tranzformacion de los mismos, ya que en estos podemos encontrar algunos errores de formato.

 - La escritura de - 0, en vez del valor cero para registros que no tuvieran información.

 - En los errores de formatos de los datasets, hay que destacar dos de los mas frecuentes, todos los numeros superiores al millon, estan precentes como type objet, ya que estan precentados tal que por ejemplo

- Problemas con los datos numericos: "1.000.000" no siendo un "int", a su vez, todo numero entre mil hasta un millon no incluido esta precentado en forma de flotante tal que por ejemplo docemil quinientos termina siendo doce punto cinco

- Datos erroneos:
En el dataset de Internet_penetracion podemos encontrar en "acceso cada 100 hogares" un error en los datos de capital federal, siendo que estos superan los 100 hogares cada 100 hogares.
---
# EDA

En un analisis exploratorio se pudieron ver relaciones o patrones que se repetían en cada uno de los datsets.

- Por ejemplo: crecimiento de la velocidad media de bajada por trimestre, el año que marco la diferencia fue el 2019, en el segundo trimestre se da un aumento significativo:

![grafica_01](/Src/grafica_01.png)

- Con respecto a las tecnologias, podemos relacionar el crecimiento de cablemodem y fibra optica con el crecimiento de la velocidad media de bajada

![07](/Src/grafica_07.png)



- En los usuarios de Dial up encontramos dos grandes valles en el grafico, que pueden deberse a errores en los datos, teniendo en cuenta que la cantidad de estos es marginal, no tendremos en cuenta estos datos:

![03](/Src/grafica_03.png)


- Aqui podemos ver como los usuarios de banda ancha aumentan rapidamente cada trimestres:

![02](/Src/grafica_02.png)

- Pero de la misma manera podemos observar que los usuarios de +1 Mbps a 6 Mbps disminuyen, lo que nos muestra que cambián de velocidad pero no aumentan las conexiones.

![06](/Src/grafica_06.png)

- Por otro lado también se puede hacer una analisis exploratorio de como se comportan cada una de las provincias que conforman Argentina, cuales serían los totales en Acceso y la velocidad que escogen:

![04](/Src/grafica_04.png)

![05](/Src/grafica_05.png)


---

### Declaración de Objetivos

* Desarrollar un programa que le permita a la empresa brindar un acceso de mayor velocidad pero dirigido a las provincias que en estos instantes presentan buenos accesos como lo pueden ser Cordoba, Santa fe, Tucuman y Entre Rios.

* Crear un índice de medición que permita establecer los costos para ofrecer mejores velocidades a mejores precios que permita le llegada de nuevos suscriptores.

* Si no es posible dar conexión fija, ver la manera de adaptar las antenas de telecomunicación para ofrecer mejores velocidades a través de las comunicaciones moviles.

---

### Conclusiones

* Argentina, en comparación con la región, está rezagada en el acceso a internet fijo aunque tienes buenas cifras en acceso a internet.

* A la fecha Argentina se encuentra en el puesto 10 de [velocidades de banda ancha](https://dplnews.com/velocidades-de-banda-ancha-fija-en-america-latina-y-el-mundo-septiembre-2022/) se debe trabajar en mejorar tanto la velocidad como la tecnología.

* Se observaron inconvenientes en la continuidad del desarrollo de forma sostenida entre cambios de gobiernos.
