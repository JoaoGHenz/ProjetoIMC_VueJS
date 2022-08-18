<template>

    <p>
        {{ text }}
    </p>

</template>

<script>

export default {
    name: "TextComponent",
    props: {
        text: {
            String,
            default: "Text Component"
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

</style>