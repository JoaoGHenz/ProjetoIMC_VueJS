<template>
  <button v-on:click="clickButton">Calcular</button>
</template>

<script>

export default {
    name: "ButtonComponent",
    props: {
        clickButton: {
            type: String,
        }
    }
}

</script>

<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');

button {
    background: #F7B718;
    border-radius: 4px;
    width: 60%;
    box-sizing: border-box;  
    height: 60px;
    font-family: 'Poppins';
    font-family: 'Poppins';
    font-style: normal;
    font-weight: 300;
    font-size: 30px;
    line-height: 45px;
    color: #FFFFFF;
}

</style>