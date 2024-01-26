<template>
    <div class="form-container">
        <h3>Contactez-moi</h3>
        <form ref="form" @submit.prevent="sendEmail">
            <label>Nom</label>
            <input class="form-input" type="text" name="from_name" placeholder="Entrez votre nom svp" required>
            <label>Email</label>
            <input class="form-input" type="email" name="reply_to" placeholder="Entrez votre email svp" required>
            <label>Message</label>
            <textarea class="form-message" name="message" required style="resize: none;"></textarea>
            <button class="button_global button_form" type="submit">Envoyer</button>
        </form>
        <p v-if="submitted">Votre message a bien été envoyé. À bientôt</p>
    </div>
</template>

<script>
import emailjs from '@emailjs/browser';
export default {
  data() {
    return {
      submitted: false,
    };
  },

  methods: {
    sendEmail() {
      emailjs.sendForm("service_t16hr35", "template_x12a01n", this.$refs.form, "_Aybmf8YJu73jv86J")
        .then((result) => {
          console.log('SUCCESS!', result.text);
          this.submitted = true;
          this.clearForm();
        }, (error) => {
          console.log('FAILED...', error.text);
          this.submitted = false;
        });
    },
    clearForm() {
      this.$refs.form.reset();
    }
  }
};
</script>

<style scoped>
@import "./ContactForm.sass";
</style>