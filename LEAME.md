https://www.youtube.com/watch?v=EJjiK16Lw_8

AWS Amplify
Nos permite generar el backend rapido, con un api, base de datos, subida de archivos, despliegue de la app, analyticas y mas caracteristicas gracias a los servicios de aws

git clone https://github.com/agsmanmx/nextjs-amplify-aws

ya en el repositorio local ejecutamos en consola DE VSCODE 

npm i

ejecutamos 
npm i next@latest
npm i node@latest

npm run dev
Esto levantara una app en el servidor local en puerto 3000
http://localhost:3000/

Para acceder a la configuracion del entorno, bd, etc de produccion en aws, realizmaos una busqueda de dinamoDB en la consola de aws en su pagina web aws.

Instalar para agregar un framework de css para tener interfaces graficas o un conjunto de bibliotecas de componentes
npm add @aws-amplify/ui-react

Generamos un entorno de pruebas para la base de datos, por defecto la aplicacion demo viene configurada con el entorno de produccion
npx ampx sandbox

Esto nos indica que fallo la carga de las credenciales de acceso al entorno aws, por tanto realizamos una busqueda del servicio AIM en la consola de AWS en su pagina web y desde ahi podremos gestionar los usuarios de la base.
He creado un usuario con acceso a administracion de amplify y le he creado un par de claves token de acceso a aws desde la CLI de aws, por tanto instalamos en local la cli de aws


https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html
Como estoy en windows ejecuto abriendo consola de powershell:
msiexec.exe /i https://awscli.amazonaws.com/AWSCLIV2.msi


Para comprobar que todo se instalo bien, comprobamos la  version de aws cli
Escribimos en consola aws --version

Ahora si ejecutamos en al consola lo siguiente para configurar el acceso al usuario que conectara al servidor de pruebas de la bd de aws

ejecutamos :

aws configure 

Nos solicitara las claves de token y otros datos y podremos de este modo ejecutar el comando 

npx ampx sandbox


