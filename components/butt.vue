<template>
  <div v-motion :initial="{ x: -80 }" :enter="{ x: 10 }">
    <img
      class="butt"
      src="https://res.cloudinary.com/defkmsrpw/image/upload/q_auto,f_auto/v1614936696/scottspence.com/buttbutt.png"
      alt="butt butt"
    />
  </div>
</template>

<style scoped>
.butt {
  position: absolute;
  left: 150px;
  top: -240px;
  width: 70%;
}
</style>
