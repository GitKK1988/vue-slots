<template>
    <div class="goals">
        <ul>
            <li v-for="goal in goals" :key="goal.id">
                <slot :item="goal" another-prop="..."></slot>
            </li>
        </ul>
    </div>

</template>

<script>

export default {
    name: 'GoalsSlot',
    props: {
        msg: String
    },
    data(){
        return {
            goals: ['goal1', 'goal2', 'goal3']
        }
    },
    mounted()
    {
        console.log(this.$slots)
    }
}

</script>

<style scoped>

.goals
{
    background-color: #555;
    border: 1px solid yellow;
    padding: 1em;
}



</style>