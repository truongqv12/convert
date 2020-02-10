<template>
    <div>
        <div class="container">
            <card class="card-nav-tabs text-center" header-classes="card-header-warning">
                <div slot="header" class="mt-2">
                    Mã hóa MD5
                </div>
                <div class="form-group">
                    <label for="">String</label>
                    <textarea class="form-control border" name="" id="" rows="10" v-model="inputArea"></textarea>
                </div>
                <p>{{md5hash}}</p>
                <n-button type="primary" v-on:click="convert">Mã hóa</n-button>
            </card>
        </div>

    </div>
</template>

<script>
    import {Card} from '@/components'
    import {Button} from '@/components'
    import md5 from 'blueimp-md5'

    export default {
        name: "md5.vue",
        components: {
            Card,
            "n-button": Button,
        },
        data() {
            return {
                inputArea: '',
                md5hash:''
            }
        },
        methods: {
            convert: function () {
                let md5hash = md5(this.inputArea);
                return md5hash
            }
        }
    }
</script>

<style scoped>
    textarea.form-control {
        max-height: 500px;
    }
</style>