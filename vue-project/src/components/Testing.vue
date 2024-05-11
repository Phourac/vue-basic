<template>
  <!-- <p v-bind:style="{ color: 'blue' }" v-if="num === 5">testing</p>
  <p v-show="showElement">V-show</p> -->
  <!-- <p v-for="item in name" :key="item">{{ item }}</p> -->
  <!-- <p v-for="(item, index) in objectArr" :key="index">
    {{ item.name }} {{ item.data[0].age }} {{ item.data[0].sex }}
  </p> -->

  <!-- using list arr with condition
  <template v-for="item in name" key="name">
    <p v-if="item === 'john'">{{ item }}</p>
  </template> -->
  <p>Add method -{{ add(3, 7) }}</p>
  <p>Mutiply method -{{ mutiply() }}</p>
  <p>{{ count }}</p>

  <button v-on:click="increment()">Increment</button>
  <button v-on:click="decrement()">Decrement</button>
</template>

<script>
export default {
  name: "Testing",
  data() {
    return {
      num: 5,
      count: 0,
      //   showElement: true,
      name: ["john", "clark", "batman"],
      objectArr: [
        {
          name: "sok",
          data: [{ age: 10, sex: "male" }],
        },
        {
          name: "kha",
          data: [{ age: 10, sex: "female" }],
        },
      ],
    };
  },

  methods: {
    add(a, b) {
      return a + b;
    },

    mutiply() {
      let local = 10; // defining a local variable
      return 10 * local; // multiplying 10 with the local variable
    },

    increment() {
      return (this.count = this.count + 1);
    },

    decrement() {
      return (this.count = this.count - 1);
    },
  },
};
</script>
