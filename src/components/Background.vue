<script setup>
import { onMounted, onUnmounted } from 'vue'
import { watchViewport, unwatchViewport } from 'tornis'

const updateValues = ({ size, mouse, orientation }) => {

  var xFromCenterRatio, yFromCenterRatio

  if (mouse.changed || orientation.changed) {
    if (mouse.changed) {
      xFromCenterRatio = (mouse.x - size.x / 2) / (size.x / 2)
      yFromCenterRatio = (mouse.y - size.y / 2) / (size.y / 2)
    }

    if (orientation.changed) {
      xFromCenterRatio = orientation.gamma / 22.5
      yFromCenterRatio = orientation.beta / 22.5
    }

    document.body.style.setProperty('--shiftX', xFromCenterRatio.toFixed(2))
    document.body.style.setProperty('--shiftY', yFromCenterRatio.toFixed(2))
  }
}

onMounted(() => {
  // bind the watch function
  watchViewport(updateValues)
})


onUnmounted(() => {
  // when you want to stop updating
  unwatchViewport(updateValues)
})


</script>

<template>
  <div class="absolute top-0 left-0 right-0 bottom-0 overflow-hidden brightness-75 -z-10">
    <img
      src="/assets/W_1/layer_0.png"
      alt
      class="min-w-full object-cover fixed top-0 xl:top-[-5%] 2xl:top-[-10%] z-[-100]"
    />
    <img
      src="/assets/W_1/layer_1.0.png"
      alt
      class="moving left-[-5%] -z-50"
      style="transform: translate3d(calc(var(--shiftX) * -1%), calc(var(--shiftY) * -1%), 0);"
    />
    <img
      src="/assets/W_1/layer_2.0.png"
      alt
      class="moving left-[-5%] z-[-49]"
      style="transform: translate3d(calc(var(--shiftX) * -0.5%), calc(var(--shiftY) * -0.5%), 0);"
    />
    <img
      src="/assets/W_1/layer_3.0.png"
      alt
      class="moving z-[-48]"
    />
    <img
      src="/assets/W_1/layer_4.0.png"
      alt
      class="moving left-[-5%] z-[-47]"
      style="transform: translate3d(calc(var(--shiftX) * 0.5%), calc(var(--shiftY) * 0.5%), 0);"
    />
    <img
      src="/assets/W_1/layer_5.1.png"
      alt
      class="moving left-[-5%] z-[-45]"
      style="transform: translate3d(calc(var(--shiftX) * 1%), calc(var(--shiftY) * 1%), 0);"
    />
    <div class="h-[3%] w-full fixed bottom-0 bg-gray-600 z-[-46]" />
  </div>
</template>

<style scoped lang="postcss">
img {
  @apply min-h-full md:min-h-[115%] 2xl:min-h-[125%];
}
.moving {
  @apply w-[110%] min-w-[100vh] max-w-none fixed top-0 md:top-[-15%] 2xl:top-[-25%] transition-all duration-500 ease-out;
}
</style>