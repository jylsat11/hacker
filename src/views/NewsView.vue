<template>
<div>
  <list-item :listData="list"></list-item>
</div>
</template>

<script>
import ListItem from '../components/ListItem.vue'

export default {
    computed: {
        list() {
            return this.$store.state.list;
        }
    },
    created() {
        this.$store.dispatch('FETCH_LIST', 'news')
    },
    components: {
        ListItem
    }
}
</script>

<style>

</style>