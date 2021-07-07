<template>
  <div class="card-series">
      <img :src="link.thumb" :alt="link.type">
      <h6>{{link.series}}</h6>
  </div>
</template>

<script>
export default {
    name: 'DcCard',
    props: ["link"]
}
</script>

<style lang="scss">
    .card-series{
        padding: 20px 0;

        img{
            width: 120px;
            height: 120px;
        }

        h6{
            color: white;
            text-transform: uppercase;
            margin-top: 5px;
        }
    }
</style>