<template>
  <div style="margin-top: 150px">
    <h3>Value of variable 'c' is {{variables.c}}</h3>
    <p>The value of the variable 'c' is displayed correctly and its change is also triggered</p>
    <p>Since we created it with "$set()"</p>
    <br>
    <button @click="changeValue">Change Value "c"</button>
  </div>

</template>

<script>
export default {
  name: "ExampleOfCorrectUseData",

  data() {
    return {
      variables: {

      },
    }
  },

  created() {
    // add the variable 'c' using the built-in method this.$set(),
    // which adds the necessary getter/setter for variable 'c'
    this.$set(this.variables, 'c', "Initial value for variable 'c'.");
  },

  methods: {
    changeValue() {
      // when changing the variable 'c', its new value will be displayed
      // since we created it with "$set()" and it is now reactive.
      this.variables.c = "The value of the variable 'c' is changed!";
    }
  }

}
</script>