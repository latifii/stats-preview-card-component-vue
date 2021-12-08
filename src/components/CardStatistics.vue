<template>
  
    <div class="card-statistics">
      <div class="value">
        {{ value }}
      </div>
      <div class="activity">
        {{ activity }}
      </div>
    </div>
  
</template>
<script>
export default {
  name: "CardStatistics",
  props: {
    value: {
      type: String,
      required: true,
    },
    activity: {
      type: String,
      required: true,
    },
  },
};
</script>

<style scoped>
.card-statistics {
  display: flex;
  flex-direction: column;
  /* gap: 2rem; */
  margin-bottom: 2rem;
}
.value {
  font-weight: 700;
  font-size: 2.3rem;
  color: var(--white);
  margin-bottom: 0.8rem;
  /* text-transform: uppercase; */
}
.activity {
  color: var(--slightly-transparent-white-stat-headings);
  text-transform: uppercase;
  /* margin-bottom: 2rem; */
  font-family: Lexend Deca;
  font-size: 1.2rem;
  letter-spacing: 0.1rem;
}
.card-statistics:last-child {
  margin: 0;
}
@media (min-width: 1000px) {
  
  .card-statistics {
    /* gap: 5rem; */
  }
  .value {
  font-size: 1.5rem;
  }
  .activity {
    font-size: 1.1rem;
  }
}
</style>