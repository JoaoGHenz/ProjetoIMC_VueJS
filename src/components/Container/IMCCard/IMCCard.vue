<template>
    <div id="IMCCard">
        <TitleComponent content="Calcule seu IMC"
        TitleProp="h1"/>
        <div class="slide">
            <div class="titleSlide">
                <TextComponent text="Peso"/>
                <TextComponent :text="peso" class="resTexto"/>
            </div>
            <input type="range" min="0" max="100" :value="this.peso" @input="getPeso" class="slider" id="pesoSlider">
        </div>
        <div class="slide">
            <div class="titleSlide">
                <TextComponent text="Altura"/>
                <TextComponent :text="altura" class="resTexto"/>
            </div>
            <input type="range" min="0" max="2.0" :value="this.altura" step="0.01" @input="getAltura" class="slider" id="alturaSlider">
        </div>
        <ButtonComponent :clickButton="calcIMC"/>
        <TitleComponent :content="this.IMCString + this.resultado + this.IMCStringAfter + this.IMCFinal + this.IMCGambiarra"/>
    </div>
</template>

<script>
import TitleComponent from '@/components/Micro/Title/TitleComponent.vue';
import TextComponent from '@/components/Micro/Text/TextComponent.vue';
import ButtonComponent from '@/components/Micro/Button/ButtonComponent.vue';

export default {
    name: "IMCCard",
    components: {
    TitleComponent,
    TextComponent,
    ButtonComponent
},
    props: {
    },
    data() {
        return {
            peso: 50,
            altura: 1.0,
            resultado: "NA",
            IMCString: "IMC ",
            IMCStringAfter: " (",
            IMCGambiarra: ")",
            IMCFinal: "NA"
        }
    },
    methods: {
        getPeso() {
            this.peso = document.getElementById("pesoSlider").value;
            console.log(this.peso);
        },
        getAltura() {
            this.altura = document.getElementById("alturaSlider").value;
            console.log(this.altura);
        },
        calcIMC() {
            let res = this.peso / (this.altura * this.altura)
            this.resultado = res.toFixed(2)
            
            if (this.res <= 18.5) {
                this.IMCFinal = "Abaixo do Peso";
            } else if (this.resultado <= 24.9) {
                this.IMCFinal = "Peso Normal";
            } else if (this.resultado <= 29.9) {
                this.IMCFinal = "Sobrepeso";
            } else if (this.resultado <= 34.9) {
                this.IMCFinal = "Obesidade Grau I";
            } else if (this.resultado <= 39.9) {
                this.IMCFinal = "Obesidade Grau II";
            } else if (this.resultado > 40) {
                this.IMCFinal = "Obesidade Mórbida";
            }
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

    .titleSlide {
        display: flex;
        justify-content: space-between;
    }

    .slider {
        height: 60px;
        background: #FFFFFF;
        border-radius: 4px;
        -webkit-appearance: none;
        height: 25px;;
    }

    .slider::-moz-range-thumb {
        width: 45px;
        height: 45px;
        background: #F7B718;
        border-radius: 100%;
    }
}

</style>