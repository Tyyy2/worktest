<template>
  <AllHeader></AllHeader>
</template>

<script>
// @ is an alias to /src
import AllHeader from "@/components/AllHeader.vue";
export default {
  name: "HomeView",
  components: { AllHeader },
};
</script>

<style lang="scss">
body{
background-color: black;
}

</style>
