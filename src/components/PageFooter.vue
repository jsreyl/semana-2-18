<template>
    <footer class="page-footer bg-secondary text-white pt-4">
        <div class="container-fluid text-justify">

            <div class="row">
                <div class="col-md-5">
                    <h4 class="footer-title">Arquitectura de Servicios Tecnológicos</h4>
                    <p>Proyecto motivado por la MisionTIC2022 en su ciclo 3, donde se utilizan lenguajes para una aplicación web, conceptos de HTML, CSS, JavaScript, el uso de APIs, de VUE-JS entre otras herramientas para el aprendizaje del desarrollo web.</p>
                    <a href="https://github.com/jsreyl/semana-2-18.git">Enlace a nuestro repositorio!</a>
                </div>
                <div class="col-md-7">
                    <h4 class="footer-title">Contacto:</h4>
                    <ul class="footer-integrantes__lista">
                        <li class="footer-integrantes__lista__elemento"> <i>Alejandro Díaz Moscoso</i> (E-mail: <a href="alejo2dm@hotmail.com">alejo2dm@hotmail.com</a>) - Arquitecto de Software</li>
                            <label for="enviarMensaje"><small>Envíe su mensaje: </small> </label>
                            <input class="w-50" type="text" id="enviarMensaje">
                            <button class="btn btn-info" type="submit">Enviar mensaje</button>
                        <li class="footer-integrantes__lista__elemento"> <i>Martha Isabel Betancourt Castañeda</i> (E-mail: <a href="marticaisa4@gmail.com">marticaisa4@gmail.com</a>) - Analista de software</li>
                            <label for="enviarMensaje"><small>Envíe su mensaje: </small> </label>
                            <input class="w-50" type="text" id="enviarMensaje">
                            <button class="btn btn-info" type="submit">Enviar mensaje</button>
                        <li class="footer-integrantes__lista__elemento"> <i>Juan Sebastián Rey Lancheros</i> (E-mail: <a href="juansreyl@gmail.com">juansreyl@gmail.com</a>) - Desarrollador Fullstack</li>
                            <label for="enviarMensaje"><small>Envíe su mensaje: </small> </label>
                            <input class="w-50" type="text" id="enviarMensaje">
                            <button class="btn btn-info" type="submit">Enviar mensaje</button>
                    </ul>
                </div>
            </div>
        </div>
        
    </footer>
</template>

<script>
export default {
    name: 'PageFooter',
}
</script>

<style scoped>
/* Esta etiqueta no se va a usar porque estamos usando los de Bootstrap */
</style>