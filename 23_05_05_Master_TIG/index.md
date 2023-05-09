---
marp: true
theme: gaia
class:
title: UA
author: Joan Cano
# paginate: true
# header: 'Header content'
footer: '![image w:50px](../assets/liberam/simbolo_white.png)'
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

# Nubes, y de puntos

9 de mayo

###### Joan Cano / [Liberam](https://liberam.es) / Máster en TIG Unizar

![bg](../assets/portada.ng)

---

<!-- backgroundColor: white -->
<!-- _class: lead -->

## > whoami

###### Joan Cano
<p style="color: grey; font-size: 0.8em;">Geógrafo especializado en GIS, Teledetección, láser escáner, fotogrametría y UAV</p>

![bg left:40% 60%](../assets/foto_perfil.png)

---

## 2017 - 2023
#### (2017 - 2023) Tecnitop / 3DScanner
Soporte técnico, proyectos relacionados con fotogrametría, láser escáner y drones

#### (2023) Liberam
Operadora de drones, fotogrametría, láser escáner, cartografía

---

# 2017 - 2023
![bg right:100% 70%](../assets/joan_2017.png)
![bg left:100% 50%](../assets/foto_perfil.png)

---

### ¿De qué vamos a hablar? 2017 - 2023

<iframe src="diagrams/indice.html" style="height:100%; width: 100%;"></iframe>

---

### ¿De qué vamos a hablar? 2023

<iframe src="diagrams/indice2.html" style="height:100%; width: 100%;"></iframe>

---
# Fotogrametría
![bg right:800](../assets/img_presentacion/img_fotogrametria3.gif)


----


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
![center w:1200](../assets/img_presentacion/inputs_pix4d.png)

---
# Outputs
![center w:1200](../assets/img_presentacion/outputs.png)

---

# Profundicemos: **Fotogrametría** <!--fit -->
- Ciencia que permite realizar mediciones
- Se necesitan imágenes principalmente
- Mediciones y representaciones 2D y 3D
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
<i>A tener en cuenta cuando se realiza un vuelo fotogramétrico</i>

### **Solape** Longitudinal / Transversal

- Recubrimiento entre las pasadas de un vuelo, normalmente expresado en porcentaje.
- Finalidad: permitir unir las fotografías mediante estereoscopía.

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
## **GSD** (Ground Simple Distance)
<i>distancia entre dos centros de píxeles consecutivos medidos en el suelo. A mayor valor de la imagen, menor será la resolución espacial y los detalles serán menos visibles.</i>

![center w:600](../assets/img_presentacion/gsd.png)

---

![center w:1000](../assets/img_presentacion/gsd_3.png)

El GSD varía con los cambios de terreno

---

![center w:1000](../assets/img_presentacion/gsd_6.png)

---

## Precisión a partir del GSD
[**Cálculo del Ground Simple Distance**](https://support.pix4d.com/hc/en-us/articles/202560249-TOOLS-GSD-calculator)

![bg right  w:500](../assets/img_presentacion/gsd_5.png)
![bg  vertical w:700](../assets/img_presentacion/gsd_4.png)

---

### **GSD**

- **A** = altura o distancia **[metros]**
- **Iw** = ancho de imagen **[pixeles]**
- **Fr** = distancia focal **[millímetros]**
- **Sw** = ancho de sensor **[millímetros]**

![bg right:40% 100%](../assets/img_presentacion/gds4.png)

---

## **Resolución**
Mayor resolución del sensor: representación más detallada en la imagen

![bg right:50% 100%](../assets/img_presentacion/sensor_size.png)

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

[![bg fit](../assets/img_presentacion/masqi.png)](https://liberam.es/dev/pcviewer/masqi.html)
https://liberam.es/dev/pcviewer/masqi.html

---

## **Topografía con drones (sin RTK)**
**Opción 1**
Uso de bases que transmiten datos vía Internet-Móvil. Por ejemplo la **[Red geodésica de Aragón](http://gnss.aragon.es/)**
![bg right:55% 105%](../assets/img_presentacion/gpsrtk_gnssBase.png)

---

## **Topografía con drones**
**Opción 1**

Solo necesitamos conexión a internet. Se conecta la emisora al servidor y esta recibe las correcciones de mi posición, pudiendo obtener precisiones centimétricas con mi GPS (rover/dron).
![bg right:33%](../assets/img_presentacion/aragea_base.png)
[Servicio de Posicionamiento en Tiempo Real - IGN](https://www.ign.es/web/ign/portal/gds-gnss-tiempo-real)

---

## Drones con RTK

![bg w:500](../assets/img_presentacion/ebeeX.png)![bg w:400](../assets/img_presentacion/gs16.png)

---

## **Topografía con drones (sin RTK)**
**Opción 2**

![bg:33%](../assets/img_presentacion/mavic2.png)
![bg right:50% 100%](../assets/img_presentacion/gcp.png)

---
## **Topografía con drones (sin RTK)**
### Adquisición de puntos de apoyo

![bg left:30% 80%](../assets/img_presentacion/gs16.png)

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
### Puntos GPS de apoyo. **Toma de datos con GPS RTK**

![bg right:50% 100%](../assets/img_presentacion/target_conocido.JPG)

---
### Puntos GPS de apoyo. **Colocar GCP en campo**

![bg right:65% 120%](../assets/img_presentacion/target_drone_points.png)

---
# Puntos GPS de apoyo. **Toma de datos con GPS RTK**

![bg right:40% 70%](../assets/img_presentacion/take_point_reach3.png)

https://youtu.be/4tm3bJcf_wk
https://youtu.be/BwAx5-Wqd_A

---

#### Monitorización de los recursos hidrológicos nivales: [el glaciar de Monte Perdido](https://www.youtube.com/watch?v=LmFXOKf-TKE) (Huesca)

[![center w:500](../assets/img_presentacion/mp_1.png)](https://tecnitop.threedcloud.com/visor/viewer.php?tk=moneP)

---

# [Seguimiento de la erupción](https://datos-lapalma.opendata.arcgis.com/)

![bg right](../assets/img_presentacion/laPalma.png)
[Proyecto QGIS](https://drive.google.com/file/d/1D2aBwB3IKoYT-drgazqQVGmx-X64JZdq/view?usp=sharing)

[13/10](https://datos-lapalma.opendata.arcgis.com/maps/d1a80de876b14f188cece8da90fc54f0/explore)
[18/10](https://datos-lapalma.opendata.arcgis.com/maps/d1a80de876b14f188cece8da90fc54f0/explore)

---

# Software
<iframe src="diagrams/software.html" style="height:100%; width:100%;"></iframe>

---
<!-- _class: lead -->
<!-- _backgroundColor: #1962a7ff -->
<!-- _color: #fff -->

# Procesamiento fotogramétrico - Pix4D

---
<!-- _class: lead -->
<!-- _backgroundColor: #1962a7ff -->
<!-- _color: #fff -->

# Procesamiento fotogramétrico - Agisoft Metashape

---
# Láser escáner
![bg right:50% 180%](../assets/geoslam.png)

Instrumentos para analizar un objeto o entorno físico para reunir datos tanto de su geometría como de su radiometría (forma y color).
	
Los resultados de la toma de datos son nubes de puntos, que contienen información x, y, z y rgb.

---

### **Tipologías de captura masiva de datos**

![bg 85%](../assets/tipos_escaneres.png)

---
## **Toma de datos**
![bg 85%](../assets/funcionamiento_escaner.png)

--- 

## **Registro**
![bg 45%](../assets/img_presentacion/registro/registro.png)


---
<!-- _class: lead -->
<!-- _backgroundColor: #1962a7ff -->
<!-- _color: #fff -->

# Procesamiento con Register360

---
<!-- _class: lead -->
# **Procesamiento datos LIDAR con DJI Terra - Matrice 300 RTK**

---
# **Datos LIDAR - Elios 3**
![bg fit 45%](../assets/img_presentacion/elios3.png)


---

![bg](../assets/liberam/liberam_name_blue_black.png)

---

![bg 50%](../assets/liberam/logos.png)

---

<iframe src="https://inteligenciaclimatica.es/" style="height:100%; width: 100%;"></iframe>

---

# **Operadora de drones**
- Categoría abierta A1/A2/A3
- Categoría específica STS-ES-01 / STS-ES-02
- Radiofonista
- Inspecciones en interiores

---

<!-- _class: lead -->
# Proyectos, software y experiencias

---
<!-- _backgroundColor: #121212 -->

# **La Torronera**
![bg fit](../assets/img_proyectos/torronera.png)

---

# Bella Orxeta

![bg right:60%](../assets/img_proyectos/borxeta.png)
Datos disponibles -> http://gofile.me/70z3P/Dwj0e27Hl

---

# Toma de nube de puntos con E3
![bg fit](../assets/img_proyectos/inspector_e3.png)

---

# Control espigón del super puerto de Bilbao
![bg fit](../assets/img_proyectos/puertoBilbao.png)

---
<!-- _color: #fff -->

# MasQI
![bg](../assets/img_proyectos/masqi11.png)

---
<!-- _color: #fff -->

# MasQI
![bg](../assets/img_proyectos/masqi12.png)

---

# Delineación C. de golf
![bg right 160%](../assets/img_proyectos/golf1.png)

---

# **Delineación C. de golf**
![bg](../assets/img_proyectos/golf2.png)

---
<!-- _color: #fff -->
<!-- _backgroundColor: #1e68a0 -->

# Vuelo en zona urbana para gemelo digital
![bg 70%](../assets/img_proyectos/oza1.png)

---
<!-- _color: #fff -->

# Vuelo en zona urbana para gemelo digital
![bg](../assets/img_proyectos/oza2.png)

---
# Vuelos para redacción de proyecto A4

<iframe src="assets/vuelos_a4/index.html" style="height:100%; width: 100%;"></iframe>

---

# Vuelos para redacción de proyecto A4

![bg](../assets/img_proyectos/aguilar.png)

---

# Vuelos para redacción de proyecto A4
![bg](../assets/img_proyectos/almuradiel.png)

---

# Vuelos para redacción de proyecto A4
![bg](../assets/img_proyectos/sjulian.png)

---

<!-- _color: #fff -->

# Topografía 3D para escalada
![bg](../assets/img_proyectos/climbingSurvey.png)

---

# Servicios de cartografía web
- Librerías webmapping
- Bases de datos
- Servicios OGC
- Docker

---
<!-- _backgroundColor: #1e68a0 -->
<!-- _color: #fff -->

# Gracias!

![bg right:35% 80%](../assets/liberam/simbolo_white.png)
## ![image w:50px](../assets/rrss/email.png) / joan@liberam.es
## ![image w:50px](../assets/rrss/linkedin.png) / liberam-technologies
## ![image w:50px](../assets/rrss/insta.png) / _liberam

---

![bg contain](../assets/img_presentacion/eslibre.png)




