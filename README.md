# Animação Dock Header com scroll Elementor
CSS no Header
````
.custom-header {
    width: 100%;
    position: fixed;
    top: 0;
    left: 50%; /* Centraliza horizontalmente */
    transform: translateX(-50%); /* Garante que fique centralizado desde o início */
    z-index: 9999;
    transition: all 0.3s ease-in-out;
}

.custom-header.scrolled {
    width: 800px; /* Reduz a largura quando rolar */
    border-radius: 150px;
    margin-top: 20px;
    /* Nenhuma mudança no left ou transform, o header permanece centralizado */
}
````
JS no Custon Code do Elementor

````
<script>
jQuery(window).on("scroll", function() {
    if (jQuery(window).scrollTop() > 30) {
        jQuery(".custom-header").addClass("scrolled");
    } else {
        jQuery(".custom-header").removeClass("scrolled");
    }
});
</script>
````
