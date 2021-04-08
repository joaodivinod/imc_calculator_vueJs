<template>
    <div class="content imc">
        <header>
            <h2>Calculadora de IMC</h2>
        </header>
        <main>
            <section class="genres conainer">
                    <div @click="female = false, male = true" class="genre" :class="{select : male}">
                        <img src="../assets/img/man-icon.svg" alt="">
                        <h3>Homem</h3>
                    </div>

                <div @click="female = true, male = false" class="genre" :class="{select : female}">
                    <img src="../assets/img/female-icon.svg" alt="">
                    <h3>Mulher</h3>
                </div>

            </section>


        </main>
        <footer></footer>
    </div>
</template>

<script>
export default {
    name: "Imc",
    data(){
        return{
            male:false,
            female:false,
        }
    }
}
</script>

<style scoped>
    .imc{
        background-color: #0B0E20;
    }
    .content{
        width: 375px;
        min-height: 600px;
        border-radius: 10px;
        box-shadow: 1px 1px 1px #000;
        margin: auto;
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
    .genres h3{
        color: #8B8C96;
        font-weight: 300;
        font-size: 16px;

    }
    .genres{
        display: flex;
        justify-content: space-between;

    }
    .genre{
        width: 45%;
        background-color: #1D1E33;
        height: 135px;
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
    .genre:hover{
        background-color: #303258;
    }

    .select{
        background-color: #303258;
        border: 2px solid #EB1555;
    }

</style>