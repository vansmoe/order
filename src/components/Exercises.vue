<template>
  <div>
    <button @click="fun4">test</button>
  </div>
</template>

<script>
export default {
  name: "Exercises",
  data() {
    return {
      price: "55",
      orderData: {
        price: "25",
        getPrice: () => this.price,
      },
      employees: [
        { name: "Adam", age: 45 },
        { name: "Tomasz", age: 22 },
        { name: "Aga", age: 27 },
      ],
    };
  },
  methods: {
    getData() {
      return new Promise((resolve, reject) => {
        setTimeout(() => {
          resolve("data");
          reject("error");
        }, 1500);
      });
    },
    fun1() {
      //  get data here
      this.getData().then((res) => {
        console.log(res);
        console.log("log after data fetch");
      });
    },
    fun2() {
      console.log(this.orderData.getPrice());
    },
    fun3() {
      const data = this.employees
        .map((e) => {
          e.age *= 2;
          return e;
        })
        .filter((e) => e.age > 50);
      console.log(data);
    },
    fun4() {
      let i = 1;
      for (let i = 0; i < 10; i++) {
        i = 10
      }
      console.log(i);
    },
    fun5() {
      let x;
      console.log(x);
      x = 1;
    },
    fun6() {
      console.log(0 == false);
    },
    fun7() {
      console.log(null == undefined);
    },
    fun8() {
      console.log("0" === 0);
    },

    fun9() {
      console.log(2 + 4 + "1");
    },
  },
};
</script>

<style>
</style>