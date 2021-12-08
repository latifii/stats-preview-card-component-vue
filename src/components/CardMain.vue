<template>
  <div class="main">
    <section class="section">
      <article class="card-main">
        <h1 class="card-main-title">
          Get <span class="strong-word">insights</span> that help your business
          grow.
        </h1>
        <p class="card-main-paragraph">
          Discover the benefits of data analytics and make better decisions
          regarding revenue, customer experience, and overall efficiency.
        </p>
      </article>
      <div class="statistics">
        <CardStatistics
          v-for="item in cardStatistics"
          :key="item.id"
          :value="item.value"
          :activity="item.activity"
        />
      </div>
    </section>
    <div class="card-img">
      <img src="../assets/image-header-desktop.jpg" alt="image header" />
    </div>
  </div>
</template>

<script>
import CardStatistics from "./CardStatistics.vue";
export default {
  name: "CardMain",
  components: { CardStatistics },
  data() {
    return {
      cardStatistics: [
        {
          id: 1,
          value: "10k+",
          activity: "companies",
        },
        {
          id: 2,
          value: "314",
          activity: "templates",
        },
        {
          id: 1,
          value: "12M+",
          activity: "queries",
        },
      ],
    };
  },
};
</script>

<style scoped>
.main {
  display: flex;
  flex-direction: column-reverse;
  justify-content: center;
  align-items: center;
  background-color: var(--dark-desaturated-blue);
  max-width: 50rem;
  margin: 9rem 1.3rem;
  border-radius: 1rem;
  overflow: hidden;
  text-align: center;
}
.section {
  padding: 4rem 3rem;
}
.card-main-title {
  font-size: 2.8rem;
  line-height: 1.2;
  margin-bottom: 1.5rem;
}
.strong-word {
  color: var(--soft-violet);
}
.card-main-paragraph {
  font-size: 1.5rem;
  color: var(--slightly-transparent-white-main-paragraph);
  line-height: 1.7;
  margin-bottom: 3rem;
}
.card-img {
  display: flex;
  background: #5d0788;
}
.card-img img {
  width: 100%;
  opacity: 0.5;
}
@media (min-width: 1000px) {
  .main {
    flex-direction: row;
    text-align: left;
    max-width: 95%;
  }
  .section {
    padding: 0 6rem;
    margin: 0rem;
    flex: 1 1 50%;
  }
  .card-main-title {
    font-size: 3.1rem;
    margin-bottom: 2.3rem;
  }
  .card-main-paragraph {
    font-size: 1.3rem;
    margin-bottom: 6rem;
  }
  .statistics {
    display: flex;
    gap: 5rem;
    margin-top: 8rem;
  }
  .card-img {
    flex: 1 1 50%;
  }
}
</style>