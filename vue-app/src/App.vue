<template>
  <div id="app" class="small-container">

    <product-page :products="products" />
    <product-form @update:product="addProduct" />
  </div>
</template>

<script>

import ProductPage from '@/components/ProductPage.vue'
import ProductForm from '@/components/ProductForm.vue'

export default {
  name: 'App',
  components: {
    ProductPage,
    ProductForm
  },
  data(){
    return {
      products: [
                {
          "price": "$13.99",
          "name": "Blue Moon Belgian White Belgian-Style Wheat Ale",
          "rating": {
            "average": 4.775260833383482,
            "reviews": 305
          },
          "image": "https://www.totalwine.com/media/sys_master/twmmedia/he8/h67/11931543830558.png"
        }, {
          "price": "$16.99",
          "name": "Guinness Extra Stout",
          "rating": {
            "average": 3.9785961474594638,
            "reviews": 119
          },
          "image": "https://www.totalwine.com/media/sys_master/twmmedia/h50/h90/11996630056990.png"
        }, {
          "price": "$8.99",
          "name": "Guinness Extra Stout",
          "rating": {
            "average": 3.5135460961961718,
            "reviews": 199
          },
          "image": "https://www.totalwine.com/media/sys_master/twmmedia/h35/he7/11996577726494.png"
        },
      ]
    }
  },
  methods: {
  add(employee) {
    this.employees = [...this.employees, employee]
  }
}
}
</script>

<style>
body {
  background-color: #202329;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
  color:white;
}


</style>
