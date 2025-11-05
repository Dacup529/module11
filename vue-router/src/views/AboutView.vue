<template>
  <div id="about">
    <h1>About</h1>
    <p>This is my Module 11 Vue Assignment with Routing</p>
    <GoBack/>
  </div>
</template>

<script>
import GoBack from "@/components/GoBack.vue";

export default {
  name: "AboutView",
  components: {
    GoBack,
  },
};
</script>

<style>
#about {
  text-align: center;
  margin-top: 50px;
  font-family: Arial, sans-serif;
}
</style>
