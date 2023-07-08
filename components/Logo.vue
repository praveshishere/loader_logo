<template>
  <div
    class="p-10 relative flex justify-center items-center border-2 border-red-600"
  >
    <div
      class="border-t-blue-600 border-b-blue-600 border-4 rounded-full p-2 w-72 h-72 flex justify-center items-center parent"
    >
      <div
        class="border-4 border-l-blue-800 border-r-blue-800 rounded-full p-2 w-64 h-64 flex justify-center items-center child"
      >

      <div
        class="border-4 border-l-blue-700 border-r-blue-700 rounded-full p-8 w-56 h-56 flex justify-center items-center grandchild"
      >
    </div>
    </div>
    </div>
    <img id="logo" src="/epf_logo.svg" alt="" class="animate-none absolute" />
  </div>
</template>

<script setup lang="ts"></script>

<style>
@keyframes rotateClockwise {
  100% {
    transform: rotate(360deg);
  }
}
@keyframes rotateCounterClockwise {
  100% {
    transform: rotate(-360deg);
  }
}

.parent {
  animation: rotateClockwise 4s ease-in-out infinite;
}

.child {
  animation: rotateClockwise 5s ease-in infinite;
}

.grandchild {
  animation: rotateClockwise 6s ease-out infinite;
}
</style>
