<template>
    <v-app>
        <v-content class="text-center">
            <AnimationList></AnimationList>
            <AnimationVue></AnimationVue>
            <AnimationMode></AnimationMode>
            <AnimationWithLibCss></AnimationWithLibCss>
        </v-content>
    </v-app>
</template>

<script>
    import AnimationList from './components/AnimationList';
    import AnimationVue from './components/AnimationVue';
    import AnimationMode from './components/AnimationMode';
    import AnimationWithLibCss from './components/AnimationWithLibCss';

    export default {
        name: 'App',

        components: {
            AnimationList, AnimationVue, AnimationMode, AnimationWithLibCss
        },

        data: () => ({}),
    };
</script>