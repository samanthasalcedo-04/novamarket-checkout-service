# Guía de instalación

## Propósito
Esta guía detalla los pasos necesarios para configurar y desplegar de forma segura el servicio Checkout Service de NovaMarket en entornos de desarrollo y pruebas.

## Requisitos previos
* Git instalado en el sistema local.
* Node.js v18 o superior.
* Acceso credencializado al repositorio de NovaMarket.

## Preparación del entorno
1. Clonar el repositorio en el espacio de trabajo local.
2. Configurar las variables de entorno en el archivo `.env` tomando como base el archivo `.env.example`.
3. Ejecutar `npm install` para restaurar las dependencias del proyecto.

## Validación funcional
Para verificar que el entorno base está levantado, ejecute el comando `npm run test:init`. El sistema deberia retornar un estado exitoso (200 OK) en el puerto local.
> Advertencia: la validación no debe considerarse completa si solo se revisa el contenido del archivo. También debe comprobarse que el entorno local permite ejecutar el flujo documentado.

## Error común que debe evitarse
No omitir la configuración de las variables de entorno locales, ya que el servicio no iniciará sin los tokens de conexión a la base de datos de pasarela de pagos.