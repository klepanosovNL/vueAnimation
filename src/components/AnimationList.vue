<template>
    <v-container class="text-center">
        <button class="btn btn-success mx-1"  @click="add">Add</button>
        <button  class="btn btn-danger mx-1" @click="remove">Remove</button>
        <transition-group tag="ul" class="list-group box mt-5" name="ma">
            <li
                    v-for="item in items"
                    :key="item"
                    class="list-group-item">{{ item }}</li>
        </transition-group>
    </v-container>
</template>

<script>
    export default {
        data () {
            return {
                items: [1,2,3,4,5],
                nextNum: 6
            }
        },
        methods: {
            getIndex () {
                return Math.floor(Math.random() * this.items.length)
            },
            add () {
                this.items.splice(this.getIndex(), 0, this.nextNum++)
            },
            remove () {
                this.items.splice(this.getIndex(), 1)
            }
        }
    }
</script>

<style scoped>
.box {
    max-width: 300px;

    margin: 0 auto;
}

    .ma-enter-active, .ma-leave-active {
        transition: 1s all;
    }

    .ma-enter, .ma-leave-to {
        transform: translateX(-100px);
    }

</style>