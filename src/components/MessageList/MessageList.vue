<template>
    <div :class="$style.wrapper">
        <template v-for="chair in messages">
            <Message @deleteMessage="deleteMessage" :message="chair" />
        </template>
        <input @keyup.enter="textEntered" v-model="newMessageContents" type="text" />
    </div>
</template>

<script>
import Message from '../Message/Message.vue'

export default {
    name: 'MessageList',
    components: {
        Message,
    },
    data() {
        return {
            messages: [{
                userId: 1,
                messageId: 0,
                content: 'This is a test message',
                timestamp: Date.now(),
            }],
            newMessageContents: '',
            newMessageId: 1,
        }
    },
    methods: {
        textEntered() {
            this.createNewMessage(this.newMessageContents, this.newMessageId)

            this.newMessageContents = ''
            this.newMessageId++
        },
        createNewMessage(content, messageId) {
            const message = {
                userId: 1,
                messageId: messageId,
                content: content,
                timestamp: Date.now(),
            }

            this.messages.push(message)
        },
        deleteMessage(messageId) {
            this.messages = this.messages.filter((message) => {
                if (messageId !== message.messageId) {
                    return true
                }
                return false
            })
        },
    }
}
</script>

<style module src="./MessageList.module.css" />