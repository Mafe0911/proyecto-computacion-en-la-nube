# Toma de pedidos a domicilio - Documentación del proyecto

Este proyecto tiene como objetivo principal crear una infraestructura completa utilizando CloudFormation para garantizar que todos los recursos creados estén centralizados en un solo lugar.

## Descripción del proyecto

Este proyecto consiste en desarrollar una aplicación completa para la toma de pedidos a domicilio de un restaurante. El enfoque principal se centra en la infraestructura. La aplicación permitirá a los clientes realizar pedidos proporcionando la siguiente información:

- Cliente:
  - Nombre completo
  - Dirección
  - Teléfono
  - Correo electrónico
- Pedido:
  - Producto
  - Cantidad
  - Valor unitario
  - Valor total

Una vez que un cliente realiza un pedido, recibirá una notificación por correo electrónico con los detalles del pedido, y el pedido se pondrá en cola para su procesamiento y envío.

Los propietarios del restaurante podrán acceder a través de un API Gateway que proporcionará dos servicios:

## - POST: Permite crear un nuevo pedido.
## - GET: Permite buscar un pedido por su identificador.

Cada pedido será respaldado en un bucket de almacenamiento. Los archivos de los pedidos se eliminarán automáticamente del bucket cada 2 días.

## Instrucciones de instalación

Para instalar y ejecutar el proyecto, siga los pasos a continuación:

1. Clonar el repositorio del proyecto:
git clone https://github.com/tu-usuario/nombre-del-repositorio.git

2. Acceder al directorio del proyecto:
cd nombre-del-repositorio

3.Configurar y desplegar la infraestructura utilizando CloudFormation:
Abra el archivo de plantilla de CloudFormation (template.yml) y modifique los parámetros y configuraciones según sea necesario.
Utilice una herramienta de línea de comandos de AWS, como la AWS CLI, para crear la pila de CloudFormation. Asegúrese de tener las credenciales adecuadas configuradas.

aws cloudformation create-stack --stack-name nombre-de-la-pila --template-body file://template.yml --capabilities CAPABILITY_IAM

##Instrucciones de ejecución
Una vez que la infraestructura esté en funcionamiento, puede utilizar el API Gateway para interactuar con la aplicación. A continuación se detallan los servicios disponibles:

POST: Para crear un nuevo pedido, realice una solicitud POST a la URL del API Gateway. Proporcione los datos del pedido en el cuerpo de la solicitud en formato JSON.

GET: Para buscar un pedido existente, realice una solicitud GET a la URL del API Gateway, incluyendo el identificador del pedido en la URL.
Ahora el proyecto está instalado y listo para ser ejecutado

## Junto a los archivos de la carpeta de proyecto final hay un documento de word donde podemos ver con más claridad los comandos que se deben ejecutar y su respectivo orden.
