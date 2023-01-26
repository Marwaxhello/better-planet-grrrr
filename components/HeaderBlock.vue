<template>
  <div class="header-block">
    <h4>{{ text }}</h4>
  </div>
</template>

<script>
export default {
  name: 'TextBlock',
  props: ['text'],
}
</script>

<style lang="scss" scoped>
.header-block {
  display: flex;
  justify-content: center;
  align-items: center;
  text-transform: uppercase;
  background: $primary-blue;
  margin-bottom: 3rem;
  border-radius: 4px;
  color: $primary-green;


      @media only screen and (max-width: $tablet) {
        margin-bottom: 1.5rem;
        text-align: center;
      }
}

.header-block h4 {
  font-size: 2rem;
  // color: black;

      @media only screen and (max-width: $tablet) {
        font-size: 1.5rem;
      }
}
</style>
