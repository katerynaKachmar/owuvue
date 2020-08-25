<template>
  <div>
    <div>
      <input type="text" v-model="item">
      <button @click="add()" v-if="toDoList.length<10">add</button>

      <ul>
        <li v-for="(item, index) in toDoList" :key="index">{{item}}
          <button @click="remove(index)">remove</button>

        </li>

      </ul>
    </div>

  </div>

</template>

<script>


export default {
  name: 'App',
  data() {
    return {
      toDoList: ['sleep', 'eat', 'home work'],
      item: ''
    }

  },
  computed: {

  },
  methods: {
    add() {
      this.toDoList.push(this.item),
      this.item = ''
    },
    remove(index) {
      this.toDoList.splice(index, 1)

    }



  }


}
</script>

<style>

</style>
