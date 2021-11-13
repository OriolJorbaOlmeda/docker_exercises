Para poder realizar este apartado, reutilizaremos el Dockerfile del ejercicio anterior y lo modificaremos. Para que exponga el servicio en el purto 8080 y siga la configuración pedida en el enunciado, el código tendrá que quedar de la siguiente manera: (ver imagen_5.png)
De esta forma tenemos un Healthcheck con un intervalo de 45s un tiempo de espera a respuesta de 5s, un tiempo de espera de 15s y 2 reintentos.
Para poder llevarlo a cabo, crearemos una imagen de este dockerfile: (ver imagen_6.png)
Con la imagen solo nos falta hacer la prueba con docker run –d –p 8080:80 go_healthcheck: (ver imagen_7.png)
Como podemos ver en la imagen superior, aun no está en status healthy, ya que no han pasado los 45 segundos: (ver imagen_8.png)
Una vez pasados los 45 segundos podemos ver que el status ha cambiado a healthy, tal y como deseábamos.
