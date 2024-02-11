<template>
  <div>
    <h1>To-Do</h1>
    <form>
      <input type="text">
    </form>
    <ul>
      <li v-for="(item, index) in list" :key="index">{{ item }}</li>
    </ul>
  </div>

  <script>
    export default{
      data:function(){
        return{
          list: [
            {
              title: "menyapu"
            },
            {
              title: "cuci piring"
            },
            {
              title: "pel"
            },
          ],
          input: ""
        }
      },
      mounted() {
        console.log("Component mounted.")
      },
    }
  </script>
</template>