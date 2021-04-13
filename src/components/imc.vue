<template>
    <div class="content imc">
        <header>
            <h2>Calculadora de IMC</h2>
        </header>
        <main>
            <section class="genres container">
                <div @click="genre= 'male' " class="genre" :class="{select : genre === 'male'}">
                    <img src="../assets/img/man-icon.svg" alt="">
                    <h3>Homem</h3>
                </div>
                <div @click="genre= 'female' " class="genre" :class="{select : genre === 'female'}">
                    <img src="../assets/img/female-icon.svg" alt="">
                    <h3>Mulher</h3>
                </div>
            </section>
            <section class="height container">
                <div>
                    <h2>{{height}}</h2>
                    <h3>cm</h3>
                </div>
                <RangeSlider
                    class="slider"
                    min="100"
                    max="230"
                    step="1"
                    v-model="height">
                </RangeSlider>
            </section>
            <section class="status container">
                <div class="info">
                    <h3>Peso</h3>
                    <h2>{{weight}}</h2>
                    <div class="crtl-btn">
                        <button @click="weight -=1">-</button>
                        <button @click="weight +=1">+</button>
                    </div>
                </div>
                <div class="info">
                    <h3>idade</h3>
                    <h2>{{age}}</h2>
                    <div class="crtl-btn">
                        <button @click="age -=1">-</button>
                        <button @click="age +=1">+</button>
                    </div>
                </div>
            </section>
            <section class="result container">
                <h3>Resultado</h3>
                <h2>{{ calcImc() }}</h2>
                <h3>Seu peso esta acima do peso normal</h3>
            </section>
        </main>

        <footer>
           <div class="container">
               <p>Desenvolvido por : </p> <img src="../assets/img/github-icon.svg" alt=""> <a href="#">João Divino</a>
           </div>
        </footer>
    </div>
</template>

<script>
import RangeSlider from 'vue-range-slider'
import 'vue-range-slider/dist/vue-range-slider.css'
export default {
    name: "Imc",
    components: {RangeSlider},
    data(){
        return{
            genre:'female',
            height:0,
            weight:60,
            age:15,
            result :0
        }
    },
    methods:{
       calcImc(){

       }
    }

}
</script>

<style scoped>
header{
    margin-bottom: 20px;
}
main{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    height: 100%;
}
footer{
    background: #111328;
    border-top-right-radius: 10px;
    border-top-left-radius: 10px;
    height: 60px;
    display: flex;
    margin-top: 20px;
}
footer a{
    color: #fff;
    text-decoration: none;
}
footer div{
    max-width: 270px;
    display: flex;
    padding: 10px 5px;
    justify-content: space-between;
    align-items: center;
    color: #fff;
    font-weight: 300;
    font-size: 16px;
    text-align: center;
}
footer div img {
    width: 25px;
    margin-left: 10px;
    margin-right: 8px;
}

.imc{
    background-color: #0B0E20;
}
.content{
    width: 414px;
    height: 736px;
    border-radius: 10px;
    box-shadow: 1px 1px 1px #000;
    margin: auto;
    display: flex;
    flex-direction: column;
}
.imc header{
    border-top-right-radius: 10px;
    border-top-left-radius: 10px;
    height: 60px;
    display: flex;
    align-items: center;
    padding-left: 20px;
    background-color: #111328;

}
.imc header h2{
    color: #fff;
    font-size: 22px;
    font-weight: 500;

}
.genres h3, .status h3, .result h3{
    color: #8B8C96;
    font-weight: 300;
    font-size: 16px;

}
.genre img{
    height:50%;
}
.genres, .status{
    display: flex;
    justify-content: space-between;
}
.genre, .info{
    width: 45%;
    background-color: #1D1E33;
    height: 120px;
    border-radius: 12px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-direction: column;
    padding: 20px 0;
    cursor: pointer;
    transition: 300ms;
    border: 2px solid #1D1E33;
}
.info{
    padding: 7px 0;
}
.genre:hover{
    background-color: #303258;
}

.select{
    background-color: #303258;
    border: 2px solid #EB1555;
}
.height, .result{
    background-color: #1D1E33;
    border-radius: 12px;
    height: 130px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}
.height div{
    display: flex;
    margin-bottom: 10px;
}
.height h2, .info h2, .result h2{
    color: #fff;
    font-size: 45px;
    font-weight: 500;
    margin-right: 7px;
}
.result h2{
    margin:10px 0;
}
.height h2{
    margin-top: -17px;
}
.height h3{
    color: #8B8C96;
    font-size: 22px;
    font-weight: 300;
    margin-top: auto;
    margin-bottom: 10px;
}
.crtl-btn{
    width: 46%;
    display: flex;
    justify-content: space-between;
}
.crtl-btn button{
    width:27px;
    height: 27px;
    background-color: #4C4F5E;
    border-radius: 50%;
    color: #fff;
    border: none;
    font-weight: 500;
    font-size: 20px;
    cursor: pointer;
}

</style>