<template>
  <header class="w-full text-sm">
    <div class="fixed top-0 left-0 h-16 w-full bg-white">
      <div class="navbar">
        <a href="/" class="flex h-full items-center text-xl">
          {{ company }}
        </a>

        <nav class="ml-12 h-full">
          <ul class="m-0 flex h-full list-none p-0">
            <li
              v-for="menu in menuItems"
              class="ml-9 h-full first:ml-0"
              :key="menu.id"
              data-test="menu-list-item"
            >
              <a :href="menu.url" class="flex h-full items-center py-2.5">
                {{ menu.name }}
              </a>
            </li>
          </ul>
        </nav>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'MainNav',
  data() {
    return {
      company: 'Eclectic Careers',
      menuItems: [
        { id: 1, name: 'Teams', url: '#' },
        { id: 2, name: 'Locations', url: '#' },
        { id: 3, name: 'Life at Eclectic Corp', url: '#' },
        { id: 4, name: 'How we hire', url: '#' },
        { id: 5, name: 'Students', url: '#' },
        { id: 6, name: 'Jobs', url: '#' }
      ]
    };
  }
};
</script>

<style scoped>
.navbar {
  @apply mx-auto flex h-full flex-nowrap border-b border-solid border-brand-gray-1 px-8;
}
</style>
