<template>
    <div :class="$style.wrapper">
        {{ message }}
        {{ message1 }}
        {{ message2 }}
    </div>
</template>

<script>
export default {
    name: 'MessageList',
    props: {
        message: String,
        message1: String,
        message2: String,
    }
}
</script>

<style module src="./MessageList.module.css" />