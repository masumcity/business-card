<template>
  <div class="body__profile__icons">
    <a href="https://www.linkedin.com/in/masumonline/"
      ><fa :icon="['fab', 'linkedin']"
    /></a>
    <a href="https://twitter.com/masumonline"
      ><fa :icon="['fab', 'twitter']"
    /></a>
    <a href="https://activelava.net"
      ><fa :icon="['fa', 'globe']"
    /></a>
  </div>
</template>

<script>
export default {
  name: "Social",
};
</script>

<style>
a {
  color: #999;
}
.body__profile__icons {
  font-size: 3.5em;
  letter-spacing: 0.4em;
  top: -20px;
  color: #737373;
  position: relative;
}

.body__profile__icons a {
  font-size: inherit;
  padding: 0 0.15em;
  color: #737373;
  transition: all 0.5s;
}

.body__profile__icons a:hover {
  font-size: inherit;
  color: #ddd;
}
</style>
