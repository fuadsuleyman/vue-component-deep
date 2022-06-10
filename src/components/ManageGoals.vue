<template>
  <div>
    <h2>Manage Goals</h2>
    <input type="text" ref="goal" />
    <button @click="setGoals">Set Goal</button>
    <teleport to="body">
      <alert-error v-if="inputisInvalid">
        <h2>Input is Invalid</h2>
        <p>Please add at least few characters...</p>
        <button @click="confirmError">Okay</button>
      </alert-error>
    </teleport>
  </div>
</template>


<script>
import AlertError from "./ErrorAlert.vue";
export default {
  components: { AlertError },
  data() {
    return {
      inputisInvalid: false,
    };
  },
  methods: {
    setGoals() {
      if (this.$refs.goal.value === "") this.inputisInvalid = true;
      console.log(`this.inputisInvalid: ${this.inputisInvalid}`);
    },
    confirmError() {
      this.inputisInvalid = false;
      console.log(`this.inputisInvalid: ${this.inputisInvalid}`);
    },
  },
};
</script>