<template>
  <!-- <div>
    <h1 v-once>{{message}}</h1>
    <h2>{{age * 2}}</h2>
    <p>{{sayHello()}}</p>
    <p>
      <a v-bind:href='link'>Google</a>
    </p>
    <span v-html="finishedLink"></span>
  </div> -->

  <!-- <div>
    <button v-on:click="increase(2)">Click Me!</button>
    <p>{{counter}}</p>
    <p>{{counter < 10 ? 'Greater than 10' : 'Smaller than 10'}}</p> -->
  <!-- <p v-on:mousemove='updateCoordinates'>
    Coordinates: {{x}} {{y}}
    <span v-on:mousemove.stop>DEAD SPOT</span>
    </p>

    <input type="text" v-on:keyup.enter='alert'> -->
  <!-- </div> -->

  <!-- <button v-on:click="increase">Click Me!</button> -->
  <!-- <div>

    <input type="text" v-model="fullName.name">
    <input type="text" v-model="fullName.surname">
    <p>{{fullName.name}} {{fullName.surname}}</p>
  </div> -->

<!-- <div>
  <button v-on:click='increase'>Increase</button>
  <button v-on:click='decrease'>Decrease</button>
  <button v-on:click='counter++'>Increase</button>
  <button v-on:click='counter--'>Decrease</button>
  <button v-on:click='secondCounter++'>Increase Second</button>

  <p>{{newOutput}}</p>
  <p>counter: {{counter}} | {{secondCounter}}</p>
  <p>result: {{result()}} | {{output}}</p>
  <div class="demo" @click="attachedRed = !attachedRed"></div>
  <div class="demo" :class="divClass"></div>
  <div class="demo" :class="color"></div>

  <input type="text" v-model="color">
</div> -->

<!-- <div>
<div v-show="show"></div>

  <p v-if="show">You can see me!</p>
  <p v-else>You can't see me</p>
  <button @click="show = !show">Show</button>
</div> -->

<!-- <div>
  <ul>
    <li v-for="(ingredient, index) in ingredients" :key="`${ingredient} - ${index}`">
      {{ingredient}}
    </li>
    <button @click="ingredients.push('salt')">add salt</button>
  </ul> 
</div> -->

<!-- <div>
  <ul>
    <li v-for="(person, index) in persons" :key="`${person} - ${index}`">
     {{index + 1}} . {{person.name}} - {{person.age}}
    </li>
  </ul> 
</div> -->

<!-- <div>
  <li v-for="(n, i) in 10" :key="i">
    {{n}}
  </li>
</div> -->


<div>
  <ul>
    <li v-for="(person, i) in persons" :key="i">
      <div v-for="(value, key, index) in person" :key="index">
        {{value}}: {{key}}: {{index}}
      </div>
    </li>
  </ul>
</div>

</template>

<script>

export default {
  name: "App",

  data() {
    return {
      // counter: 0,
      // secondCounter: 0,
      // // result: '',

      // attachedRed: false,
      // color: "green",
      // show: true,

      ingredients: ['meat', 'fruits', 'cookies'],
      persons: [
        {name: 'Jack', age: 33, id: 1},
        {name: 'Bob', age: 32, id: 2},
        {name: 'Roman', age: 31, id: 3}
      ]
    }
  },

    // computed: {
    //   output() {
    //     console.log('output')
    //     return 12345;
    //   },

    //   newOutput() { 
    //     return this.message;
    //   },

    //   divClass() {
    //     return {
    //       red: this.attachedRed, 
    //       green: !this.attachedRed
    //       }
    //   }
    // },


    // methods: {
   
    //   result() {
    //     console.log('result');
         

    //     return this.counter > 5 ? 'Greater than 5' : 'Smaller than 5'
    //   }

    

    // increase() {
    //   this.counter ++;
    //   this.result = this.counter > 5 ? 'Greater than 5' : 'Smaller than 5'
    // },
  
    // decrease() {
    //   this.counter --;
    //   this.result = this.counter > 5 ? 'Greater than 5' : 'Smaller than 5'
    // }
  
  }





</script>

<style>

/* .demo {
  display: inline-block;
  margin: 5px;
  background-color: blue;
  height: 50px;
  width: 50px;
}

.red {
  background-color: red;
}

.green {
  background-color: green;
} */
</style>
