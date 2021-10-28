<template>
<body>
  <div id ="app">
    <div id = "top=bar">
        <h1 class="name"> Rafi's Grocery Store</h1>
    </div>
    <div class="whole-container" v-for="product in store" :key="product">

    <div class="items-image"> 
      <h2>{{product.item}}</h2>
  <img class="actual-image" :src="image">
  
  

    </div>
    <div class="items"></div>

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
         item: "toast",
         price: 3 ,
         image:  require("./assets/"),
      },{
        item: "cheese", 
        price: 5,
        image: require("./assets/cheese.jpg")

      }, 
      {
        item: "ice-cream",
        price: 6, 
        image: require("./assets/ice-cream.jpg")
      },{
        item: "bagguete", 
        price: 10, 
        image: require("./assets/bagguete.jpg")

      }, {
        item: "milk", 
        price: 5, 
        image: require("./assets/milk.jpg")
      }, {
        item: "yogurt", 
        price: 20, 
        image: require("./assets/strawberry-yogurt.jpg")
      },
 


      ]
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
  background-color:#96C6ED;
  opacity: 1;
  color: black;
  font-family: 'Courier New', Courier, monospace;
  font-weight: bold;
  font-size: 2.5rem;
  border-radius: 1rem;
  border: solid .2rem #BD8775;
 
}

.item {
  display: inline ;

}
.items-image{
  display: inline;
  color: white;
  background-color: white;
  font-family: 'Courier New', Courier, monospace;
  font-weight: 900;

}

</style>
