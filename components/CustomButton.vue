<template>
  <button :class="['button',
    {'medium': medium},
    {'xl': xl},
    {'l': l}]">{{ label }}
</button>
</template>

<script>
export default {
    name: 'Button',
    props: ['label', 'medium', 'xl', 'l']
}
</script>

<style lang="scss">

.button {
    background: $primary-green;
    border: none;
    padding: 1rem 2rem;
    font-family: $headline-regular;
    text-transform: uppercase;
}

.xl{
    font-size: 3rem;
    @media only screen and (max-width: $tablet) {
        font-size: 1.5rem;
      }
}

.l{
}

.m{

}



</style>
