<template>
  <button :class="['button','hover', 'hover__press',
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
    background: $primary-blue;
    border: none;
    padding: 1rem 2rem;
    font-family: $headline-regular;
    text-transform: uppercase;
    cursor: pointer;
    filter: drop-shadow(0 10px 0 rgba(0,0,0,0.5));
    transition: all 0.1s ease;
    color: white;
    border-radius: 4px;
}

.hover:hover,.hover__press:hover {
  filter: drop-shadow(0 0 0 #15111a);
  transform: translate(0, 10px);
  clip-path: inset(0% 0 0% 0 round 10px);
}


.press:active {
  filter: drop-shadow(0 0 0 #15111a);
  transform: translate(0, 10px);
}


.hover__press:active {
  filter: drop-shadow(0 -10px 0 #1b1621);
  transform: translate(0, 20px);
  
  clip-path: inset(-20% 0 13% 0 round 10px);
  
  background-color: #3c3047;
}

.xl{
    font-size: 2.5rem;
    @media only screen and (max-width: $tablet) {
        font-size: 1.5rem;
      }
}

.l{
}

.m{

}



</style>
