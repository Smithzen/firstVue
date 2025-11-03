<script setup lang="ts">
defineProps({
  handleChangeDisplay: Function,
})
</script>

<template>
  <section id="welcome">
    <div class="benefits">
      <h2>Complete this program<br />If you can...</h2>
    </div>
    <div>
      <p><input type="checkbox" />Follow this program if you want to get shredded</p>
    </div>
    <div>
      <h3>The training plan</h3>
      <p>This training plan follows a program known as the <strong>Bro Split</strong>.</p>
      <h5><i>push &rarr; pull &rarr; legs &rarr; repeat</i></h5>
    </div>
    <div class="card challenge">
      <h3>flame emoji Your Challenge</h3>
      <p>Complete all the workouts and track your progress along the way</p>
      <p>Do you accept?</p>
      <button @click="() => handleChangeDisplay(2)">Begin &rarr;</button>
    </div>
  </section>
</template>

<style scoped>
#welcome,
.challenge,
.benefits {
  display: flex;
  flex-direction: column;
}

#welcome {
  gap: 1.5rem;
}

.benefits {
  gap: 0.5rem;
}

.challenge {
  gap: 0.25rem;
}

@media (min-width: 640px) {
  #welcome {
    gap: 2rem;
    padding: 1rem 0;
  }

  .benefits {
    gap: 1rem;
  }
}
</style>
