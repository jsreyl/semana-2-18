<template>
    <div class="card text-white bg-dark">
        <div class="d-flex justify-content-center p-2">
            <svg src="./imagenes/martha.jpg" height="300px" alt="Participante 3 Martha">
            </svg>
        </div>
        <div class="card-body">
            <h2 class="card-title">Martha Isabel Betancourt Castañeda</h2>

            <p><b>Domicilio:</b> Popayán, Cauca</p>
            <p><b>Estudios:</b>  Esta joven es ingeniera de sistemas de la Corporación universitaria Remington.</p>
            <p><b>Pasatiempos:</b></p>
                <nav>
                    <ul>
                        <li>Estudiar.</li>
                        <li>Aprender.</li>
                    </ul>
                </nav>
            <p><b>Datos curiosos:</b> Es una persona activa, trabajadora y siempre le pone la mejor actitud a cada situación que se le presenta. Actualmente trabaja de noche por lo que valora mucho la oportunidad de estudiar en el día.</p>
            <p><b>E-mail:</b> marticaisa4@gmail.com</p>
        </div>
        <pre>
            {{ member }}
        </pre>
    </div>
</template>

<script>
    export default {
        name: "TeamCard",
        props: ['member']
    }
</script>

<style scoped>

</style>
