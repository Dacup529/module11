<template>
  <div id="contact">
    <h1>Contact</h1>
    <p>Name: Reese Parker</p>
    <p>Email: rgparker@my.waketech.edu</p>
    <GoBack/>
  </div>
</template>

<script>
import GoBack from "@/components/GoBack.vue";

export default {
  name: "ContactView",
  components: {
    GoBack,
  },
};
</script>

<style>
#contact {
  text-align: center;
  margin-top: 50px;
  font-family: Arial, sans-serif;
}
</style>