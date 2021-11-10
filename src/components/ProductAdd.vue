<template>
  <div id="addForm">
      <form @submit.prevent="handleAdd">
          <div class="form-group">
              <label for="id">Id</label>
            <input v-model="product.id" type="text" class="form-control" id="id">
          </div>
          <div class="form-group">
              <label for="categoryId">Product Name</label>
            <input v-model="product.categoryId" type="text" class="form-control" id="id">
          </div>
          <div class="form-group">
              <label for="productName">Category</label>
            <input v-model="product.productName" type="text" class="form-control" id="id">
          </div>
          <div class="form-group">
              <label for="quantityPerUnit">Info</label>
            <input v-model="product.quantityPerUnit" type="text" class="form-control" id="id">
          </div>
          <div class="form-group">
              <label for="unitPrice">Price</label>
            <input v-model="product.unitPrice" type="text" class="form-control" id="id">
          </div>
          <div class="form-group">
              <label for="unitsInStock">Stocks</label>
            <input v-model="product.unitsInStock" type="text" class="form-control" id="id">
          </div>
          <button type="submit" class="btn btn-sm btn-success">Add</button>
      </form>
  </div>
</template>
<script>
export default {
    name:'product-add',
    data(){
        return{
            product:{id:'',categoryId:'',productName:'',quantityPerUnit:'',unitPrice:'',unitsInStock:''}
        }
    },
    methods:{
        handleAdd(){
            this.$emit("add:product", this.product)
        }
    }
};
</script>
<style scoped>
#addForm{
    margin: 100px;
}
</style>