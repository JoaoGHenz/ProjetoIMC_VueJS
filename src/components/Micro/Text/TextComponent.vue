<template>

    <p :class="textoClass">
        {{ text }}
    </p>

</template>

<script>

export default {
    name: "TextComponent",
    props: {
        text: {
            type: String,
            default: "Text Component"
        },
        textoClass: {
            type: String,
        }
    }
}

</script>

<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');

p {
    font-family: 'Poppins';
    font-style: normal;
    font-weight: 300;
    font-size: 24px;
    line-height: 36px;
    margin: 0;
}

.resTexto {
    color: #F7B718;
    font-style: normal;
    font-weight: 300;
    font-size: 40px;
    line-height: 60px;
}

</style>