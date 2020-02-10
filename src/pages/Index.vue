<template>
    <div class="starter-page">
        <div class="section text-center pb-0">
            <h3>Mã hóa MD5</h3>
        </div>
        <md5></md5>
    </div>
</template>
<script>
    import md5 from './components/md5';
    export default {
        name: 'index',
        components :{
            md5
        }
    };
</script>
<style>
    .starter-page {
        min-height: calc(100vh - 100px);
    }
</style>
