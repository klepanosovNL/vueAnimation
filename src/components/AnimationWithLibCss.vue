<template>
    <v-container class="text-center">
        <v-btn class="primary" @click="show = !show">touch me!</v-btn>
        <transition
                enter-active-class="animate__animated animate__lightSpeedInLeft"
                leave-active-class="animate__animated animate__lightSpeedInRight"
        >
            <p v-if="show" class="mt-6">some text...some text...some text...some text...some text...</p>
        </transition>

    </v-container>
</template>

<script>
    export default {
        data: () => ({
            show: true
        }),
    }
</script>

<style>

</style>