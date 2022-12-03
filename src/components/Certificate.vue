<template>
  <div>
    <h1
      class="md:pl-40 ml-8 text-4xl pb-16 text-green-400 underline underline-offset-8 font-black"
    >
      Certificate
    </h1>
    <div class="md:flex justify-center items-center gap-9">
      <img
        class="sm:min-w-96 lg:max-w-lg h-auto rounded-lg transition-all duration-300 cursor-pointer filter grayscale hover:grayscale-0"
        src="../assets/img/img14.jpg"
        alt="image description"
        @click="show = true"
      /><img
        class="sm:min-w-96 lg:max-w-lg h-auto rounded-lg transition-all duration-300 cursor-pointer filter grayscale hover:grayscale-0"
        src="../assets/img/img19.jpg"
        alt="image description"
        @click="show1 = true"
      />
    </div>

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
        src="../assets/img/img14.jpg"
      />
    </div>
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
        src="../assets/img/img19.jpg"
      />
    </div>
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

<style></style>
