<template>
  <div id="demo">
    <div v-if="bangla" class="body__profile__button-area" id="bn-bd">
      <transition name="fade" v-on:enter="enter">
        <Bangla />
      </transition>
      <Social />
      <button class="body__profile__button github">
        <a href="https://github.com/masumonline"
          >Github প্রোফাইল</a
        >
      </button>
    </div>

    <div v-else class="body__profile__button-area">
      <transition name="fade" v-on:enter="enter">
        <English />
      </transition>
      <Social />
      <button class="body__profile__button github botao">
        <a href="https://github.com/masumonline"
          >View portfolio on GitHub</a
        >
      </button>
    </div>
    <div class="body__profile__translate">
      <button @click="translate" v-if="trans" v-on:click="fadeMe">
        <fa icon="flag" /> Translate {{ enFlag }}
      </button>
      <button @click="translate" v-else v-on:click="fadeMe">
        <fa icon="flag" /> অনুবাদ (BN)
      </button>
    </div>
  </div>
</template>

<script>
import Bangla from "./Bangla";
import English from "./English";
import Social from "./Social";

export default {
  name: "Buttons",
  el: "#demo",
  components: {
    Bangla,
    English,
    Social,
  },
  data() {
    return {
      trans: Boolean(true),
      bangla: Boolean,
      resume:
        "../assets/profile.pdf",
      curriculo:
        "../assets/profile.jpg",
      ptFLag: "(PT-BR)",
      enFlag: "(EN)",
      show: false,
    };
  },
  methods: {
    translate() {
      this.bangla = !this.bangla;
      this.trans = !this.trans;
      console.log("clicado aqui");
    },

    fadeMe: function () {
      this.show = !this.show;
    },

    enter: function () {
      var that = this;

      setTimeout(function () {
        that.show = false;
      }, 3000); // hide the message after 3 seconds
    },
  },
};
</script>

<style>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 1s;
}

.fade-enter,
    .fade-leave-to
    /* .fade-leave-active in <2.1.8 */ {
  opacity: 0;
}

.body__profile__button-area {
  top: -40px;
  position: relative;
}

.body__profile button a {
  text-decoration: none;
  color: white;
}

.body__profile button {
  border: none;
  border-radius: 10px;
  font-family: Orkney;
  text-transform: uppercase;
  padding: 1.5em 1em;
  width: 100%;
  color: white;
  letter-spacing: 2px;
  font-weight: bold;
  margin: 0.5em 0;
  cursor: pointer;
  transition: all 0.5s;
}

.github {
  background-color: #d1a1f5;
}

.github:hover {
  background-color: #df2fe6;
}

.cv {
  background-color: #b9a9ff;
}

.cv:hover {
  background-color: #842fe6;
}

.body__profile__translate button {
  font-size: 0.75em;
  border: 0;
  background-color: transparent;
  padding: 0;
  text-transform: uppercase;
  letter-spacing: 3px;
  color: #999;
  top: -10px;
  cursor: pointer;
  position: relative;
  transition: all 0.5s;
}
</style>
