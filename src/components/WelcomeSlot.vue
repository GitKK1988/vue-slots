<template>
    <div class="slotpart">
        <slot name="slotpart1"></slot>

        <slot name="slotpart2"></slot>
    </div>

</template>

<script>

export default {
    name: 'WelcomeSlot',
    props: {
        msg: String
    },
    mounted()
    {
        console.log(this.$slots)
    }
}

</script>

<style scoped>

.slotpart
{
    background-color: #f0f0f0;
    border: 1px solid #000;
    padding: 1em;
}



</style>