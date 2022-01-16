<template>
    <div class="Display">
        <User :users="users"/>
    </div>
</template>

<script>
import User from './User.vue';

export default {
    name: 'Display',
    components: {
        User,
    },
    props: {
        users: Array,
    }
}
</script>

<style scoped>

</style>