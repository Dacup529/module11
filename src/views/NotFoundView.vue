<template>
  <div id="notfound">
    <h1>404 - Page Not Found</h1>
    <p>Oops! The page you are looking for does not exist.</p>
    <GoBack/>
  </div>
</template>

<script>
import GoBack from "@/components/GoBack.vue";

export default {
  name: "NotFoundView",
  components: {
    GoBack,
  },
};
</script>

<style>
#notfound {
  text-align: center;
  margin-top: 50px;
  font-family: Arial, sans-serif;
  color: #c0392b; /* red color for error page */
}

#notfound h1 {
  font-size: 2rem;
  margin-bottom: 15px;
}

#notfound p {
  font-size: 1.1rem;
  margin-bottom: 25px;
}
</style>