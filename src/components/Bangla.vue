<template>
  <div class="body__profile__title">
    <h1>রিয়াজ উদ্দিন মাসুম</h1>
    <h2>হেড অফ ডিজিটাল সার্ভিস </h2>
    <h2>ফুল স্ট্যাক ডেভেলপার</h2>
    <div class="body__profile__bio-en">{{ bioEn }}</div>
  </div>
</template>

<script>
export default {
  name: "Bangla",
  data: () => ({
    bioEn: `কেউ আমাকে থামান`,
  }),
};
</script>

<style>
.body__profile__title {
  top: -20px;
  position: relative;
}

.body__profile__title h1 {
  font-size: 1.5em;
  font-weight: 900;
  text-align: center;
  color: rgb(84, 84, 84);
  margin: 0 0 0.5em 0;
}

.body__profile__title h2 {
  font-size: 0.75em;
  color: rgb(153, 153, 153);
  line-height: 1.391;
  font-weight: lighter;
  text-align: center;
  text-transform: uppercase;
}

.body__profile__bio-en {
  font-size: 0.75em;
  color: rgb(171, 171, 171);
  font-weight: 900;
  line-height: 1.404;
  text-align: center;
  margin: 1em 0;
  padding: 1.25em 0;
  border-top: 4px solid whitesmoke;
  border-bottom: 4px solid whitesmoke;
  transition: all 0.5s ease-in-out;
}
</style>
