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
<hr>
<h2>Trabajo desde NEWMAN</h2>
<hr>
<h2>Trabajo desde Jenkins</h2>
