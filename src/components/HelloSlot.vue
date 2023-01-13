<template>
    <div class="slot1">
        <slot></slot>
    </div>

</template>

<script>

export default {
    name: 'HelloSlot',
    props: {
        msg: String
    }
}

</script>

<style scoped>

.slot1
{
    background-color: #f0f0f0;
    border: 1px solid #ccc;
    padding: 1em;
}

</style>