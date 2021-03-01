<template>
  <h2>Manage goal</h2>
  <input type="text" ref="goal" />
  <button @click="setGoal">Set goal</button>
  <teleport to="body">
    <error-alert v-if="isInputInvalid">
      <h2>This is error alert</h2>
    </error-alert>
  </teleport>
</template>
<script>
import ErrorAlert from "./ErrorAlert.vue";
export default {
  components: {
    ErrorAlert,
  },
  data() {
    return {
      isInputInvalid: true,
    };
  },
  methods: {
    setGoal() {
      const enteredValue = this.$refs.goal.value;
      if (enteredValue === "") {
        this.isInputInvalid = true;
      } else {
        this.isInputInvalid = false;
      }
    },
  },
};
</script>
