<template>
  <section>
      <div class="container">
          <h3>Content goes here</h3>
      </div>
  </section>
</template>

<script>
export default {
    name: 'Content',
}
</script>

<style lang="scss" scoped>
    @import '../style/var.scss';

    section{
        background-color: $black-ground;
        height: 80px;
    }

    h3{
        color: white;
        line-height: 80px;
    }

</style>