<template>
  <div>
    <img
      class="filezilla"
      src="/assets/filezilla.png"
      alt="filezilla logo"
    />
    <img
      class="old-website"
      src="/assets/old-website.png"
      alt="old website graphic"
    />
  </div>
</template>

<style>
.filezilla {
  position: absolute;
  left: 220px;
  top: 107px;
  width: 30%;
  z-index: 1;
}
.old-website {
  position: absolute;
  left: 450px;
  top: 150px;
  width: 30%;
  z-index: -1;
}
</style>
