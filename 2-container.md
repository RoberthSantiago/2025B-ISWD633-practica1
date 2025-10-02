# Contenedores

### Crear un contenedor
Para crear un nuevo contenedor Docker a partir de una imagen específica, pero sin iniciarlo automáticamente. 

```
docker create --name <nombre contenedor> <nombre imagen>:<tag>
```
Crear el contenedor  **srv-web** usando la imagen nginx version alpine
<img width="797" height="110" alt="image" src="https://github.com/user-attachments/assets/58a0c3b9-f918-4316-aba6-5d836f608c2c" />


Si creas un contenedor en Docker sin asignarle un nombre específico utilizando la opción --name, Docker asignará automáticamente un nombre aleatorio al contenedor. Este nombre suele consistir en una combinación de palabras y números.  

Crear el contenedor usando la imagen hello-world
<img width="803" height="104" alt="image" src="https://github.com/user-attachments/assets/5c012578-a431-4932-8c19-5021aee7fee1" />


### Listar los contenedores ejecutándose o no

```
docker ps -a
```

### Para iniciar un contenedor

```
docker start <nombre contenedor o identificador>
```
Iniciar el contenedor srv-web 
<img width="582" height="109" alt="image" src="https://github.com/user-attachments/assets/ac9d7cf3-3986-4a4e-8fc4-51e7cf225604" />

### Listar los contenedores ejecutándose
```
docker ps 
docker ps | grep <nombre contenedor>
```
<img width="1270" height="141" alt="image" src="https://github.com/user-attachments/assets/9e396b86-e21a-4fbd-93c4-bb31cc52f2f8" />


### Para detener un contenedor

```
docker stop <nombre contenedor>
```
<img width="558" height="110" alt="image" src="https://github.com/user-attachments/assets/278316d6-c4b6-4a3f-b024-e3758f0eeca2" />


### Para crear un contenedor y ejecutarlo inmediatamente

```
docker run --name <nombre contenedor> <nombre imagen>:<tag>
```
![Ecosistema de Docker](dockerRun.PNG)

Crear y ejecutar inmediatamente el contenedor **srv-web2** usando la imagen nginx:alpine
<img width="1041" height="690" alt="image" src="https://github.com/user-attachments/assets/ebdc5e21-bd59-47b5-8f83-da931f85124d" />


**¿Qué sucede luego de la ejecución del comando?**
Se esta ejecutando el contenedor en primer plano y que solo captura la entrada estandar de la entrada principal.

Cuando ejecutas un contenedor en primer plano sin la opción -d (modo detach), el contenedor captura la entrada estándar (stdin) del terminal, lo que significa que el terminal queda "atrapado" y no puedes introducir más comandos hasta que detengas el contenedor.

### Para crear un contenedor y ejecutarlo inmediatamente sin estar vinculados al mismo
-d: Es la opción que indica a Docker que ejecute el contenedor en segundo plano (en modo "detach").
Cuando un contenedor se ejecuta en segundo plano, Docker devuelve el control al terminal inmediatamente después de iniciar el contenedor, lo que permite al usuario seguir ejecutando otros comandos en el mismo terminal sin que el contenedor detenga la interacción.

```
docker run -d --name <nombre contenedor> <nombre imagen>:tag
```
Crear y ejecutar inmediatamente el contenedor **srv-web3** en modo detach usando la imagen nginx:alpine
<img width="832" height="119" alt="image" src="https://github.com/user-attachments/assets/e7b4e9e9-2b5a-480e-9fc3-c1e83845d93b" />


### Para eliminar un contenedor

```
docker rm <nombre contenedor>
```
Eliminar el contenedor que se creó a partir de la imagen hello-world 
<img width="680" height="102" alt="image" src="https://github.com/user-attachments/assets/47a74d1d-67f6-418d-b6c3-30ce50eab679" />


Verificar que el contenedor que se eliminó
<img width="1463" height="173" alt="image" src="https://github.com/user-attachments/assets/94a5c211-35ef-47f2-b5aa-9b0f153f37fc" />


### Para eliminar un contenedor que esté ejecutándose

```
docker rm -f <nombre contenedor>
```
Eliminar el contenedor **srv-web3** 
<img width="564" height="73" alt="image" src="https://github.com/user-attachments/assets/a739fc65-845e-4798-bedc-6a32f6b98ac6" />


Verificar que el contenedor que se eliminó
<img width="1504" height="149" alt="image" src="https://github.com/user-attachments/assets/2faa7e9c-896c-44f0-9fe3-81fe9d66a904" />


### Para inspecionar un contenedor 

Inspeccionar el contenedor **srv-web** 
<img width="1252" height="1414" alt="image" src="https://github.com/user-attachments/assets/4c268e3b-692b-4244-9be8-02c38e712846" />

