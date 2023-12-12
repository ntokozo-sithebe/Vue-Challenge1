<template>
  <div class="wrapper">
  <input class="search" placeholder="Search for a product" type="text" >
  <button>categories</button>
    <div class="row" v-if="products.length">
      <div class="prodCard" v-for="product in products" :key="product.id">
      <div class="card-hearder">
        <h2>{{ product.productType }}</h2>
        </div>
        <div class="card-body">
          <img :src="product.image" :alt="product.description" loading="lazy">
          <p>R{{ product.Price }}</p>
        </div>
        <div class="card-footer">
          <a href="" type="button"> View products </a>
        </div>
      </div>
    </div>
    <div v-else>
      <h4> Products are sold out </h4>
    </div>
</div>



  
</template>

<script>
export default {
  name: 'App',
  components: {},
  data(){
    return{
      products:[
      {
        id: "1",
        productType: "Cream",
        Price: 450,
        description: "Used day and night",
        image:
          " https://i.postimg.cc/zvbhjbnh/cream-stylized-product-opt-540x.webp",
      },
      {
        id: "2",
        productType: "Cleanser",
        Price: 550,
        description: "Used day and night",
        image: "https://i.postimg.cc/xC0qsszM/goji-berry-clenser-opt-900x.webp",
      },
      {
        id: "3",
        productType: "Vitamin C Serum",
        Price: 560,
        description: "Used day and night",
        image:
          "https://i.postimg.cc/3NbX9pCC/vitamin-c-serum-stylized-2-opt-900x.webp",
      },
      {
        id: "4",
        productType: "Deep Eye Therapy",
        Price: 680,
        description: "Used day and night",
        image:
          "https://i.postimg.cc/zvtQKHL7/eye-complex-stylized-optimized-900x.webp",
      },
      {
        id: "5",
        productType: "Toner",
        Price: 750,
        description: "Used day and night",
        image:
          "https://i.postimg.cc/3rgfvK3c/white-tea-toner-stylized-opt-720x-no5.jpg",
      },
      {
        id: "6",
        productType: "Fine SKN All in One",
        Price: 7750,
        description: "Used day and night",
        image: "https://i.postimg.cc/Z5r9q8vr/all-5.webp",
      },
    ]
    }
  },
  computed:{
    categories(){
      this.products.id;this.product.productType;this.product.image;this.product.description;this.product.Price
      return{
        
      }

    },

    },
    // methods:{
    //    onclick(){
    //      If(product);{
    //        products.filter((product)=> {
    //          return this.productType
    //        })
    //      }

    //    }
    
    // }
  }
  
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.row :is(.row) {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}
.prodCard {
  width: 18rem;
}
.card-body :is(>*, img){
  width: 100%;
  aspect-ratio: 1/1;
}








</style>
