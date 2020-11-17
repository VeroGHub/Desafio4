# INSTRUCCIONES DESAFIO4 DOCKER SWARM

1. Abrir conexion a terminal o linea de comando.
 
2. Verificar que el siguiente archivo este en un directorio a su eleccion:

- docker-compose.yml 

3. En ese directorio a eleccion ejecute el siguiente comando:

   ***docker stack deploy -c docker-compose.yml (nombre stack)***

4. Conectarse al contenedor ansible que esta en ejecucion.

5. Una vez conectado al contenedor ansible, asegurarse que este posicionado en el directorio /root, luego ejecutar el siguiente comando:

   ***ansible-playbook playdesa4.yml***

6. Validar mediante cliente Rest INSOMNIA, que la carga inicial en MongoDB este disponible, mediante estas url:

    - Utilizar Metodo GET
        
- http://localhost:3000/api/animal *Este endpoint seleccciona todos los documentos de la coleccion **animal** desde el contenedor Nodejs1*.

- http://localhost:3000/api/automovil *Este endpoint seleccciona todos los documentos de la coleccion **automovil** desde el contenedor Nodejs1*.

- http://localhost:4000/api/animal *Este endpoint seleccciona todos los documentos de la coleccion **animal** desde el contenedor Nodejs2*.

- http://localhost:4000/api/automovil *Este endpoint seleccciona todos los documentos de la coleccion **automovil** desde el contenedor Nodejs2*.

7. Generar nuevos documentos en ambas colecciones **animal y automovil**, utilizar Metodo POST.

- http://localhost:3000/api/animal (NodeJS1)
    Se utiliza el siguiente formato Json:
{
 "Nombre":  "XXXXXXXXX ", 
 "Estatura":  "XXXXX ",
 "Peso":  "XXXXX "
}

- http://localhost:3000/api/automovil  (NodeJS1)
    Se utiliza el siguiente formato Json:
{
 "Modelo": "ZZZZZZZ", 
 "Ano": ZZZZZ,
 "TipoNeumatico": "ZZZZZZ"
}

- http://localhost:4000/api/animal (NodeJS2)
    Se utiliza el siguiente formato Json:
{
 "Nombre":  "XXXXXXXXX ", 
 "Estatura":  "XXXXX ",
 "Peso":  "XXXXX "
}

- http://localhost:4000/api/automovil (NodeJs2)
    Se utiliza el siguiente formato Json:
{
 "Modelo": "ZZZZZZZ", 
 "Ano": ZZZZZ,
 "TipoNeumatico": "ZZZZZZ"
}
    
    


















