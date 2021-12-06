<template>
  <div class="all_content_container">
    <nav id="nav" class="quoter_nav">
      <router-link to="/" class="quoter_nav--route">Home</router-link>
      <router-link to="/info" class="quoter_nav--route">Info</router-link>
    </nav>
    <router-view />
    <footer id="footer" class="quoter_footer">
      <span class="quoter_footer--credits">
        Created by <a href="https://github.com/andreialexc30" class="footer_anchor">Andrei Caia</a> using VueJS
      </span>
    </footer>
  </div>
</template>