<template>
        <div class="main">
            <h1 class="display-4">Semua Produk</h1>
            <table class="table table-hover">
                <thead>
                    <tr>
                        <th scope="col">Name</th>
                        <th scope="col">Description</th>
                        <th scope="col">Stock</th>
                        <th scope="col">Price</th>
                        <th scope="col"></th>
                    </tr>
                </thead>
                <tbody>
                    <ProductListItem v-for="productItem in productItems" :key="productItem.id" :productItem="productItem"/>
                </tbody>
            </table>
        </div>
</template>

<script>
import { mapGetters } from 'vuex';
import ProductListItem from './Product_List_Item.vue'

export default {
  name: "ProductList",
  components:{
      ProductListItem
  },
  components: {
    ProductListItem
  },
  computed: {
    ...mapGetters([
      'productItems'
    ])
  },
  
 
};
</script>
<style scoped>
.main{
    max-width: 80%;
}
</style>