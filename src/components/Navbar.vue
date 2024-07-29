<template>
       <header>
        <nav>
            <RouterLink to="/">DoinStuff</RouterLink>
            <div class="dropdown">
                <button @click="toggleDropdown">Articles</button>
                <div class="dropdown-options" v-if="dropdownOpen">
                    <RouterLink to="/search/Dev">Dev</RouterLink>
                    <RouterLink to="/search/Fitness">Fitness</RouterLink>
                    <RouterLink to="/search/Lifestyle">Lifestyle</RouterLink>
                    <RouterLink to="/search/Business">Business</RouterLink>
                </div> 
            </div>
            <RouterLink to="/people">People</RouterLink>
            <RouterLink to="/about">About</RouterLink>
        </nav>
    </header>
</template>

<script setup>
import { ref } from 'vue';

var dropdownOpen = ref(false);
var toggleDropdown = () => {
    dropdownOpen.value = !dropdownOpen.value;
}
</script>



<style>
header{
    
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}
@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>