<template>
  <div>
    <div class="">
      <img
        src="../assets/img/img20.jpg "
        alt=""
        class="object-cover h-screen w-full"
      />
      <div class="w-full absolute top-[4.35rem] h-screen bg-black/50"></div>
      <h1
        class="absolute text-center text-lg font-extrabold text-gray-900 dark:text-white md:text-3xl sm:text-xl lg:text-6xl top-[50%] lg:top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2"
      >
        <span
          class="text-transparent bg-clip-text bg-gradient-to-r from-green-400 to-blue-500"
          >{{ show_text }}</span
        >
      </h1>
      <h1
        class="absolute text-center text-sm text-white md:text-2xl lg:text-2xl top-[60%] left-[50%] lg:left-1/2 -translate-x-1/2 -translate-y-1/2"
      >
        <span
          class="italic font-medium text-white"
          style="text-shadow: 1px 1px 1px #000, 3px 3px 5px blue"
          >{{ show_text2 }}</span
        >
      </h1>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      xxx: 0,
      full_text: " I'M KRIT SAEEAW ",
      full_text2:
        " I am constantly improving myself and never stop learning new things. ",
      show_text: "",
      show_text2: "",
    };
  },
  mounted() {
    this.print_log();
    this.print_log2();
  },
  methods: {
    print_log() {
      let text = this.full_text.split("");
      let len_text = 0;
      for (let i = this.full_text.length; i >= 1; i--) {
        setTimeout(() => {
          this.show_text += text[len_text];
          len_text++;
        }, 200 * i);
      }
    },
    print_log2() {
      let text2 = this.full_text2.split("");
      let len_text2 = 0;
      for (let i = this.full_text2.length; i >= 1; i--) {
        setTimeout(() => {
          this.show_text2 += text2[len_text2];
          len_text2++;
        }, 100 * i);
      }
    },
  },
};
</script>

<style>
.textShadow {
  text-shadow: 2px 2px #ff0000;
}
</style>
