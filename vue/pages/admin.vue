<template>
    <div class="title" v-if="isAuthenticated">
        <h2>Admin Menu</h2>
        <h4>//TODO: Show users</h4>
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
//            content: false
        }),
//        methods: {
//        },
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