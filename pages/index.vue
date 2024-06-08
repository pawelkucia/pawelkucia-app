<template>
    <div>
        <div class="social-cover"></div>
        <div class="dark-layer"></div>

        <div class="profile-details flex flex-col items-center justify-center gap-10">
        <img src="/img/pawel-kucia.jpg" class="">
        <h1 class=" text-black dark:text-white">{{ name }}</h1>
        </div>
    </div>
</template>

<script setup>
    let name = 'Pawel Kucia'
</script>

<style lang="scss">
.social-cover {
  position: fixed;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  width: 100%;
  height: 100vh;
  /* background-image: url(/img/pawel-kucia-bg.jpg); */
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  transition: background-color 0.3s ease-in-out;
}

.dark {
    .social-cover {
        // background-image: url(/img/pawel-kucia-bg.jpg);
        background-color: #000000;
    }
}

.light {
    .social-cover {
        // background-image: url(/img/pawel-kucia-bg-light.jpg);
        background-color: #ffffff;
    }

    .dark-layer {
        background-color: rgba(0,0,0, 0.2);
    }
}

.dark-layer {
  position: fixed;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  width: 100%;
  height: 100vh;
  background-color: rgba(0,0,0, 0.4);
  z-index: 2;
  //backdrop-filter: blur(10px);
}

.profile-details  {
  position: absolute;
  color: white;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 3;
  width: 100%;
  padding: 20px;
  text-align: center;

  img {
    width: 300px;
    height: 300px;
    border-radius: 50%;
    object-fit: cover;
  }

}
</style>