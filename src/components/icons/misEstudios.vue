<template>
    <section id="estudios" class="estudios">
        <div class="container">
            <div container class="categoria border-bottom">
                <div class="categoria_icono">
                    <i class="fa-sharp fa-solid fa-graduation-cap"></i>
                    <h2 class="title">Estudios</h2>
                </div>
            </div>
            <table id="tabla-cursos">
                <thead>
                    <tr>
                        <th>Curso / Institución</th>
                        <th>Año</th>
                        <th>Horas</th>
                        <th></th>
                    </tr>
                </thead>
                <tbody>
                    <!-- Aquí se insertarán las filas -->
                </tbody>
            </table>
        </div>
    </section>
</template>

<script setup>

</script>

<script>
document.addEventListener("DOMContentLoaded", function () {
    let url2 =
        "https://raw.githubusercontent.com/dariosci/MiPortafolio-web/refs/heads/main/JSON/estudios.json";

    const tbody = document.querySelector("#tabla-cursos tbody");
    fetch(url2)
        .then((response) => response.json())
        .then((data2) => {
            data2.forEach((curso) => {
                const tr = document.createElement("tr");
                tr.innerHTML = `
          <td>
            <strong>${curso.course_name}</strong><br>
            <span class="instituto-class">${curso.course_instr}</span>
          </td>
          <td>${curso.course_date}</td>
          <td>${curso.course_totalHoras}</td>
          <td>${curso.course_link
                        ? `<a href="${curso.course_link}" target="_blank" title="Ver curso">
            <i class="fa-solid fa-arrow-up-right-from-square link-icono"></i>
            </a>`
                        : ""
                    }
          </td>
        `;
                tbody.appendChild(tr);
            });
        })
        .catch((error) => {
            console.error("Error al cargar el JSON:", error);
        });
});

</script>

<style scoped>
.estudios {
    display: flex;
    justify-content: center;
    padding: 2rem;
    margin-bottom: 3rem;
}

.container-estudios {
    display: flex;
    width: 100%;
    padding: 2rem;
    line-height: 2.5rem;
    font-size: large;
}

.cabecera {
    font-style: italic;
    font-size: 30px;
}

#tabla-cursos th,
#tabla-cursos td {
    padding: 0.5rem 0.3rem;
    /*text-align: left;*/
}

#tabla-cursos td:last-child {
    text-align: center;
}

#tabla-cursos th:nth-child(2),
#tabla-cursos th:nth-child(3),
#tabla-cursos td:nth-child(2),
#tabla-cursos td:nth-child(3) {
    text-align: center;
}

th {
    font-style: italic;
}

.link-icono {
    font-size: 1.2em !important;
    /* Ajusta el tamaño según prefieras */
    transition: font-size 0.2s;
}

/* Media Queries agrupadas */

/* Moviles (Pantallas pequeñas, hasta 767px) */
@media (max-width: 767px) {

    /* Agregando el responsivo para la seccion estudios */
    .container-estudios {
        width: 100%;
        margin: 0rem;
    }

    .estudios {
        width: 100%;
        padding: 1rem;
        margin-top: 1rem;
        font-size: small;
    }

    .img-estudios {
        width: 25%;
        height: auto;
        border-radius: 0.5rem;
    }

    .detalle-estudios {
        color: var(--black2);
        font-size: 15px;
        line-height: 32px;
        margin-bottom: auto;
    }

    .link-icono {
        font-size: 1em;
    }

    th {
        font-size: large;
    }

    td {
        font-size: small;
    }

    .instituto-class {
        font-style: italic;
    }
}

/* Tablets (Pantallas medianas, entre 768px y 1023px) */
@media (min-width: 768px) and (max-width: 1023px) {

    /* Agregando el responsivo para seccion estudios */
    .estudios {
        width: 100%;
    }

    #tabla-cursos th:nth-child(2),
    #tabla-cursos th:nth-child(3),
    #tabla-cursos td:nth-child(2),
    #tabla-cursos td:nth-child(3) {
        font-size: medium;
    }

    td {
        font-size: medium;
    }

    th {
        font-size: large;
    }
}

/* Escritorio (Pantallas anchas, a partir de 1024px) */
@media (min-width: 1024px) {

    /* Agregando el responsivo para seccion estudios */
    .estudios {
        width: 100%;
    }

    .container-estudios-section {
        display: flex;
        align-items: center;
        width: 100%;
        gap: 2rem;
    }

    th {
        font-size: large;
    }

    td {
        font-size: large;
    }
}
</style>