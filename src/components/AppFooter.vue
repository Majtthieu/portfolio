<template>
    <footer>
        <div class="footer-icons">
            <a href="https://github.com/Majtthieu" target="_blank"><img src="@/assets/images/icos/github.svg"
                    class="footer-icons_icon" alt="icone Github" /></a>
            <a href="https://www.linkedin.com/in/matthieu-jankowiak" target="_blank"><img
                    src="@/assets/images/icos/linkedin.svg" class="footer-icons_icon" alt="icone Linkedin" /></a>
            <img src="@/assets/images/icos/mail.svg" class="footer-icons_icon" @click="$router.push('/contact')"
                alt="icone email" />
        </div>
        <div class="footer-copyright">
            <p>Matthieu Jankowiak - 2024</p>
        </div>
    </footer>
</template>

<style>
@import "./AppFooter.sass";
</style>
