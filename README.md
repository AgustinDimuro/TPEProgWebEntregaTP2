# TPEProgWebEntregaTP2

En este repositorio se encontrará la resolución de los incisos solicitados para la entrega referente al **Trabajo Práctico Especial de Programación Web** en el **Trabajo Práctico 2**.  

Los integrantes del grupo son:  
- Agustín Nicolás Dimuro  
- Tomás Agustín Padilla  

---
## Descripción de la base de datos

Actualmente la base de datos posee dos tablas. Una referete a las cabañas y la información asociada a ellas como un identificador, que es el número de cabaña, datos de contacto y credenciales de acceco a la plataforma. Para el caso de la segunda tabla, se almacenan los datos referentes a las reservas, como el número de la cabaña que realiza la reserva y la fecha.


---

## Cómo inicializo la base de datos

1. Clonar el repositorio.  
2. Abrir una terminal y navegar hasta el directorio **`TPEProgWebEntregaTP2`** (podés usar `ls` para listar directorios y luego `cd` para entrar).  
3. Inicializar el docker, base de datos en PostgreSQL y generar el código necesario con sqlc mediante el comando:
    
    ```bash
    make start

Luego de ejecutado este comando, se realizará la descarga de la imágen de PostgreSQL para el docker compose en caso de que no este descargada en su dispositivo. De mismo modo, se ejecutará el comando "sqlc generate" y generara el código pertinente para las queries. Por último, se ejecutara el main.go preparado para que pueda observar una prueba realizada sobre la base de datos en la cuál se creará una cabaña, se creará una reserva, se listarán tanto la reserva como la cabaña, y por último se preguntará si dada una fecha existe una reserva.

---
## Requisitos previos
- [Go](https://go.dev/dl/) (versión 1.20 o superior recomendada)  
- Git (para clonar el repositorio)  
- SQLC (para poder generar el código)

Podés verificar si tenés Go instalado ejecutando en la terminal:

    ```bash
    go version

---
## Consejo en caso de que el sqlc no esté instalado o generé error de path (127).
Los siguientes consejos serán utiles en caso de tener Ubuntu/Linux, LinuxMint o similares.
En caso de que no tenga instalado sqlc debe ejecutar el comando:
    
    ```bash
    go install github.com/sqlc-dev/sqlc/cmd/sqlc@latest
    export PATH=$PATH:$(go env GOPATH)/bin


En caso que al ejecutar, se genere el error 127 o error de path, recomendamos ejecutar los siguientes comandos

    ```bash
    echo 'export PATH=$PATH:$(go env GOPATH)/bin' >> ~/.bashrc
    source ~/.bashrc

Para verificar correcta instalación puede utilizar el comando:
    
    ```bash
    sqlc version

Para confirmar donde quedo instalado puede ejecutar el comando:
    
    ```bash
    go env GOPATH

Esto debería mostrarle /home/tuUsuario/go lo que significaría que el sqlc está instalado en el path correcto.


