<template>
  <ul>
    <li v-for="goal in goals" :key="goal">
        <slot :item="goal" another-prop="HI"></slot>
    </li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      goals: ["first goal!", "second goal!"],
    };
  },
};
</script>

