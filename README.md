  <style>
    body {
      font-family: sans-serif;
      margin: 20px;
      background: #f0f2f5;
    }

    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 20px;
      max-width: 900px;
      margin: auto;
    }

    .gallery img {
      width: 100%;
      height: 400px; /* Altura fija para uniformidad */
      object-fit: cover;
      border-radius: 16px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
      background: white;
    }

    @media (max-width: 600px) {
      .gallery img {
        height: 300px;
      }
    }
  </style>

<h1>Proyecto TRAINTRAVELAPP  # Challenge_Diplomatura</h1>
<h1>Documentación sobre el challenge</h1>


<hr>


Este es el Repositorio del Challenger - Diplomatura


<h2>DOCUMENTACIÓN DE LA API</h2>

https://github.com/bump-sh-examples/train-travel-api

![image](https://github.com/user-attachments/assets/61e3a4aa-45f6-4cbd-a58f-465877454b91)


<h2>Link del Jira</h2>

https://actividad4.atlassian.net/jira/software/projects/LC/boards/269
<hr>
<h2>Estructura de Documentacion</h2>

🗂️Challenge_Diplomatura/<br>
├── 🗂️PrototipoPantallas                            <i>  (Prototipos de Pantallas)</i><br>
├── 🗂️QA_API                                        <i>  (Ejercicios Postman, Newman y Jenkins)</i><br>
├── 🗂️Zephyr                                        <i>  (Reporteria de Zephyr)</i><br>
├── Equipo 1_Sugerencia.txt                          <i>  (Sugerencias para armado Json)</i><br>
├── Equipo1.png                                      <i>  (Imagen: Integrantes de grupo)</i><br>
├── Instrucciones_ChallengerFinal.pdf                <i>  (Instrucciones del trabajo)</i><br>
├── Req_NuestraTravelApp.pdf                         <i>  (Requerimientos de la APP)</i><br>
├── README.md                                        <i>  (Este archivo)</i><br>
└── train-travel-api-openapi-source.jso              <i>  (Json modelo)</i><br>

<br>

 <h1 style="text-align: center;">Pantallas de la App</h1>
  <div class="gallery">
    <img src="PrototipoPantallas/1 - Inicio.jpg" alt="Pantalla 1" />
    <img src="PrototipoPantallas/2 - Datos Personales.jpg" alt="Pantalla 2" />
    <img src="PrototipoPantallas/3 - Consulta de viajes.jpg" alt="Pantalla 3" />
    <img src="PrototipoPantallas/4 -  Seleccion de Origen y Destino.jpg" alt="Pantalla 4" />
    <img src="PrototipoPantallas/5 - Opciones de viajes.jpg" alt="Pantalla 5" />
    <img src="PrototipoPantallas/6 - Pasaje - Generacion Qr.jpg" alt="Pantalla 6" />
  </div>
