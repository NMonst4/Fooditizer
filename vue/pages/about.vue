<template>
    <div class="title" v-if="isAuthenticated">
        <h2>Button content</h2>
        <v-btn primary>Primary button</v-btn>
        <v-btn secondary>Secondary button</v-btn>
        <v-btn success>Success button</v-btn>
    </div>
</template>

<script>
    import {mapGetters} from 'vuex'
    export default {
        computed: mapGetters([
            'isAuthenticated',
            'loggedUser'
        ]),
        data: () => ({
        }),
        methods: {

        },
        mounted: function () {
            let self = this;
            setTimeout(function () {
                if(!self.isAuthenticated){
                    window.location.href = '/';
                }
            }, 500);
        }
    }
</script>