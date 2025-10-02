# Imagen
### Descargar imagen
Descarga la última versión de la imagen disponible en el registro de Docker.

```
docker pull <nombre imagen> 
```

Descarga una versión específica de la imagen, cada imagen tiene etiquetas (tags) para diferentes versiones.
Una imagen puede tener la etiqueta latest para representar la última versión, si no se especifica una etiqueta se hará referencia a la versión latest.

```
docker pull <nombre imagen>:<tag>
```

Descargar la imagen **hello-world**
docker pull hello-world
<img width="957" height="182" alt="image" src="https://github.com/user-attachments/assets/b89fd8b7-f018-4400-94b7-60a9a7511a21" />


**¿Qué es nginx**
Nginx es un servidor web de alto rendimiento y código abierto que también puede funcionar como proxy inverso y balanceador de carga. Se caracteriza por su capacidad de manejar miles de conexiones simultáneas con bajo consumo de recursos, lo que lo hace ideal para sitios web de gran tráfico y aplicaciones modernas.

Descargar la imagen  **nginx** en la versión **alpine**
docker pull nginx:alpine
<img width="971" height="314" alt="image" src="https://github.com/user-attachments/assets/b0743619-ae01-4c7a-bbe3-5549125f3c0f" />



### Listar imágenes

```
docker images
```

<img width="781" height="156" alt="image" src="https://github.com/user-attachments/assets/21c3d4c9-ddff-44df-882c-8d861b1d458b" />
 

**Identificadores**

En Docker, se utilizan varios identificadores para diferenciar de manera única los elementos del sistema, como imágenes, contenedores, volúmenes y redes. Estos identificadores son generados automáticamente por Docker y son únicos dentro del contexto del sistema Docker en el que se encuentran. 

### Inspeccionar una imagen
El comando docker inspect se utiliza para obtener información detallada sobre un objeto de Docker específico, como un contenedor, una imagen, un volumen o una red.  Proporciona información en formato JSON sobre el objeto especificado.

```
docker inspect <nombre imagen>
docker inspect <nombre imagen>:<tag>
```

Inspeccionar la imagen hello-world 
<img width="1153" height="587" alt="image" src="https://github.com/user-attachments/assets/5864cb8b-2e47-4ab3-9218-0bda09108ca8" />



**¿Con qué algoritmo se está generando el ID de la imagen**
sha256:54e66cc1dd1fcb1c3c58bd8017914dbed8701e2d8c74d9262e26bd9cc1642d31 

### Filtrar imágenes

```
docker images | grep <termino a buscar>

```
<img width="732" height="199" alt="image" src="https://github.com/user-attachments/assets/0f33c10c-553d-4651-89a4-a3907abb7369" />


### Para eliminar una imagen
Eliminar permanentemente la imagen de tu sistema Docker.

```
docker rmi <nombre imagen>:<tag>
```

Eliminar la imagen hello-world 
<img width="1041" height="124" alt="image" src="https://github.com/user-attachments/assets/27d88da0-2da5-463e-9623-d01c3b163b49" />


-f: Es la opción para forzar la eliminación de la imagen incluso si hay contenedores en ejecución que utilizan esa imagen.
Cuando eliminas una imagen Docker, Docker no elimina automáticamente los contenedores que se han creado a partir de esa imagen. Esto significa que, aunque hayas eliminado la imagen, el contenedor seguirá ejecutándose normalmente.  
**Considerar**
Eliminar una imagen no afecta a los contenedores que se han creado a partir de esa imagen, a menos que esos contenedores dependan de archivos o configuraciones específicas de la imagen eliminada. En ese caso, es posible que los contenedores se comporten de manera inesperada después de eliminar la imagen.
Es una buena práctica detener y eliminar todos los contenedores que dependan de una imagen antes de eliminar la imagen en sí.

```
docker rmi -f <nombre imagen>:<tag>
```
