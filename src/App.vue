<template>
    <div id="app">
        <button @click="changeLanguage">{{$t('buttons.change')}}</button>
        <h1>{{$t('greeting')}}</h1>
        <p>
            <span v-for="num in $t('numbers')">
                {{num}}
            </span>
        </p>
    </div>
</template>

<script>
    export default {
        name: 'app',
        methods: {
            changeLanguage() {
                this.$i18n.locale = this.$i18n.locale === 'zh' ? 'en' : 'zh';
            }
        },
        created() {
            console.log(this.$t('greeting'));
        }
    };
</script>

<style>

</style>
