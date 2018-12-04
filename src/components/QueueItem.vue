<template>
  <div class="box queue-item">
    <article class="media">
      <div class="media-left">
        <figure class="image is-64x64">
          <img src="https://api.adorable.io/avatars/128/aboptt.png" alt="Image">
        </figure>
      </div>
      <div class="media-content">
        <div class="content">
          <p>
            <strong>John Smith</strong>
            <br>Phone cannot be restarted.
            <br>11:03
          </p>
        </div>
        <nav class="level is-mobile">
          <div class="level-left">
            <div class="level-item">
              <b-dropdown>
                <button class="button" slot="trigger">
                  <span>Click me!</span>
                  <b-icon icon="menu-down"></b-icon>
                </button>

                <b-dropdown-item>Action</b-dropdown-item>
                <b-dropdown-item>Another action</b-dropdown-item>
                <b-dropdown-item>Something else</b-dropdown-item>
              </b-dropdown>
            </div>
            <div class="level-item primary">
              <button class="button is-primary">Assign</button>
            </div>
          </div>
        </nav>
      </div>
    </article>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component({})
export default class QueueItem extends Vue {}
</script>

<style>
.queue-item {
  margin-top: 10px;
  margin-left: 10px;
}
</style>
