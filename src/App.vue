<script setup>
import MessageList from './components/MessageList/MessageList.vue'
</script>

<template>
  <header>

    
  </header>

  <main>
    <div class="wrapper">
      <MessageList ></MessageList>
    </div>
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
  display: flex;
  place-items: center;
  padding-right: calc(var(--section-gap) / 2);
}

.logo {
  display: block;
  margin: 0 2rem 0 0;
}

</style>
