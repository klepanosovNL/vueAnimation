<template>
    <v-container class="text-center">
        <v-btn class="primary" @click="show = !show">touch me!</v-btn>
        <transition name="ma" mode="out-in">
            <v-alert
                    class="mt-10"
                    type="success"
                    v-if="show"
                    key="success"
            >Success
            </v-alert>
            <v-alert
                    class="mt-10"
                    type="error"
                    v-else
                    key="danger"
            >Danger
            </v-alert>
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