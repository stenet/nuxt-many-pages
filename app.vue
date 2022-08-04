<script lang="ts" setup>
const links = ref(Array.from(Array(10)).map((v, i) => {
  return {
    route: `/page-${i.toString().padStart(4, "0")}`
  };
}));
</script>
<template>
  <div>
    <div>
      <h1>Current Page</h1>
      <div>
        <NuxtPage></NuxtPage>
      </div>
    </div>
    <div>
      <h1>Navigate</h1>
      <div>
        <div v-for="link in links" :key="link.route">
          <NuxtLink :to="link.route">{{link.route}}</NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>
