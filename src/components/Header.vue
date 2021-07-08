<template>
  <div class="logo">
    <img src="@/assets/img/logo.png" alt="logo spotify">
  </div>
</template>

<script>
export default {
    name: 'Header',
}
</script>

<style lang="scss" scoped>

.logo
{
    background-color: #2e3a46;
    height: 80px;
    padding: 18px;

    img
    {
        width: 3%;
        margin-left: 30px;
    }
}

</style>