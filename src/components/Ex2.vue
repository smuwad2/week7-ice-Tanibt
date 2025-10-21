<script>
export default {
    // Add code in appropriate places
    data() {
        return {
            items: ['keyboard', 'mouse', 'iPhone', 'macbook', 'adapter'],
            newItem: ''
        }

    },
    methods: {
        addItem() {
            if (this.newItem !== '') {
                this.items.push(this.newItem)
                this.newItem = ''

            }
        },
        deleteItem(index) {
            this.items.splice(index, 1)
        }
    }
}
</script>

<template>

    <h2>Shopping Cart</h2>
    <!-- TODO: Add Code Here -->
    <input v-model="newItem" placeholder="Enter item name" />
    <button @click="addItem">Add!</button>

    <ul>
        <li v-for="(item, index) in items" :key="index">
            {{ item }}
            <button @click="deleteItem(index)">Delete</button>
        </li>
    </ul>



</template>
