<template>
  <footer
    class="footer"
    :class="{ [`footer-${type}`]: type }"
    :data-background-color="backgroundColor"
  >
    <div class="container">
      <nav>
        <ul>
          <li>
            <a href="https://www.margarethmaroto.com.br">
              Margareth Maroto
            </a>
          </li>
          <li>
            <a href="https:///presentation.creative-tim.com">
              Sobre nós
            </a>
          </li>
          <li>
            <a href="https:///blog.creative-tim.com">
              Blog
            </a>
          </li>
          <li>
            <a href="https://www.creative-tim.com/license">
              Licenças
            </a>
          </li>
        </ul>
      </nav>
      <div class="copyright">
        &copy; {{ year }}, feito pela equipe
        <a href="https://www.margarethmaroto.com.br" target="_blank">Margareth Maroto</a>
      </div>
    </div>
  </footer>
</template>
<script>
export default {
  props: {
    backgroundColor: String,
    type: String
  },
  data() {
    return {
      year: new Date().getFullYear()
    };
  }
};
</script>
<style></style>
