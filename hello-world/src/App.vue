<template>
<body>
  <div id ="app">
    <div id = "top=bar">
        <h1 class="name"> Rafi's Grocery Store</h1>
    </div>

    <div class="items-image" v-for= "store in store" :key= "store"> 
      <img v-bind:src="image">
  

    </div>
    <div class="items">{{item}}</div>

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
         image:  require("./assets/toast.jpg"),
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
        item: "bagguete.jpg", 
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

</style>
