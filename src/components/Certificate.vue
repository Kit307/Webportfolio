<template>
  <div>
    <h1
      class="md:pl-40 reveal ml-8 text-4xl pb-16 text-green-400 underline underline-offset-8 font-black"
    >
      Certificate
    </h1>
    <div class="lg:flex reveal justify-center items-center lg:gap-9">
      <img
        class="sm:min-w-96 lg:max-w-lg py-10 px-5 h-auto rounded-lg transition-all duration-300 cursor-pointer filter grayscale hover:grayscale-0"
        src="../assets/img/unity.jpg"
        alt="image description"
        @click="show = true"
      /><img
        class="sm:min-w-96 lg:max-w-lg py-10 px-5 h-auto rounded-lg transition-all duration-300 cursor-pointer filter grayscale hover:grayscale-0"
        src="../assets/img/depa.jpg"
        alt="image description"
        @click="show1 = true"
      />
    </div>

<Transition>
 
    <div
      v-if="show"
      class="z-50 fixed top-0 left-0 w-screen h-screen bg-black/70 flex justify-center items-center"
    >
      <!-- The close button -->
      <button
        @click="show = false"
        class="fixed z-90 top-6 right-8 text-white text-5xl font-bold"
      >
        &times;
      </button>

      <!-- A big image will be displayed here -->
      <img
        id="modal-img"
        class="md:max-h-[500px] lg:max-h-[500px] xl:max-h-[700px] sm:max-h-[800px] w-auto"
        src="../assets/img/unity.jpg"
      />
    </div>
    </Transition>
    <Transition>
    <div
      v-if="show1"
      class="z-50 fixed top-0 left-0 w-screen h-screen bg-black/70 flex justify-center items-center"
    >
      <!-- The close button -->
      <button
        @click="show1 = false"
        class="fixed z-90 top-6 right-8 text-white text-5xl font-bold"
      >
        &times;
      </button>

      <!-- A big image will be displayed here -->
      <img
        id="modal-img"
        class="md:max-h-[500px] lg:max-h-[500px] xl:max-h-[700px] sm:max-h-[800px] w-auto"
        src="../assets/img/depa.jpg"
      />
    </div>
  </Transition>
  </div>
</template>

<script>
export default {
  data() {
    return {
      show: false,
      show1: false,
    };
  },
};
</script>

<style>/* we will explain what these classes do next! */
.v-enter-active,
.v-leave-active {
  transition: opacity 0.5s ease;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}
</style>
