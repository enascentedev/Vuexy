<template>
  <header id="header">
    <i class="fas fa-search"></i>
    <div>
      <font-awesome-icon :icon="['fas', 'user']" />
      <font-awesome-icon :icon="['fas', 'bell']" />
      <font-awesome-icon :icon="['fas', 'circle-user']" />
			<font-awesome-icon icon="fa-solid fa-user-secret"/>

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
