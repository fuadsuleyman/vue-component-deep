<template>
  <div>
    <h2>Manage Goals</h2>
    <input type="text"  ref="goal"/>
    <button @click="setGoals">Set Goal</button>
  </div>
</template>


<script>
export default {
    methods: {
        setGoals(){
            if (this.$refs.goal.value === '')
            alert("Input is Empty")
        }
    },
}
</script>