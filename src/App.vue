<script>
import HelloSlot from './components/HelloSlot.vue'
import WelcomeSlot from './components/WelcomeSlot.vue'
import GoalsSlot from './components/GoalsSlot.vue'


export default {
  name: 'App',
  components: {
    HelloSlot,
    WelcomeSlot,
    GoalsSlot
  },
  mounted()
  {
    console.log(this.$slots)
  }
}
</script>

<template>
  <main>
    <!-- Single slot -->
    <HelloSlot>
      <h1>Slot</h1>
      <p>Slot</p>
    </HelloSlot>

    <!-- named slots -->
    <WelcomeSlot>
      <template v-slot:slotpart1>
        <div class="slotpart">
          <h2>Slot Part 1</h2>
          <p>This is part 1</p>
        </div>
      </template>  
      <template v-slot:slotpart2>
        <div class="slotpart">
          <h2>Slot Part 2</h2>
          <p>This is part 2</p>
        </div>
      </template>  
    </WelcomeSlot>

  <!-- scoped slots, slotProps (you can choose the name freely) is an object that I create where all the slot data is merged in from GoalsSlot -->
  <GoalsSlot>
    <template v-slot:default="slotProps">
      <div class="goals">
        <h2>{{slotProps.item}}</h2>
        <p>{{ slotProps['another-prop'] }}</p>
      </div>
    </template>
  </GoalsSlot>



  </main>
</template>

<style scoped>

</style>
