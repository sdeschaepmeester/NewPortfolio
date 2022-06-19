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
            <a href="https://www.creative-tim.com">
              LinkedIn
            </a>
          </li>
          <li>
            <a href="mailto:deschaepmeester.samantha@gmail.com">
              Contactez-moi
            </a>
          </li>
          <li>
            <a href="https://www.creative-tim.com/license">
              Licences Creative Tim 
            </a>
          </li>
        </ul>
      </nav>
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
