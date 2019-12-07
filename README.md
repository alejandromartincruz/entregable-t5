# USO DEL ENTORNO

en este ejercicio se pueden iniicar los contenedores con las variables de entorno de desarrollo o las de producción

## Iniciar en desarrollo

Para iniciar los contenedores con las variables de desarrollo, hay que usar el siguiente comando:

```bash
docker-compose up -d
```

No hace falta declarar la variable del entorno a development, ya que es la que se inicia por defecto si no se declara, aunque si se quiere declarar se hace de la siguiente forma:

```bash
ENV=development docker-compose up -d
```

## Iniciar en producción

Para iniciar los contenedores con las variables de producción hay que hacerlo de la siguinete manera:

```bash
ENV=production docker-compose up -d
```

En caso de no indicar la variable ENV como production, se inicializará por defecto la de development como se ha indicado antes.


## Información adicional

parar todos los contenedores:

```bash
docker stop $(docker ps -a -q)
```

Eliminar todos los contenedores:

```bash
docker rm $(docker ps -a -q)
```
