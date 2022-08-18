<template>

    <div>
        <h1 :class="TitleClass" 
        v-if="TitleProp === 'h1'"> {{ content }}</h1>
        <h2 :class="TitleClass" 
        v-if="TitleProp === 'h2'"> {{ content }}</h2>
    </div>

</template>

<script>

export default {
    name: "TitleComponent",
    props: {
        TitleClass: {
            type: String,
        },
        TitleProp: {
            type: String,
            default: "h2"
        },
        content: {
            type: String,
            default: "Title Component"
        }
    }
}

</script>

<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');

h1, h2 {
    font-family: 'Poppins', sans-serif;
    font-weight: 400;
    font-size: 40px;
    line-height: 60px;
}
</style>