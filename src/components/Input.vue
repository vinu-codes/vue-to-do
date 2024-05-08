<template>
    <label html-for="search">
        Search
        <input id='search' v-model="inputValue" @input="handleInput" />
    </label>
</template>

<script>
export default {
    data() {
        return {
            inputValue: ''
        };
    },
    methods: {
        handleInput(event) {
            this.$emit('input', this.inputValue);
        }
    }
};
</script>