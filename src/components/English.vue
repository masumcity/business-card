<template>
  <div class="body__profile__title">
    <h1>Riaz Uddin Masum</h1>
    <h2>Head Of Digital Service</h2>
    <h2>Full Stack Web Developer</h2>
    <div class="body__profile__bio-en">{{ bioEn }}</div>
  </div>
</template>

<script>
export default {
  name: "English",
  data: () => ({
    bioEn: `Web Developer with 15 years of experience in designing and developing user interfaces, testing, debugging, and training staff within eCommerce technologies. Proven ability in optimizing web functionality that improve data retrieval and workflow efficiencies.`,
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
