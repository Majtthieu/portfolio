<template>
    <div class="form-container">
    <h3>Contactez-moi</h3>
    <form @submit="submitForm">
        <label for="name">Nom :</label>
        <input type="text" id="name" v-model="name" required>
        
        <label for="email">Email :</label>
        <input type="email" id="email" v-model="email" required>
        
        <label for="message">Message :</label>
        <textarea id="message" v-model="message" required></textarea>
        
        <button type="submit">Envoyer</button>
    </form>
    <!-- <div v-if="submitted" class="">
<p class="">Merci ! À bientôt</p>
</div> -->
</div>
</template>

<script>
export default {
    data() {
        return {
            name: '',
            email: '',
            message: ''
        };
    },
    methods: {
        submitForm() {
            const subject = 'Nouveau message de ' + this.name;
            const body = 'Email : ' + this.email + '\n\n' + 'Message : ' + this.message;
            const mailtoLink = 'mailto:ricpau51@gmail.com?subject=' + encodeURIComponent(subject) + '&body=' + encodeURIComponent(body);
            window.location.href = mailtoLink;
        }
    }
};
</script>

<style scoped>@import "./ContactForm.sass";</style>