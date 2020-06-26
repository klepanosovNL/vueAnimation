<template>
    <v-container class="text-center">
        <v-btn class="primary" @click="show = !show">touch me!</v-btn>
        <transition
                name="ma"
                :duration="{enter: 500, leave: 2000}"
                appear
        >
            <p v-if="show" class="mt-6">some text...</p>
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

<style scoped>
    .ma-enter {
        opacity: 0;
    }

    .ma-enter-active {
        transition: opacity 2s;
    }

    .ma-enter-to {
    }

    .ma-leave {
    }

    .ma-leave-active {
        animation: .5s ma-slide forwards;
        transition: opacity 1s;
    }

    .ma-leave-to {
        opacity: 0;
    }

    @keyframes ma-slide {
        from {
            transform: translateY(0);
        }

        to {
            transform: translateY(-50%);
        }
    }

</style>