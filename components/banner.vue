<template>
    <div class="banner">
        <BaseButton to="/shop" class="banner-button"/>
    </div>
</template>

<script>
	export default {
		name: "Banner",
		methods: {
		}
	}	
</script>

<style scoped>
	.banner{
    display: flex;
    justify-content: center;
    align-items: flex-end;
    width: 100%;
    height: 500px;
    background: center url(https://www.cupcakeskent.co.uk/wp-content/uploads/2021/09/AdobeStock_315308340-scaled-1200x300.jpeg);
    background-size: cover;
}
    .banner-button{
        text-decoration: none;
        margin-bottom: 40px;
    }
</style>