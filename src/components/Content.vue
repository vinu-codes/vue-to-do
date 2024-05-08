<template>
    <div class="content">
        <slot></slot>
    </div>
</template>

<script>
export default {

};
</script>

<style scoped>
.content {
    background: white;
    border: 1px solid black;
    padding: 24px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    min-height: 500px;
    max-height: 500px;
    overflow: auto;
}
</style>