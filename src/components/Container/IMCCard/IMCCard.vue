<template>
    <div id="IMCCard">
        <TitleComponent content="Calcule seu IMC"/>
    </div>
</template>

<script>
import TitleComponent from '@/components/Micro/Title/TitleComponent.vue';

export default {
    name: "IMCCard",
    components: {
    TitleComponent,
}
}

</script>

<style lang="scss" scoped>

#IMCCard {
    width: 50%;
    height: 50%;
    background: rgba(255, 255, 255, 0.6);
    border-radius: 15px;
}

</style>