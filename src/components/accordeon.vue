

<template>
<section class="faq">
        <h2 class="faq__title">Frequently asked questions</h2>
<div class="faq__accordeon">
  
</div>
</section>
</template>
<script>

export default {
  name: "Accordeon",
  data() {
    
  }}
  
</script>


<style lang="scss">
@import "../styles/core/vars.scss";
.faq {
  font-family: $main-font;
  min-height: 50vh;
  &__title {
    text-transform: uppercase;
  }
}


</style>