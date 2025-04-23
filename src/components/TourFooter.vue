<template>  
<div class ="footerMain">
    <div class="footerContainer">
        <div class="footerContent">
        <h2 class="footerTitle">Contáctanos</h2>
        <form @submit.prevent="submitForm" class="footerForm">
            <input type="text" v-model="contact.name" placeholder="Nombre" required class="footerInput" />
            <input type="email" v-model="contact.email" placeholder="Email" required class="footerInput" />
            <textarea v-model="contact.message" placeholder="Mensaje" required class="footerTextarea"></textarea>
            <button type="submit" class="footerButton">Enviar</button>
        </form>
        </div>
    </div>
    <div class="footerLinks">
        <router-link to="/sobre-nosotros" class="footerLink">¿Quieres saber más sobre nosotros?</router-link>
        <router-link to="/contacto" class="footerLink">Contáctenos</router-link>
        <router-link to="/politica-privacidad" class="footerLink">Política de Privacidad</router-link>
</div>
</div>
</template>

<script scoped>




</script>