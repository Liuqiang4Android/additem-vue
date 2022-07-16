<template>
  <div class="hello">
    <ul>
      <li
        v-for="(num,index) in nums"
        :key="index"
      >
      {{num}}
      {{index}}
      <button @click="remove(index)">删除</button>
      </li>
    </ul>
    <button @click="add()">生成</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  // props: {
  //   msg: String
  // },
  data(){
    return {
      nums:[Math.floor(Math.random()*100),Math.floor(Math.random()*100)]
    }
  },
  methods:{
    remove(index) {
      console.log(index)
        this.nums.splice(index,1)
  },
  add(){
    let newnum=Math.floor(Math.random()*100)
    console.log(newnum)
    this.nums.push(newnum)
  }
}
}
</script>

<style scoped>

</style>
