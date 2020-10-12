<template>
    <div class="product-form">

        <div class="container">


            <form @submit.prevent="handleSubmit">

                <div class="form-group">
                    <label for="price">PRICE</label>
                    <input v-model="product.price" type="text" class="form-control" id="" aria-describedby="emailHelp" placeholder="price">
                </div>

                <div class="form-group">
                    <label for="exampleInputPassword1">NAME</label>
                    <input v-model="product.name" type="text" class="form-control" id="" placeholder="name">
                </div>

                <div class="form-group">
                    <label for="exampleInputPassword1">AVERAGE</label>
                    <input v-model="product.average" type="text" class="form-control" id="" placeholder="average">
                </div>

                <div class="form-group">
                    <label for="exampleInputPassword1">REVIEWS</label>
                    <textarea v-model="product.reviews" class="form-control" aria-label="With textarea"></textarea>
                </div>

                <button type="submit" class="btn btn-primary">Submit</button>
       
       </form>

    </div>

    </div>
</template>

<script>
export default {
    name:'product-form',
    data(){
        return{
            product:{
                price: '',
                name:'',
                average:'',
                reviews:'',
                image:'',
            }
        }
    },
    methods: {
    handleSubmit() {
      //console.log('form submitted')
      this.$emit('update:product', this.product)
    }
  }
}
</script>