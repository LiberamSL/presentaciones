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

# El uso de OpenDroneMap en proyectos de fotogrametría aérea con drones
![bg right:33% contain](../assets/img_presentacion/odm.png)


13 de mayo

###### Joan Cano / [Liberam](https://liberam.es) / esLibre

![bg](../assets/portada.ng)

---

<!-- backgroundColor: white -->
<!-- _class: lead -->

## > whoami

###### Joan Cano
<p style="color: grey; font-size: 0.8em;">Geógrafo especializado en GIS, Teledetección, láser escáner, fotogrametría y UAV</p>

![bg left:40% 60%](../assets/foto_perfil.png)

---

# **OpenDroneMap** 

Herramientas de línea de comandos de código abierto para procesar **imágenes aéreas de drones**. 

**ODM** convierte imágenes en:
- Nubes de puntos clasificadas
- Modelos 3D texturizados
- Imágenes ortorrectificadas georreferenciadas
- Modelos digitales de elevación georreferenciados

---

![bg fit](../assets/img_presentacion/odm_output_1.png)

---

![bg fit](../assets/img_presentacion/odm_output_2.png)

---

# Fotogrametría
![bg right:800](../assets/img_presentacion/img_fotogrametria3.gif)

---

## De sensores digitales a información espacial

Transformación de imágenes tomadas a mano, por drones o con avioneta en mapas 2D precisos y georreferenciados, modelos 3D, nubes de puntos y análisis.

![bg vertical w:450](../assets/img_presentacion/img_fotogrametria.jpg)
![bg right w:550](../assets/img_presentacion/img_fotogrametria2.jpg)

---
<!-- _color: #fff -->

![bg](../assets/img_proyectos/masqi11.png)

---
<!-- _color: #fff -->

![bg](../assets/img_proyectos/masqi12.png)

---

![bg fit](../assets/img_proyectos/golf1.png)

---

![bg](../assets/img_proyectos/golf2.png)

---
<!-- _color: #fff -->

![bg](../assets/img_proyectos/climbingSurvey.png)

---

# **Instalación** 

## Docker 

```
# Windows
docker run -ti --rm -v c:/Users/youruser/datasets:/datasets opendronemap/odm --project-path /NameProjectsFolder/images nameProject
```

```
# Mac/Linux
docker run -ti --rm -v /home/youruser/datasets:/datasets opendronemap/odm --project-path /NameProjectsFolder/images nameProject
```

---

#### **Agregar parámetros adicionales al proceso**

```
docker run -ti --rm -v  /home/youruser/datasets:/datasets opendronemap/odm --project-path /NameProjectsFolder nameProject [--additional --parameters --here]
```
<br>

**Ejemplo:** generar un DSM (--dsm) y aumentar la resolución de la ortofoto (--orthophoto-solution 2):

```
docker run -ti --rm -v  /home/youruser/datasets:/datasets opendronemap/odm --project-path /NameProjectFolder nameProject --dsm --orthophoto-resolution 2
```

---

# WebODM

![bg fit](../assets/img_presentacion/webodm.png)

---
# Uso de WebODM

Instalación

```
sudo apt install docker-compose
sudo apt install python-pip
git clone https://github.com/OpenDroneMap/WebODM --config core.autocrlf=input --depth 1
cd WebODM 
sudo ./webodm.sh start --media-dir /home/user/webodm_data
```

Acceder a webodm: http://localhost:8000

---
![bg fit](../assets/img_presentacion/urra_odm.png)

---

![bg fit](../assets/img_presentacion/webodm.png)

---

![bg fit](../assets/img_presentacion/webodm_pc.png)

---

## Drones con RTK

![bg w:500](../assets/img_presentacion/ebeeX.png)![bg w:400](../assets/img_presentacion/gs16.png)

---

## **Topografía con drones (sin RTK)**
**Opción 2**

![bg:33%](../assets/img_presentacion/mavic2.png)
![bg right:50% 100%](../assets/img_presentacion/gcp.png)

---

## Informes
<iframe src="../assets/img_presentacion/odm/report.pdf" width="100%" height="600px"></iframe>

---

## Comparemos

<iframe width="560" height="315" src="../assets/img_presentacion/odm/comparativa/orto_1.mp4" frameborder="0" allowfullscreen></iframe>

---

## Comparemos

<iframe width="560" height="315" src="../assets/img_presentacion/odm/comparativa/orto_2.mp4" frameborder="0" allowfullscreen></iframe>

---

## Comparemos

<iframe width="560" height="315" src="../assets/img_presentacion/odm/comparativa/pc_1.mp4" frameborder="0" allowfullscreen></iframe>

---


## Comparemos

<iframe width="560" height="315" src="../assets/img_presentacion/odm/comparativa/pc_2.mp4" frameborder="0" allowfullscreen></iframe>

---
<!-- _backgroundColor: #1e68a0 -->
<!-- _color: #fff -->

# Gracias!

![bg right:35% 80%](../assets/liberam/simbolo_white.png)
## ![image w:50px](../assets/rrss/email.png) / joan@liberam.es
## ![image w:50px](../assets/rrss/linkedin.png) / liberam-technologies
## ![image w:50px](../assets/rrss/insta.png) / _liberam
