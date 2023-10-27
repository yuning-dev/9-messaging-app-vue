<template>
    <div :class="$style.wrapper">
        <p>
            {{ message.content }}
        </p>
        <img @click="deleteButtonClicked" :class="$style.deleteButton" role="button" src="bin-icon.png" width="24" height="24" alt="Deletion button"/>
    </div>
</template>

<script>
export default {
    name: 'Message',
    props: {
        message: Object,
    },
    mounted() {
        // This function is called when the component is added to the DOM
    },
    methods: {
        deleteButtonClicked() {
            this.$emit('deleteMessage', this.message.messageId)
        }
    },
}
</script>

<style module src="./Message.module.css" />