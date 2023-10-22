<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
import MessageList from './components/MessageList/MessageList.vue'
</script>

<template>
  <header>

    
  </header>

  <main>
    <div class="wrapper">
      <MessageList message="It's a glorious feeling!" message1="Deh tah heh!" message2="You're powered up..."></MessageList>
      <MessageList message="Get in there." message1="Pressing Q!" message2="Ahee barambassa"></MessageList>
    </div>
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }
}
</style>
