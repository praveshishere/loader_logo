<template>
  <div
    class="p-10 relative flex justify-center items-center border-2 border-red-600"
  >
    <div
      class="border-blue-600 rounded-full p-2 w-64 h-64 flex justify-center items-center parent"
    >
      <div
        class="border-4 border-white border-l-blue-600 border-r-blue-600 rounded-full p-8 w-56 h-56 flex justify-center items-center child"
      >
        <img id="logo" src="/epf_logo.svg" alt="" class="animate-none" />
      </div>
    </div>
  </div>
</template>

<script setup lang="ts"></script>

<style>

@keyframes rotate {
  from{ -webkit-transform: rotate(0deg);   }
  to{   -webkit-transform: rotate(360deg); }
}

@keyframes rotate_reverse {
  from{ -webkit-transform: rotate(360deg);   }
  to{   -webkit-transform: rotate(0deg); }
}
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

.dot {
  position: absolute;
  height: 250px;
  width: 40px;
  top: -25px;
  left: 50%;
	margin-left: -20px;
  
  &:before {
    display: block;
    content: '';
    height: 40px;
    width: 40px;
    border-radius: 50%;
    box-shadow: 0 2px 3px rgba(0,0,0,.1);
  }
}
.dot--one {
  animation: rotateClockwise 4s linear infinite;
  
  &:before {
    background: #e6a933;
  }
}


/* .parent {
  animation: rotate 2s linear infinite;
} */

.child {
  animation: rotate_reverse 2s linear infinite;
}

#logo {
  /* animation: none !important; */
  animation: rotate 2s linear infinite;

}

</style>
