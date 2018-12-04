<template>
  <form action>
    <div class="modal-card">
      <header class="modal-card-head">
        <p class="modal-card-title">New Visitor</p>
      </header>
      <section class="modal-card-body">
        <b-field label="First Name">
          <b-input type="text" v-model="firstName" placeholder="Enter first name" required></b-input>
        </b-field>

        <b-field label="Last Name">
          <b-input type="text" v-model="lastName" placeholder="Enter last name" required></b-input>
        </b-field>
      </section>
      <footer class="modal-card-foot">
        <button class="button is-primary" type="button" @click="saveAndClose">Save</button>
      </footer>
    </div>
  </form>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component({})
export default class NewVisitor extends Vue {
  firstName = null;
  lastName = null;

  saveAndClose() {
    (<any>this.$parent).close();
  }
}
</script>
