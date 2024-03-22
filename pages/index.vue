<template>
    <div class="main">
        <Header/>
        
        <div class="modal">
            <BaseButton to="/shop" class="modal-button"/>
        </div>

        <Banner/>

        <div class="best-sellers">
            <h2 class="best-sellers__title">best sellers</h2>
            <div class="product-cards">
                <div class="product-card">
                    <img src="/Header/macroons.jpg" alt="" class="product-photo">
                    <BaseButton class="product-button">Add to Cart</BaseButton>
                </div>
                <div class="product-card">
                    <img src="/Header/macroons.jpg" alt="" class="product-photo">
                    <BaseButton class="product-button">Add to Cart</BaseButton>
                </div>
                <div class="product-card">
                    <img src="/Header/macroons.jpg" alt="" class="product-photo">
                    <BaseButton class="product-button">Add to Cart</BaseButton>
                </div>
                <div class="product-card">
                    <img src="/Header/macroons.jpg" alt="" class="product-photo">
                    <BaseButton class="product-button">Add to Cart</BaseButton>
                </div>
                <div class="product-card">
                    <img src="/Header/macroons.jpg" alt="" class="product-photo">
                    <BaseButton class="product-button">Add to Cart</BaseButton>
                </div>
            </div>
        </div>

        <div class="decoration-block">
            Menu
        </div>

        <div v-for="product in data">
            {{ product.id }}
        </div>

        
        <Footer/>
    </div>
</template>

<script setup>
    const { data } = await useFetch('https://fakestoreapi.com/products');
    console.log(data);
</script>

<style>
@import 'normalize.css/normalize.css';
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@100..900&display=swap');
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Montserrat', sans-serif;
}
.main {
    width: 100%;
    background-color: white;
}
.modal{
    margin-top: 140px;
    display: flex;
    justify-content: center;
    align-items: flex-end;
    width: 100%;
    /* height: calc(100dvh - 140px); */
    height: 700px;
    background: center url(https://food-images.files.bbci.co.uk/food/recipes/fruit_tarts_45402_16x9.jpg);
    background-size: cover;
}
.modal-button{
    text-decoration: none;
    margin-bottom: 100px;
}
.best-sellers{
    padding-bottom: 100px;
}
.best-sellers__title{
    font-size: 35px;
    color: #636363;
    margin: 40px;
    text-align: center;
}
.product-cards{
    width: 100%;
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    padding: 0 20px;
}
.product-card{
    width: 350px;
    height: 400px;
    background-color: #1edce9;
    margin: 10px 10px;
    border-radius: 50px;
    display: flex;
    flex-direction: column;
    align-items: center;
}
.product-photo{
    margin-top: 40px;
    width: 200px;
    height: 200px;
}
.product-button{
    margin-top: 50px;
}
.decoration-block{
    width: 100%;
    background-color: #EF3F75;
    color: white;
    font-weight: 700;
    font-size: 24px;
    padding: 20px;
}

</style>
