<template>

    <div id="product-page">
        <div class="container">
            <h1>products</h1>
            <table class="table">
            <thead>
                <tr>
                    <th>PRICE</th>
                    <th>NAME</th>
                    <th>AVERAGE</th>
                    <th>REVIEWS</th>
                    <th>IMAGE</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="product in products" :key="product.id">
                <td>{{ product.price }}</td>
                <td>{{ product.name }}</td>
                <td>{{ product.rating.average }}</td>
                <td>{{ product.rating.reviews }}</td>
                <td><img :src="product.image"></td>
                </tr>
            </tbody>
            </table>
        </div>
    </div>
</template>

<script>
export default {
    name: 'product-page',
    props:{
        products: Array,
    }
}
</script>

<style scoped>

</style>