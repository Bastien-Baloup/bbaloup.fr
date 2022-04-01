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
  <!-- Background -->
  <div class="fixed top-0 left-0 right-0 bottom-0 overflow-hidden brightness-90">
    <img src="/assets/W_1/layer_0.png" alt class="min-h-full min-w-full fixed top-0 -z-50" />
    <img
      src="/assets/W_1/layer_1.0.png"
      alt
      class="min-h-full min-w-[110%] fixed top-[-10%] left-[-5%] z-[-49] transition-all duration-500 ease-out"
      style="transform: translate3d(calc(var(--shiftX) * -2%), calc(var(--shiftY) * -2%), 0);"
    />
    <img
      src="/assets/W_1/layer_2.0.png"
      alt
      class="min-h-full min-w-[110%] fixed top-[-10%] left-[-5%] z-[-48] transition-all duration-500 ease-out"
      style="transform: translate3d(calc(var(--shiftX) * -1%), calc(var(--shiftY) * -1%), 0);"
    />
    <img src="/assets/W_1/layer_3.0.png" alt class="min-h-full min-w-full fixed top-[-10%] z-[-47]" />
    <img
      src="/assets/W_1/layer_4.0.png"
      alt
      class="min-h-full min-w-[110%] fixed top-[-10%] left-[-5%] z-[-46] transition-all duration-500 ease-out"
      style="transform: translate3d(calc(var(--shiftX) * 1%), calc(var(--shiftY) * 1%), 0);"
    />
    <img
      src="/assets/W_1/layer_5.1.png"
      alt
      class="min-h-full min-w-[110%] fixed top-[-10%] left-[-5%] z-[-45] transition-all duration-500 ease-out"
      style="transform: translate3d(calc(var(--shiftX) * 2%), calc(var(--shiftY) * 2%), 0);"
    />
    <div class="h-[3%] w-full fixed bottom-0 bg-purple-gray-600" />
  </div>
</template>
