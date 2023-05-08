---
marp: true
theme: gaia
class:
title: UA
author: Joan Cano
# paginate: true
# header: 'Header content'
footer: '![image w:50px](../../assets/liberam/simbolo_white.png)'

---
<!-- _backgroundColor: #1962a7ff -->
<!-- _color: #fff -->
<style>
  img[alt~='center'] {
    display: block;
    margin-left: auto;
    margin-right: auto;
  }
</style>

# Técnicas de documentación geométrica
El uso de drones para la generación de modelos digitales del terreno

10 y 24 de marzo

###### Joan Cano / [Liberam](https://liberam.es)

![bg right:35% 90%](../../assets/portada_charla.jpg)

----
<!-- backgroundColor: white -->
<!--_paginate: true -->
<!-- _class: lead -->

## > whoami

###### Joan Cano
<p style="color: grey; font-size: 0.8em;">Geógrafo especializado en GIS, Teledetección, láser escáner, fotogrametría y UAV</p>

![bg left:40% 60%](../assets/foto_perfil.png)

---

<!-- _class: lead -->

![bg left:33% 100%](../assets/liberam/liberam_name_blue_black.png)
<iframe src="https://liberam.es" style="height:600px;"></iframe>

---
#  Objetivos

- Conocer los principales tipos de drones y cámaras
- Conocer los principios básicos de la fotogrametría
- Flujos de trabajo / postproceso
- Tratamiento de la información espacial
- Software de procesamiento fotogramétrico

---
<!-- _class: lead -->

# ¿De qué vamos a hablar?

<iframe src="indice.html" style="height:600px;"></iframe>

---
<!-- _class: invert -->
# MDT
![bg](../assets/img_presentacion/quarry.png)

---
# Modelos Digitales del Terreno (MDT)

Estructura numérica de datos que representa la distribución espacial de una propiedad de la superficie de terreno (de una variable cuantitativa y continua). Es un concepto genérico.

#### Modelo Digital de Elevaciones (MDE)
Estructura numérica de datos que representa la distribución espacial de la altitud de la superficie de terreno. Un MDE es un caso particular dentro de los **MDT**.

---
# Drones
![bg contain](../assets/img_presentacion/ebeeX.png)

---
# Drones
Los UAV portan sensores que se encargan de capturar datos
- Imágenes (RGB, multiespectrales, térmicas)
- Nubes de puntos
- Radiancia / Reflectividad
- etc.

--- 
# Fotogrametría
![bg right:800](../assets/img_presentacion/img_fotogrametria3.gif)

---
## De sensores digitales a información espacial

Transformación de imágenes tomadas a mano, por drones o con avioneta en mapas 2D precisos y georreferenciados, modelos 3D, nubes de puntos y análisis.

![bg vertical w:450](../assets/img_presentacion/img_fotogrametria.jpg)
![bg right w:550](../assets/img_presentacion/img_fotogrametria2.jpg)

---
<!-- _backgroundColor: #1962a7ff -->
<!-- _color: #fff -->
# Flujo de trabajo escalable

![bg right w:800](../assets/img_presentacion/flujoEscalable.png)

1. Imágenes o video
2. Procesamiento y creación 2D y modelos 3D
3. Análisis y digitalización
4. Compartir modelos & Colaboración

---
# Inputs
![center w:1200](../assets/img_presentacion/types_cameras.png)

---
# Outputs
![center w:1200](../assets/img_presentacion/outputs.png)

---
#### Aplicaciones y sectores: **Topografía & Construcción**

- Gestión de movimiento de tierras
- Levantamientos topográficos
- Mediciones de acopio y corte/relleno
- Monitoreo/inspección visual durante la construcción
- Seguimiento del progreso
- Documentación de proyectos para visualización, medición, anotación y uso compartido
- Inspecciones de edificios e infraestructuras
- Planificación de perforaciones y voladuras
- Mapeo base para el diseño del sitio
- Comparación entre lo construido y lo diseñado

---
#### Aplicaciones y sectores: **Topografía & Construcción**

- Puentes
- Carreteras
- Túneles
- Torres de transmisión
- Torres de telefonía móvil
- Edificios
- Puertos y dársenas
- Aeropuertos

---
#### Aplicaciones y sectores: **Patrimonio cultural**

- Conservación y gestión activa
- Mapas y modelos 3D detallados y precisos
- Descubrimientos
- Experiencias inmersivas en VR & AR y web
- Restauración

---
#### Aplicaciones y sectores: **Agricultura**

- Identificación temprana de problemas
- Comprensión más profunda de su cultivo
  - Mapas de índices ligados a las características de la planta
- Aumentar la producción / rendimiento de cultivos
- Ahorro de insumos
- Estimaciones de rendimiento más precisas
- Planificación y gestión del riego
- Minimizar la erosión del suelo

---
#### Aplicaciones y sectores: **Seguridad Pública**

- Medicina forense y reconstrucción de escenas
- Reducción del tiempo en la escena
- Documentación siempre disponible en el tiempo
- Investigación de incendios
- Análisis de causa
- Evaluación de daños
- Ajustes de reclamaciones de seguros
- Búsqueda y Rescate (SAR)
- Búsqueda de personas desaparecidas
- Conciencia situacional rápida para los primeros respondedores

---
#### Aplicaciones y sectores: **Ayuda humanitaria y gestión de desastres**

- Coordinación de equipos de socorro de emergencia y recuperación
- Proporcionar conocimiento de la situación sobre el terreno a los equipos
- Compartir y difundir información en línea o fuera de línea
- Reducción de riesgos y desastres
- Identificar casas, refugios, carreteras, puentes u otros daños en infraestructuras criticas

---
# Profundicemos: **Fotogrametría** <!--fit -->
- Ciencia que permite realizar mediciones
- Se necesitan imágenes principalmente
- Los resultados primarios incluyen mediciones y representaciones 2D y 3D
- Creación de activos digitales de muy alta calidad
- Tecnología democrática

---

## **De imágenes a puntos 3D**

Si:
- Podemos identificar lo mismo en **al menos dos imágenes**
- Conocemos los parámetros **externos e internos** de una cámara

Podremos:
- Calcular la posición de un punto en el espacio 3D
![bg right:40% 100%](../assets/img_presentacion/stereoscopy_2.png)

---
## **De imágenes a puntos 3D**

- En este ejemplo, la posición de un solo punto en el espacio 3D se calcula con mayor precisión, principalmente porque se han tenido en cuenta más imágenes

![bg right:40% 100%](../assets/img_presentacion/stereoscopy_3.png)

---
## Principios: **Estereoscopía**

La visión estereoscópica se obtiene mediante la **observación de un punto**, fotografiado **desde dos puntos de vista diferentes**, y donde los puntos homólogos se intersecan, consiguiendo así una visión en 3 dimensiones.

![bg right:40% 90%](../assets/img_presentacion/stereoscopy.png)

---
## Principios: **Paralaje**

Cambio aparente de posición de un objeto debido a un cambio de posición del observador.

En fotogrametría se consigue mediante cambios en la posición de la cámara al realizar fotografías.

![bg left:40% 100%](../assets/img_presentacion/Parallax_art.svg)

---

## **Parámetros externos e internos**

- Los **parámetros externos** de una cámara definen la **posición** y la **orientación** de la cámara
- Los **parámetros internos** de una cámara definen las **geometrías del objetivo** y del **sensor de la cámara**

---
<!-- _class: lead -->
# Captura de imágenes con dron
![bg right:60% 150%](../assets/img_presentacion/flight_missions.svg)

---

### **Solape** Longitudinal / Transversal

- Recubrimiento entre las pasadas de un vuelo, normalmente expresado en porcentaje.
- La finalidad es la de permitir unir las fotografías mediante estereoscopía.

![bg left:40% 100%](../assets/img_presentacion/solape.png)

---
### **Solape** 
![bg](../assets/img_presentacion/solape_1.png)
![bg](../assets/img_presentacion/solape_2.png)

---
<!-- _color: #fff -->

### **Solape** 
Más imágenes y más ángulos = Mejor resultado

![bg](../assets/img_presentacion/solape_4.png)![bg](../assets/img_presentacion/solape_5.png)

---
### **Solape** 
![bg](../assets/img_presentacion/solape_6.png)![w:725](img_presentacion/solape_7.png)

---
### **Solape** 
![bg](../assets/img_presentacion/solape_8.png)![w:600](img_presentacion/solape_9.png)

---
![bg](../assets/img_presentacion/gsd_3.png)

---
## **GSD** (Ground Simple Distance)
`distancia entre dos centros de píxeles consecutivos medidos en el suelo. A mayor valor de la imagen, menor será la resolución espacial y los detalles serán menos visibles.`
![center w:800](../assets/img_presentacion/gsd_6.png)

- Mayor GSD = Resolución espacial más baja (menos detalle)
- Menor GSD = Mayor resolución espacial, más detalle

---
## **GSD**
- Mayor GSD = Menor resolución espacial (menos detalle)
- Menor GSD = Mayor resolución espacial (más detalle)

![center w:600](../assets/img_presentacion/gsd.png)

El GSD varía con los cambios de terreno

---
## Precisión a partir del GSD
[**Cálculo del Ground Simple Distance**](https://support.pix4d.com/hc/en-us/articles/202560249-TOOLS-GSD-calculator)

![bg right  w:500](../assets/img_presentacion/gsd_5.png)
![bg  vertical w:700](../assets/img_presentacion/gsd_4.png)

---
### **GSD**
![bg fit](../assets/img_presentacion/gds4.png)

---
### **GSD**

- **A** = altura o distancia **[metros]**
- **Iw** = ancho de imagen **[pixeles]**
- **Fr** = distancia focal **[millímetros]**
- **Sw** = ancho de sensor **[millímetros]**

![bg right:33% 100%](../assets/img_presentacion/gsd3.png)

---
## La resolución importa
- Una mayor resolución del sensor producirá una representación más detallada en la imagen
- Siempre seleccionar la resolución de imagen más elevada

![bg right:35% 100%](../assets/img_presentacion/sensor_size.png)

---
![bg fit](../assets/img_presentacion/Camera-Sensor-Size-Comparison.jpg)

---

![bg](../assets/img_presentacion/full_image.JPG)
![bg](../assets/img_presentacion/half_image.jpg)

---

![bg 1000%](../assets/img_presentacion/full_image.JPG)
![bg 1000%](../assets/img_presentacion/half_image.jpg)

---

![bg](../assets/img_presentacion/full_image_pix4d.JPG)
![bg](../assets/img_presentacion/half_image_pix4d.JPG)

---

### La fotogrametría no siempre funciona

- Objetos o superficies sin detalles
- patrones para reconstruir la geometría
- Metales, cristal u objetos transparentes

---

![bg](../assets/img_presentacion/texture_1.png)
![bg](../assets/img_presentacion/texture_2.png)
![bg](../assets/img_presentacion/texture_3.png)

---
![bg 80%](../assets/img_presentacion/office_building_cover.png)

---
![bg 80%](../assets/img_presentacion/dji_building.png)

---
<!-- _class: lead -->
### Hablemos de **precisión**. ¿Para qué se utiliza un dron en topografía/cartografía?

![bg right:45% 150%](../assets/img_presentacion/traditionalsurveyor.svg)

---
![center](../assets/img_presentacion/precio_gps_1.png)

---
![center](../assets/img_presentacion/precio_gps_2.png)

---
![bg](../assets/img_presentacion/digitalsurveyor.svg)

---
[![bg fit](../assets/img_presentacion/campo_golf.png)](https://tecnitop.threedcloud.com/visor/viewer.php?tk=islantilla)

---

## **Conceptos básicos.** Necesito más precisión

**Opción 1**
El topógrafo utiliza dos aparatos (Rover y base) que comunican vía radio, uno para ponerlo en un punto de coordenadas conocidas, y otro donde se trabajaba.
![bg right:45% 120%](../assets/img_presentacion/gps_gnssBase.png)

---
## **Conceptos básicos.** Necesito más precisión
**Opción 2**
También se pueden utilizar antenas colectivas que transmiten datos vía Internet-Móvil, por ejemplo la **[red geodésica de Aragón](http://gnss.aragon.es/)**
![bg right:55% 105%](../assets/img_presentacion/gpsrtk_gnssBase.png)

---

## **Conceptos básicos.** Opción 2

Solo necesito conexión a internet. Me conecto al servidor y recibo las correcciones de mi posición, pudiendo obtener precisiones centimétricas con mi GPS (rover).
![bg right:33%](../assets/img_presentacion/aragea_base.png)
[Servicio de Posicionamiento en Tiempo Real - Aragea](https://idearagon.aragon.es/portal/aragea.jsp)
[Servicio de Posicionamiento en Tiempo Real - IGN](https://www.ign.es/web/ign/portal/gds-gnss-tiempo-real)

---

## Drones con RTK

![bg w:500](../assets/img_presentacion/ebeeX.png)![bg w:400](../assets/img_presentacion/gs16.png)

---
## Drones **sin RTK**

![bg:33%](../assets/img_presentacion/mavic2.png)
![bg right:33% 100%](../assets/img_presentacion/gcp.png)

---

### Adquirir puntos de apoyo. **Cómo medir la posición de un objetivo de GCP**

![bg left:30% 80%](../assets/img_presentacion/medirPosicion.png)

- Los GCPs se miden comúnmente con un receptor GNSS RTK / PPK o una estación total. Nos dan:
  - Posición
  - Orientación
  - Escala
---

## Adquirir puntos GPS de apoyo. **Datos exportados de un GPS RTK**

| **ID** |   **X**    |    **Y**    |  **Z**  |
| :----: | :--------: | :---------: | :-----: |
|   1    | 672462.729 | 4677541.129 | 641.174 |
|   2    | 672476.875 | 4677543.293 | 641.628 |
|   3    | 672474.134 | 4677556.679 | 639.873 |
|   4    | 672497.089 | 4677565.651 | 641.346 |
|   5    | 672524.231 | 4677563.080 | 640.912 |
|   6    | 672534.331 | 4677555.981 | 639.723 |
|   7    | 672519.130 | 4677543.962 | 640.388 |
|   8    | 672508.032 | 4677554.127 | 640.365 |
|   10   | 672473.681 | 4677532.723 | 640.489 |
|   11   | 672480.517 | 4677538.262 | 641.572 |
|   12   | 672488.607 | 4677536.576 | 641.518 |

---
# Adquirir puntos GPS de apoyo. **Toma de datos con GPS RTK**

![bg right:40% 70%](../assets/img_presentacion/gps_height.png)

---
### Adquirir puntos GPS de apoyo. **Toma de datos con GPS RTK**

![bg right:50% 100%](../assets/img_presentacion/target_conocido.JPG)

---
### Adquirir puntos GPS de apoyo. **Colocar GCP en campo**

![bg right:65% 120%](../assets/img_presentacion/target_drone_points.png)

---
# Adquirir puntos GPS de apoyo. **Toma de datos con GPS RTK**

![bg right:40% 70%](../assets/img_presentacion/take_point_reach3.png)

https://youtu.be/4tm3bJcf_wk
https://youtu.be/BwAx5-Wqd_A

---
## Ejemplos de proyectos

##### Monitorización de los recursos hidrológicos nivales: [el glaciar de Monte Perdido](https://www.youtube.com/watch?v=LmFXOKf-TKE) (Huesca)

[![center w:600](../assets/img_presentacion/mp_1.png)](https://tecnitop.threedcloud.com/visor/viewer.php?tk=moneP)

---
![bg](../assets/img_presentacion/mp_2.png)
![bg](../assets/img_presentacion/mp_3.png)

---

![bg contain](../assets/img_presentacion/mp_4.png)

---

![bg contain](../assets/img_presentacion/mp_5.png)

---

![bg contain](../assets/img_presentacion/mp_6.png)

---

# [Seguimiento de la erupción](https://datos-lapalma.opendata.arcgis.com/)

![bg right](../assets/img_presentacion/laPalma.png)
[Proyecto QGIS](https://drive.google.com/file/d/1D2aBwB3IKoYT-drgazqQVGmx-X64JZdq/view?usp=sharing)

[13/10](https://datos-lapalma.opendata.arcgis.com/maps/d1a80de876b14f188cece8da90fc54f0/explore)
[18/10](https://datos-lapalma.opendata.arcgis.com/maps/d1a80de876b14f188cece8da90fc54f0/explore)

---
<!-- _color: #fff -->
### Extracción de altura de líneas de alta tensión por fotogrametría y estereoscopía
![bg](../assets/img_presentacion/lineas.png)

---
<!-- _color: #fff -->
### Extracción de altura de líneas de alta tensión por fotogrametría y estereoscopía

![bg](../assets/img_presentacion/lineas_2.png)

---
<!-- _color: #fff -->
# Extracción de altura de líneas de alta tensión por fotogrametría y estereoscopía

![bg](../assets/img_presentacion/lineas_3.jpeg)

---
<!-- _class: lead -->
# Software
<iframe src="software.html" style="height:600px;"></iframe>

---
![bg](../assets/img_presentacion/pix4d_suite.svg)

---
<!-- _backgroundColor: #1962a7ff -->
<!-- _color: #fff -->
<!-- _class: lead -->
# Procesamiento con Pix4D

---
<!-- _backgroundColor: #1962a7ff -->
<!-- _color: #fff -->
<!-- _class: lead -->
# Procesamiento datos LIDAR con DJI Terra - Matrice 300 RTK

---
<!-- _backgroundColor: #1962a7ff -->
<!-- _color: #fff -->
<!-- _class: lead -->

# Práctica con Agisoft Metashape

---

# Práctica con Agisoft Metashape
- Descarga el proyecto
  - [Plantación aguacates](http://gofile.me/70z3P/8vN4yQHCV)
  - [Finca con dron sin rtk y sin GCP](http://gofile.me/70z3P/dTRGjpwFQ)
  - [Finca con dron RTK](http://gofile.me/70z3P/vX0SMIKJE)
- Descarga [Agisoft](https://www.agisoft.com/downloads/installer/)

---
# Práctica con Cloud Compare
- Descarga la [nube de puntos](http://gofile.me/70z3P/CcmGVm90M)
- Descarga [Cloud Compare](https://www.danielgm.net/cc/)
  
---

# Gracias!

![bg right:35% 90%](../assets/portada_charla.jpg)
## ![image w:50px](../assets/rrss/email.png) / joan@liberam.es
## ![image w:50px](../assets/rrss/linkedin.png) / liberam-technologies
## ![image w:50px](../assets/rrss/insta.png) / _liberam


