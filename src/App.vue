<script setup></script>

<!-- <template >
  <div> -->
<!-- <body class="container-lg mx-10 my-10 bg-gray-600">
    <div class="text-3xl font-arial bg-red-600 flex border-8 border-green-500 justify-between items-center"
      style="color: black !important">
  <div class="pl-4">Invoices</div>
  <div class="pr-4 pl-2 bg-blue-600 ">New Invoice</div>
    </div>
  </body> -->

<!-- <nav class="flex items-center justify-between flex-wrap bg-gray-800 p-6">
    <div class="flex items-center mr-6">
      <img src="./assets/images/logo.png" alt="Logo" class="h-6">
    </div>
    <div class="w-full block flex-grow lg:flex lg:items-center lg:w-auto">
      <div class="text-sm lg:flex-grow">
        <a href="#responsive-header" class="block mt-4 lg:inline-block lg:mt-0 text-white hover:text-gray-200 mr-4">
          Home
        </a>
        <a href="#responsive-header" class="block mt-4 lg:inline-block lg:mt-0 text-white hover:text-gray-200 mr-4">
          About
        </a>
        <a href="#responsive-header" class="block mt-4 lg:inline-block lg:mt-0 text-white hover:text-gray-200">
          Contact
        </a>
      </div>
    </div>
  </nav> -->

<!-- <template >
  <div>
    <div class="bg-gray-300 ">
      <div class="container w-full bg-green-300 mx-auto px-0 lg:px-0" :class="containerPieces">
        <header class="bg-gray-500 text-white py-5 lg:py-10" :class="containerPieces">
          <h1 class="text-center text-xl font-bold text-red-300 lg:text-3xl">My Website</h1>
        </header>
        <main class="py-8 lg:py-12" :class="containerClasses">
          <p class="text-lg mx-5 lg:text-2xl" :class="containerPieces">Lorem ipsum dolor sit amet, consectetur adipiscing
            elit. Nulla imperdiet
            commodo
            ex, vitae luctus orci maximus id. Donec vitae nulla fermentum, cursus mauris eu, viverra nisl. Phasellus at
            mauris tortor. Proin pellentesque purus ac neque gravida, non suscipit augue ultricies. Vivamus pulvinar
            euismod
            turpis, a faucibus nisl fermentum ut.</p>

        </main>
        <footer class="bg-gray-500 text-white py-5 lg:py-8" :class="containerPieces">
          <button class="bg-blue-500 hover:bg-blue-800 hover:text-green-400 font-bold py-2 px-4 mx-2 rounded"
            @click="changeColor">test
            me</button>
        </footer>
      </div>
    </div>
  </div>
</template> -->

<template>
  <!-- <input v-model="num1" type="number" placeholder="num 1" />
  <input v-model="num2" type="number" placeholder="num 2" /> -->
  <div class="bg-gray-700 h-screen">
    <div class="flex flex-wrap">
      <!-- <br />
      num1 =>{{ num1 }}
      <br />
      num2 =>{{ num2 }}
      <br />
      res => {{ result }} -->
      <div
        v-for="(item, index) in selected"
        class="w-1/4 border border-gray-500 text-center py-2"
        :class="item"
        style="padding-top: 5%; padding-bottom: 5%"
      >
        {{ index + 1 }}
      </div>
      <!-- <div class="w-1/4  border border-gray-500 text-center py-2 " :class="selected.length > 0 ? selected[0] : 'bg-red-300'"
  style=" padding-top: 5%; padding-bottom: 5%;">1</div> -->
      <!-- <div class="w-1/4  border border-gray-500 text-center py-2 bg-blue-300" :class="selected[1]"
    style=" padding-top: 5%; padding-bottom: 5%;">2</div>
  <div class="w-1/4  border border-gray-500 text-center py-2 bg-green-300" :class="selected[2]"
    style=" padding-top: 5%; padding-bottom: 5%;">3</div>
  <div class="w-1/4  border border-gray-500 text-center py-2 bg-yellow-300" :class="selected[3]"
    style=" padding-top: 5%; padding-bottom: 5%;">4</div>
  <div class="w-1/4  border border-gray-500 text-center py-2 bg-green-300" :class="selected[4]"
    style=" padding-top: 5%; padding-bottom: 5%;">5</div>
  <div class="w-1/4  border border-gray-500 text-center py-2 bg-pink-300" :class="selected[5]"
    style=" padding-top: 5%; padding-bottom: 5%;">6</div>
  <div class="w-1/4  border border-gray-500 text-center py-2 bg-orange-300" :class="selected[6]"
    style=" padding-top: 5%; padding-bottom: 5%;">7</div>
  <div class="w-1/4  border border-gray-500 text-center py-2 bg-teal-300" :class="selected[7]"
    style=" padding-top: 5%; padding-bottom: 5%;">8</div>
  <div class="w-1/4  border border-gray-500 text-center py-2 bg-orange-300" :class="selected[8]"
    style=" padding-top: 5%; padding-bottom: 5%;">9</div>
  <div class="w-1/4  border border-gray-500 text-center py-2 bg-yellow-300" :class="selected[9]"
    style=" padding-top: 5%; padding-bottom: 5%;">10</div>
  <div class="w-1/4  border border-gray-500 text-center py-2 bg-cyan-300" :class="selected[10]"
    style=" padding-top: 5%; padding-bottom: 5%;">11</div>
  <div class="w-1/4  border border-gray-500 text-center py-2 bg-emerald-300" :class="selected[11]"
    style=" padding-top: 5%; padding-bottom: 5%;">12</div> -->
    </div>
    <div class="flex justify-center items-center py-10">
      <button
        class="bg-blue-500 hover:bg-blue-800 hover:text-green-400 font-bold px-6 py-1 m-9 rounded"
        @click="changeColor"
        style="padding-top: 2%; padding-bottom: 2%"
      >
        test me
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      // num1: 10,
      // num2: 0,
      colors: [
        "bg-green-300",
        "bg-yellow-300",
        "bg-red-300",
        "bg-pink-300",
        "bg-orange-300",
        "bg-cyan-300",
        "bg-emerald-300",
      ],
      // "count": 0
      selected: [
        "bg-emerald-300",
        "bg-red-300",
        "bg-orange-300",
        "bg-pink-300",
        "bg-cyan-300",
        "bg-emerald-300",
        "bg-green-300",
        "bg-pink-300",
        "bg-pink-300",
        "bg-emerald-300",
        "bg-pink-300",
        "bg-red-300",
      ],
    };
  },
  computed: {
    result() {
      return this.num1 + this.num2;
    },
  },
  methods: {
    changeColor() {
      this.selected = [];
      Array(12)
        .fill(1)
        .map((i) => {
          let randomness = Math.floor(Math.random() * 7);
          this.selected.push(this.colors[randomness]);
        });
      // let randomness1 = Math.floor(Math.random() * 7)
      // this.selected[0] = this.colors[randomness1]
      // let randomness2 = Math.floor(Math.random() * 7)
      // this.selected[1] = this.colors[randomness2]
      // let randomness3 = Math.floor(Math.random() * 7)
      // this.selected[2] = this.colors[randomness3]
      // let randomness4 = Math.floor(Math.random() * 7)
      // this.selected[3] = this.colors[randomness4]
      // let randomness5 = Math.floor(Math.random() * 7)
      // this.selected[4] = this.colors[randomness5]
      // let randomness6 = Math.floor(Math.random() * 7)
      // this.selected[5] = this.colors[randomness6]
      // let randomness7 = Math.floor(Math.random() * 7)
      // this.selected[6] = this.colors[randomness7]
      // let randomness8 = Math.floor(Math.random() * 7)
      // this.selected[7] = this.colors[randomness8]
      // let randomness9 = Math.floor(Math.random() * 7)
      // this.selected[8] = this.colors[randomness9]
      // let randomness10 = Math.floor(Math.random() * 7)
      // this.selected[9] = this.colors[randomness10]
      // let randomness11 = Math.floor(Math.random() * 7)
      // this.selected[10] = this.colors[randomness11]
      // let randomness12 = Math.floor(Math.random() * 7)
      // this.selected[11] = this.colors[randomness12]

      // console.log(this.selected);

      //   if (this.count % 2 === 0) {
      //     this.backgroundColor = 'bg-green-500';
      //     this.count = this.count + 1
      //   } else if (this.count % 3 === 0) {
      //     this.backgroundColor = 'bg-indigo-500'
      //     this.count = this.count + 1
      //   } else {
      //     this.backgroundColor = 'bg-yellow-500'
      //     this.count = this.count + 1
      //   }
      //   console.log(this.count)
      // },
    },
  },
};
</script>
