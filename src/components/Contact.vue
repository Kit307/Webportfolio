<template>
  <div>
    <h1
      class="md:pl-40 ml-8 text-4xl pb-16 text-green-400 underline underline-offset-8 font-black"
    >
      Contact {{ show_text }}
    </h1>
  </div>
</template>

<script>
export default {
  data() {
    return {
      xxx: 0,
      full_text:
        " I am constantly improving myself \n and never stop learning new things.",
      show_text: "",
    };
  },
  mounted() {
    this.print_log();
  },
  methods: {
    print_log() {
      let text = this.full_text.split("");
      let len_text = 0;
      for (let i = this.full_text.length; i >= 1; i--) {
        setTimeout(() => {

          this.show_text += text[len_text];
          len_text++;
        }, 500 * i);
      }
    },
  },
};
</script>

<style></style>
