<template>
<body>
  <div id ="app">
    <div id = "top=bar">
        <h1 class="name"> Rafi's Grocery Store</h1>
    </div>

    <div class="items-image" v-for="store in store"> 
      <img :src="image">
  

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

      }
  


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
