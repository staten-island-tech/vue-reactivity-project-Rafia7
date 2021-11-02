<template>
<body>
  <div id ="app">
    <div id = "top=bar">
        <h1 class="name"> Rafi's Grocery Store</h1>
    </div>
    <div class="total-amount" v-for="total in totals" :key="total" >
     $ {{total.total}}
       </div>
    <div class="whole-container" v-for="product in store" :key="product">

    <div class="items-image"> 
      <h2 class="product-name">{{product.item}}</h2>
  <img class="actual-image" :src="product.image">
  <div class="price">
   <p class="price-sub"> Price: ${{product.price}}</p> 
   <button class="buy"  v-on:click ="addToTotal">
    Buy 

   </button>


    </div>
  
  

    </div>

    </div>
  </div>

</body>
 
</template>
<script>
export default {
  name:"App", 
  data(){
    return{
      store: [{
         item: "Toast",
         price: 3 ,
         image:  require("./assets/toast.jpg"),
      },{
        item: "Cheese", 
        price: 5,
        image: require("./assets/cheese.jpg")

      }, 
      {
        item: "Ice-cream",
        price: 6, 
        image: require("./assets/ice-cream.jpg")
      },{
        item: "Bagguete", 
        price: 10, 
        image: require("./assets/bagguete.jpg")

      }, {
        item: "Milk", 
        price: 5, 
        image: require("./assets/milk.jpg")
      }, {
        item: "Yogurt", 
        price: 20, 
        image: require("./assets/strawberry-yogurt.jpg")
      },
      ], 

      totals: [{
        total: 0,
      }],
      methods:[{
        addToTotal: function (){
          this.totals += 1
        }
      }]
     
    }
  }
}





/*import AppVue from "../../my-project/src/App.vue";

const app = new AppVue({
  el: "app",
  data: {
    item: "toast",

  }
})*/

</script>

<style>
html,
body {
  display: flex;
  justify-content: center;
  font-family: 'Courier New', Courier, monospace;
  box-sizing: border-box;
  padding: 0;
  margin: 0;
  background-color: #0C6E63;
  color: black;
  font-weight: 500;
}
.name {
  background-color: blanchedalmond;
  opacity: 1;
  color: black;
  font-family: 'Courier New', Courier, monospace;
  font-weight: bold;
  font-size: 2.5rem;
  border-radius: 1rem;
  border: solid .2rem #BD8775;
  padding-left: 1rem;
  padding-right: 1rem ;
 
}

.item {
  display: inline ;

}
.items-image{
  display: inline;
  color: white;
  font-family: 'Courier New', Courier, monospace;
  font-weight: 900;
  text-align: center;


}
.actual-image{
  width: 20rem;
  border: solid .2rem #BD8775;
  border-radius: 2rem;
}

.whole-container {
  display: flex;
  align-items: center;
}
.buy{
  border-radius: 2rem ;
  border: solid .2rem black ;
  color: #BD8775;
  font-size: 2rem;
  background-color: white;
  opacity: .7;
}

.buy:hover{
  transform: scale(1.2);
  transition: all .7s;
  cursor: pointer;
}

.product-name{
  font: 900;
  font-size: 2.5rem;
  font-family: 'Courier New', Courier, monospace;
}
.price-sub{
  color: yellow;
  font-family: 'Courier New', Courier, monospace;
  font-size: 1.5rem;
  }

  .total-amount{
    color: white;
    text-align: center;
    display: flex;
    flex-direction: row-reverse;
    font-family: 'Courier New', Courier, monospace;
    font-size: 1.5rem;
  }
</style>
