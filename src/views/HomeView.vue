<template>
  <div class="home">
    <div>{{ test }}</div>
    <img alt="Vue logo" width="100" src="@/assets/demo.svg" />
    <HelloWorld :msg="msg" />
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";
import HelloWorld from "@/components/HelloWorld.vue"; // @ is an alias to /src

export default defineComponent({
  name: "HomeView",
  components: {
    HelloWorld,
  },
});
</script>
<script setup lang="ts">
const test = ref(0);
setInterval(() => {
  test.value++;
}, 1000);
const msg = ref<string>("Welcome to Your Vue.js + TypeScript App");
</script>
