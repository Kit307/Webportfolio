<script setup>
import HelloWorld from "./components/HelloWorld.vue";
import NavBar from "./components/NavBar.vue";
import TimeLine from "./components/TimeLine.vue";
import Profile from "./components/Profile.vue";
import Contact from "./components/Contact.vue";
import Email from "./components/Email.vue";
import Certificate from "./components/Certificate.vue";
</script>

<template>
  <div :class="isDark ? 'dark' : ''">
    <div class="dark:bg-gray-700">
      <!-- <Contact></Contact> -->
      <NavBar @add="isDark = !isDark" :msg="isDark"></NavBar>
      <HelloWorld></HelloWorld>
      <TimeLine></TimeLine>
      <Profile></Profile>
      <Certificate />
      <Email />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isDark: false,
    };
  },
  components: { Contact, Profile, TimeLine, NavBar, HelloWorld, Certificate },
};
</script>
