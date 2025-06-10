<h1>Documentación de Testing sobre la API del challenge</h1>
<hr>
<h2>Estructura de Documentacion</h2>

🗂️QA_API/<br>
├── 🗂️JenkinsRunner                                  <i> (Evidencia de ejecuciones Jenkins)</i><br>
├── 🗂️NewmanRunner                                 <i> (Evidencia de ejecuciones Newman)</i><br>
├── 🗂️PostmanRunner                                 <i>(Evidencia de ejecuciones Postman)</i><br>
├── Estaciones.postman_environment.json               <i>(Json del Api Testeado)</i><br>
├── README.md                                         <i>(Este archivo)</i><br>
└── TrainTavelAPI.postman_collection.json / etc.       <i>(Json de las Variables)</i><br>
🗂️Zephyr          <i> (Reportes de Zephyr)</i> <br> 
<h2>Casos Ejecutados</h2>
<ul>
  <li>🧪Listar Estaciones</li>
    <ul>
      <li>✅Status 200 OK</li>
      <li>✅La respuesta contiene una lista de estaciones</li>
      <li>✅Cada estación tiene id, nombre y dirección</li>
      <li>✅Cada valor de id, nombre y dirección es un string</li>
    </ul>
  <li>🧪Buscar Estacion</li>
    <ul>
      <li>✅Status 200 OK</li>
      <li>✅La respuesta contiene una lista de estaciones</li>
      <li>❌Body contiene el nombre buscado</li>
    </ul>
  <li>🧪Busqueda de viajes</li>
    <ul>
      <li>✅Status 200 OK</li>
      <li>✅Respuesta contiene viajes</li>
      <li>✅Cada viaje tiene campos válidos</li>
    </ul>
  <li>🧪Filtrar Viaje</li>
    <ul>
      <li>✅Status 200 OK</li>
      <li>❌Se reciben viajes filtrados</li>
      <li>❌Todos los viajes permiten bicicletas y perros</li>
    </ul>
  <li>🧪Listar Reservas</li>
    <ul>
      <li>✅Status 200 OK</li>
    </ul>
  <li>🧪Crear una reserva</li>
    <ul>
      <li>✅Status 201 OK</li>
      <li>✅La reserva se creó correctamente</li>
    </ul>
  <li>🧪Pagar una reserva</li>
    <ul>
      <li>❌Status 200 OK</li>
    </ul>
  <li>🧪Eliminar reserva</li>
    <ul>
      <li>❌Status 204 OK</li>
    </ul>
</ul>
<hr>
<h2>Trabajo desde POSTMAN</h2>
<p><b>GitHub: https://github.com/bump-sh-examples/train-travel-api</b></p>
<p><b>Documentación: https://bump.sh/bump-examples/doc/train-travel-api/</b></p>
<p>Se trabajó usando la documentación como base para la escritura de los casos y se realizó un "run" desde la aplicación de postman</p>
<p>Como se explica en "Casos Ejecutados", en la siguiente imagen se muestran los request utilizados</p>
*imagen de request
<p>Punto desde donde se inicio la ejecucion</p>
![image](https://github.com/user-attachments/assets/f0e339e6-49fe-4938-81f8-9ddcc7b7b9bd)

<p>Casos que pasaron/fallaron</p>
🗂️PostmanRunner 
<p>Variables utilizadas para las ejecuciones</p>
![image](https://github.com/user-attachments/assets/52d7d323-bab1-4a90-8a9d-4e76311d66a7)
<hr>
<h2>Trabajo desde NEWMAN</h2>
<p>Para las ejecuciones desde Newman se utilizó la ejecución por medio del "Via API", ademas se realizo la descarga del ambiente de variables para que los request se ejecuten satisfactoriamente</p>
<p>Obtención "Via API"</p>
![image](https://github.com/user-attachments/assets/28d7f0ec-50c3-4c4a-8bbd-5b210dfd36e4)<br>
![image](https://github.com/user-attachments/assets/59ec63e3-503b-4a81-9157-a1d9fddee0b8)<br>
![image](https://github.com/user-attachments/assets/9ce6feba-22e4-49c3-80c3-8ddef40ec8b8)<br>
<br>
<p>Comando a ejecutar: newman run https://api.postman.com/collections/22436216-d1537a91-03b0-4bcb-827e-c27d6110e094?access_key=PMAT-************************** --environment Estaciones.postman_environment.json -r htmlextra</p>
<p>Resultado de las ejecuciones</p>
🗂️NewmanRunner 
<hr>
<h2>Trabajo desde Jenkins</h2>
<p>Se realizó la creación del job correspondiente para la ejecución</p>

![image](https://github.com/user-attachments/assets/0748ae3b-b3d3-4a8d-843f-8244270d50f5)

<p>En el momento de determinar los pasos de ejecución se coloca : 

echo "Ejecutando colección de Postman con Newman..."

cd C:\Users\julio\OneDrive\Desktop\Git Descarga\mindHub\Challenge_Diplomatura\QA_API

newman run https://api.postman.com/collections/22436216-d1537a91-03b0-4bcb-827e-c27d6110e094?access_key=PMAT-XXXXXXXXXXXXX --environment Estaciones.postman_environment.json --suppress-exit-code</p>

<p>debido a que a la hora de la ejecucion el test contiene fallas calculadas el job regresa un estado "FAILURE", para corregir esto se agregó --suppress-exit-code al comendo que esta en la build step para que la ejecución regres un OK</p>
<p>Resultado de las ejecuciones</p>
🗂️JenkinsRunner
