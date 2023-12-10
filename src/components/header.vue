<template>
  <header id="header">
    <i class="fas fa-search"></i>
    <div>
      <font-awesome-icon :icon="['fas', 'user']" />
      <font-awesome-icon :icon="['fas', 'bell']" />
      <font-awesome-icon :icon="['fas', 'circle-user']" />

    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style lang="postcss" scoped>
#header {
  @apply flex justify-between items-center py-8 text-lg rounded-lg bg-white;
}

#header > i.fas.fa-search {
 @apply pl-5
}

#header > div {
  @apply flex items-center gap-5 pr-5;
}

#header > div > .fas {
  
}
</style>
