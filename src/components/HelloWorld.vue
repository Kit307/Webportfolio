<template>
  <div class="h-screen columns-1 md:columns-2">
    <h1
      class="dark:text-white text-center md:text-left md:mt-40 lg:ml-9 md:ml-14 p-5 text-4xl"
    >
      I am constantly improving myself <br />
      and never stop learning new things.
    </h1>
    <img src="../assets/img/spact.png" alt="" class="h-0 md:h-96 vert-move" />
  </div>
</template>

<script>
export default {};
</script>

<style>
img.vert-move {
  -webkit-animation: mover 1s infinite alternate;
  animation: mover 1s infinite alternate;
}
img.vert-move {
  -webkit-animation: mover 1s infinite alternate;
  animation: mover 1s infinite alternate;
}
@-webkit-keyframes mover {
  0% {
    transform: translateY(0);
  }
  100% {
    transform: translateY(-10px);
  }
}
@keyframes mover {
  0% {
    transform: translateY(0);
  }
  100% {
    transform: translateY(-10px);
  }
}
</style>
