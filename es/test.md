Primer encabezado | Segundo encabezado
--- | ---
Celda de contenido | Celda de contenido
Celda de contenido | Celda de contenido

Dillinger es un editor HTML5 Markdown habilitado para la nube, listo para dispositivos móviles, almacenamiento fuera de línea, con tecnología AngularJS.

- Escriba algo de Markdown a la izquierda
- Ver HTML a la derecha
- magia

#### Construyendo para fuente

Para lanzamiento de producción:

```sh
$ gulp build --prod
```

Generación de archivos zip prediseñados para su distribución:

```sh
$ gulp build dist --prod
```

Una vez hecho esto, ejecute la imagen de Docker y asigne el puerto a lo que desee en su host. En este ejemplo, simplemente asignamos el puerto 8000 del host al puerto 8080 del Docker (o cualquier puerto expuesto en el Dockerfile):

```sh
docker run -d -p 8000:8080 --restart="always" <youruser>/dillinger:${package.json.version}
```
