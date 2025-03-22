# demo-docker
## Comandos básicos
- `docker ps`: Ver contenedores corriendo.
- `docker ps -a`: Ver contenedores corriendo y parados.
- `docker images`: Listar las imágenes base disponibles.
- `docker pull nginx`: Descarga la imagen Nginx.
- `docker pull alpine`: Descarga la imagen de Alpine.
- `docker run alpine`: Crea un contenedor Alpine, se para inmediatamente. Verificar con `docker ps -a`.
- `docker run nginx`: Crea un contenedor Nginx y queda ejecutándose. Verificar en otra ventana con `docker ps`.
- `docker run -d nginx`: Crea un contenedor Nginx y queda ejecutándose en **segundo plano**. Verificar con `docker ps`.
- `docker run --name web-1 -d --rm nginx`: Crea un contenedor Nginx y queda ejecutándose en **segundo plano**. Verificar con `docker ps`.
- `docker stop ID_CONTENEDOR`: Para el contenedor con el ID especificado.
- `docker run --rm -it alpine`: Ejecuta un Alpine de forma **interactiva**, compartiendo terminal. Al pararlo, se eliminará automáticamente por el `--rm`.
- `docker run -d --name web-1 -p 7000:80 nginx`: Crea un contenedor Nginx en **segundo plano**, enlazando el puerto 80 del Nginx dentro del contenedor al puerto 7000 en la máquina **host**.



## Tarea : Explicar que hace este comando y porque funciona.

- `docker run -d --name web-2 -p 8000:80 -v /workspaces/docker:/usr/share/nginx/html:ro nginx`