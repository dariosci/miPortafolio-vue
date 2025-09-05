<template>
    <section id="proyectos" class="proyectos">
        <div class="container">
            <div container class="categoria border-bottom">
                <div class="categoria_icono">
                    <i class="fa-solid fa-screwdriver-wrench"></i>
                    <h2 class="title">Proyectos</h2>
                </div>
            </div>
            <article class="container-proyectos" id="container-proyectos">
                <div class="galeria-proyectos">
                    <div class="proyecto">
                        <h3>Página Hospital</h3>
                        <img src="/src/assets/images/proyectos.jpg" alt="Foto del proyecto 1" />
                        <p>Página del Hospital Grl. Las Heras bajo portal Joomla</p>
                        <div class="botones-proyectos">
                            <a href="#">Ver más</a>
                            <a href="#">Github</a>
                            <a href="#">Tecnologias</a>
                        </div>
                    </div>
                    <div class="proyecto">
                        <h3>Proyecto Final Android</h3>
                        <img src="/src/assets/images/proyectos.jpg" alt="Foto del proyecto 2" />
                        <p>
                            Proyecto Final Integrador - Desarrollo de Aplicaciones
                            Móviles - Argentina Programa 4.0
                        </p>
                        <div class="botones-proyectos">
                            <a href="#">Ver más</a>
                            <a
                                href="https://github.com/dariosci/ProyectoFinalAndroid?tab=readme-ov-file#proyecto-final-integrador---desarrollo-de-aplicaciones-m%C3%B3viles---argentina-programa-40">Github</a>
                            <a
                                href="https://developer.android.com/studio?gad_source=1&gad_campaignid=21831783795&gbraid=0AAAAAC-IOZm5hEjrCTxjGnkQe-KeL9fkv&gclid=CjwKCAjwx8nCBhAwEiwA_z__0wXY7DSN1sbweDND7gpTR_mnN5N3ZmU1HgNDWfQWjv2yKIncPp4v8RoCngIQAvD_BwE&gclsrc=aw.ds&hl=es-419">Tecnologias</a>
                        </div>
                    </div>
                    <div class="proyecto">
                        <h3>miPortafolio</h3>
                        <img src="/src/assets/images/proyectos.jpg" alt="Foto del proyecto 3" />
                        <p>Descripción breve del proyecto 3.</p>
                        <div class="botones-proyectos">
                            <a href="#">Ver más</a>
                            <a href="https://github.com/dariosci/MiPortafolio-web">Github</a>
                            <a href="#">Tecnologias</a>
                        </div>
                    </div>
                    <div class="proyecto">
                        <h3>Proyecto 4</h3>
                        <img src="/src/assets/images/proyectos.jpg" alt="Foto del proyecto 1" />
                        <p>Descripción del Proyecto 4</p>
                        <div class="botones-proyectos">
                            <a href="#">Ver más</a>
                            <a href="#">Github</a>
                            <a href="#">Tecnologias</a>
                        </div>
                    </div>
                    <div class="proyecto">
                        <h3>Proyecto 5</h3>
                        <img src="/src/assets/images/proyectos.jpg" alt="Foto del proyecto 2" />
                        <p>Descripción del Proyecto 5</p>
                        <div class="botones-proyectos">
                            <a href="#">Ver más</a>
                            <a
                                href="https://github.com/dariosci/ProyectoFinalAndroid?tab=readme-ov-file#proyecto-final-integrador---desarrollo-de-aplicaciones-m%C3%B3viles---argentina-programa-40">Github</a>
                            <a
                                href="https://developer.android.com/studio?gad_source=1&gad_campaignid=21831783795&gbraid=0AAAAAC-IOZm5hEjrCTxjGnkQe-KeL9fkv&gclid=CjwKCAjwx8nCBhAwEiwA_z__0wXY7DSN1sbweDND7gpTR_mnN5N3ZmU1HgNDWfQWjv2yKIncPp4v8RoCngIQAvD_BwE&gclsrc=aw.ds&hl=es-419">Tecnologias</a>
                        </div>
                    </div>
                    <div class="proyecto">
                        <h3>Proyecto 6</h3>
                        <img src="/src/assets/images/proyectos.jpg" alt="Foto del proyecto 3" />
                        <p>Descripción del Proyecto 4</p>
                        <div class="botones-proyectos">
                            <a href="#">Ver más</a>
                            <a href="https://github.com/dariosci/MiPortafolio-web">Github</a>
                            <a href="#">Tecnologias</a>
                        </div>
                    </div>
                </div>
            </article>
        </div>
    </section>
</template>

<script setup>

</script>

<style scoped>
.proyectos {
  display: flex;
  justify-content: center;
}

.container-proyectos {
  display: flex;
  width: 100%;
  padding: 2rem;
  line-height: 2.5rem;
  font-size: large;
}

.galeria-proyectos {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
  justify-content: center;

}

.proyecto {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  background-color: rgb(189, 186, 186); /* Color de fondo de la tarjeta */
  border: 1px solid #ddd;
  border-radius: 5px;
  padding: 15px;
  width: calc(
    33%-40px
  ); /* Ajusta el ancho segun la cantidad de proyectos a mostrar */
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  text-align: center;
}

.proyecto img {
  width: 100%;
  height: auto;
  border-radius: 5px;
}
.proyecto h3 {
  margin-top: 10px;
  font-size: 1.2rem;
}

.proyecto p {
  margin-top: 10px 0;
}

.proyecto a {
  display: inline-block;
  margin-top: 10px;
  padding: 10px 15px;
  background-color: #007bff; /* Color del botón */
  color: white; /* Color del texto del botón */
  text-decoration: none; /* Elimina el subrayado del enlace */
  border-radius: 5px; /* Bordes redondeados del botón */
}

.proyecto a:hover {
  background-color: #002752;
  text-decoration: none; /* Elimina el subrayado del enlace */
  color: white;
}

.botones-proyectos {
  margin-top: auto;
}

.darkModeSwitch .proyecto p{
  color: black;
}
/* Media Queries agrupadas */
@media (max-width: 767px) {
  .proyecto {
    width: calc(100% - 40px);
  }
}
/* Tablets (Pantallas medianas, entre 768px y 1023px) */
@media (min-width: 768px) and (max-width: 1023px) {
  .proyecto {
    width: calc(50% - 40px);
  }
}
/* Escritorio (Pantallas anchas, a partir de 1024px) */
@media (min-width: 1024px) {
  .proyecto {
    width: calc(33% - 40px);
  }
}

</style>