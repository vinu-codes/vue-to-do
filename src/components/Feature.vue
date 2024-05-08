<template>
    <div>
        <h1>To Do List</h1>
        <label html-for="search">
            Search
            <input id='search' v-model="searchValue" @change="onSearch" />
        </label>
        <ul class="group">
            <li class="list" v-for="item in searchItems" :key="item.id">{{ item.label }}
                <button @click="handleDelete(item)">Delete</button>
            </li>
        </ul>
        <input v-model="value" @change="onChange" />
        <button @click="handleAdd">Add item!</button>
    </div>
</template>

<script>
import { uuid } from './uuid.js'
export default {
    data() {
        return {
            value: '',
            searchValue: '',
            items: [
            ]
        };
    },
    computed: {
        searchItems() {
            return this.items.filter(item => item.label.includes(this.searchValue))
        }

    },
    methods: {
        onChange(e) {
            this.value = e.target.value
        },
        onSearch(e) {
            this.searchValue = e.target.value
        },
        handleAdd() {
            this.items = [...this.items, { id: uuid(), label: this.value }]
            this.value = ''
        },
        handleDelete(item) {
            this.items = this.items.filter(i => i.id !== item.id)
        }
    }
};
</script>

<style scoped>
.group,
.list {
    list-style: none;
    padding: 0;
}
</style>
