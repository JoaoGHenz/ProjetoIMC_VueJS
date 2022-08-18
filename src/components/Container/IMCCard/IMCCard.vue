<template>
    <div id="IMCCard">
        <TitleComponent content="Calcule seu IMC"
        TitleProp="h1"/>
        <div class="slide">
            <TextComponent text="Peso"/>
            <TextComponent :text="peso"/>
            <input type="range" min="1" max="100" :value="peso" class="slider">
        </div>
        <div class="slide">
            <TextComponent text="Altura"/>
            <TextComponent :text="altura"/>
            <input type="range" min="1" max="100" :value="altura" class="slider">
        </div>
        <TitleComponent content="IMC XXX (PESO PICA)"/>
    </div>
</template>

<script>
import TitleComponent from '@/components/Micro/Title/TitleComponent.vue';
import TextComponent from '@/components/Micro/Text/TextComponent.vue';

export default {
    name: "IMCCard",
    components: {
    TitleComponent,
    TextComponent,
    },
    props: {
    },
    data() {
        return {
            peso: 50,
            altura: 50
        }
    }
}

</script>

<style lang="scss" scoped>

#IMCCard {
    width: 50%;
    height: 60%;
    background: rgba(255, 255, 255, 0.6);
    border-radius: 15px;
    display: flex;
    justify-content: space-around;
    align-items: center;
    flex-flow: column wrap;
}

.slide {
    display: flex;
    flex-flow: column wrap;
    width: 60%;
}

</style>