<template>
  <div>
    <h1>To-Do</h1>
    <form>
      <input type="text" v-model="input">
      <button type="button" @click="addList">Submit</button>
    </form>
    <ul>
      <li v-for="(item, index) in list" :key="index">{{ item.title }}</li>
    </ul>
  </div>
</template>

<script>
export default{
  data:function(){
    return{
      list: [
        {title: "menyapu"},
        {title: "cuci piring"},
        {title: "pel"},
      ],
      input: ""
    }
  },
  mounted() {
    console.log("Component mounted.")
  },
}
</script>