<template>
    <div>
       <div v-for="(items, index) in items" :key="index">
           <list-item
                :item="item"
                class="item"
                v-on:itemChanged="$emit('reloadlist ')"
                />
       </div>
    </div>
</template>


<script>
// import { component } from 'vue/types/umd'
import listItem from "./listItem"
import ListItem from './listItem.vue'

export default {
  components: { listItem },
    props: ['items'],
    components:{
         listItem

    }
}
</script>

<style scoped>
.item {
    background: #e6e6e6;
    padding: 5px;
    margin-top: 5px;
}

</style>