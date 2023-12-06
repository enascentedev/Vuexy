<template>
  <header id="header">
    <i class="fas fa-search"></i>
    <div>
      <i class="fas fa-user"></i>
      <i class="fas fa-bell"></i>
      <i class="fas fa-user-circle"></i>
    </div>
  </header>
</template>

<script>
export default {
  name: "Cabecalho",
};
</script>

<style lang="postcss" scoped>
#header {
  @apply flex justify-between items-center p-5 text-lg shadow-2xl
}

#header > i.fas.fa-search {
 
}

#header > div {
  @apply flex items-center gap-5;
}

#header > div > .fas {
  
}
</style>
