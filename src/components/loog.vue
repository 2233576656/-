<template>
  <div class="loog">小元</div>
</template>

<script>
export default {

}
</script>

<style>
.loog{
    width: 10%;
    height: 100%;
    /* border: 1px solid red; */
    font-size: 220%;
    color: rgb(79, 179, 250);
    -webkit-mask-image:-webkit-gradient(linear, 0 0, 0 bottom, from(rgb(79, 179, 250)), to(rgba(0, 0, 255, 0)));
    font-weight: bold;
    text-align: center;
    line-height: 70px;
    /* margin: 0 5%; */
    font-style: italic;
    text-shadow: 3px 3px 3px #5e5b5b;
}
@media only screen and (max-width: 600px) {
  .loog{
    width: 12%;
    margin: 0 2%;
    line-height: 5rem;
    /* font-size: 1rem; */
  }
}
</style>