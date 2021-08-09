<template>
  <div>
    <h3>The value of the variable 'a' is {{variables.a}}</h3>
    <p>Variable 'a' was added correctly</p>
    <h3>Value of variable 'b is {{variables.b}}</h3>
    <p>The value of the variable 'b is displayed, but when it changes, the reactivity will not work</p>
    <br>
    <button @click="changeValue">Change Value "b"</button>
  </div>

</template>

<script>
export default {
  name: "ExampleOfIncorrectUseData",

  data() {
    return {
      variables: {
        a: "Initial value for variable 'a'." // a are now reactive
      },
    }
  },

  created() {
    // the variable 'b' in will be created, but its getter/setter will not be initialized,
    // since they are set during the creation of the component
    // and therefore this variable will not be reactive
    this.variables.b = "Initial value for variable 'b'.";
  },

  mounted() {
    // the displayed value of the variable 'a' will be lower than the indicated value, since it is declared correctly
    this.variables.a = "The value of the variable 'a' is changed!";

  },

  methods: {
    changeValue() {
      // to make sure that variable b is not reactive, change its value
      // and see that the result is the initial value
      this.variables.b = "The value of the variable 'b' is changed!";
      // let's see the value of the variable 'b' in the console and make sure that it has changed
      console.log(this.variables.b);
    }
  }

}
</script>