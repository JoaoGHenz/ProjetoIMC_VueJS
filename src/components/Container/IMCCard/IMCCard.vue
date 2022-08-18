<template>
    <div id="IMCCard">
        <TitleComponent content="Calcule seu IMC"/>
        <div class="firstSlide">
            <TextComponent text="Peso"/>
            <input type="range" min="1" max="100" value="50" class="slider" id="myRange">
        </div>
        <div class="secondSlide">
            <TextComponent text="Altura"/>
            <input type="range" min="1" max="100" value="50" class="slider" id="myRange">
        </div>
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
}
}

</script>

<style lang="scss" scoped>

#IMCCard {
    width: 50%;
    height: 50%;
    background: rgba(255, 255, 255, 0.6);
    border-radius: 15px;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-flow: column wrap;
}

</style>