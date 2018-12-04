<template>
  <div id="app">
    <nav class="navbar is-warning" role="navigation" aria-label="main navigation">
      <div class="navbar-menu">
        <div class="navbar-start">
          <router-link to="/" class="navbar-item">Home</router-link>
          <router-link to="/about" class="navbar-item">About</router-link>
        </div>
        <div class="navbar-end">
          <div class="navbar-item">
            <div class="buttons">
              <button
                class="button is-primary"
                @click="isModalActive = true">New Visitor</button>
            </div>
          </div>
        </div>
      </div>
    </nav>

    <router-view/>

    <b-modal :active.sync="isModalActive" has-modal-card>
      <new-visitor />
    </b-modal>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import NewVisitor from "@/components/NewVisitor.vue";

@Component({
  components: {
    NewVisitor
  }
})
export default class App extends Vue {
  isModalActive = false;
}
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
