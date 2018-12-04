<template>
  <b-table
    :data="isEmpty ? [] : data"
    :striped="isStriped"
    :hoverable="isHoverable"
    :loading="isLoading"
  >
    <template slot-scope="props">
      <b-table-column field="firstName" label="First Name">{{ props.row.firstName }}</b-table-column>

      <b-table-column field="lastName" label="Last Name">{{ props.row.lastName }}</b-table-column>
      
      <b-table-column field="agent.name" label="Agent">{{ props.row.agent.name }}</b-table-column>

      <b-table-column field="date" label="Date" centered>
        <span class="tag is-success">{{ new Date(props.row.date).toLocaleDateString() }}</span>
      </b-table-column>
    </template>

    <template slot="empty">
      <section class="section">
        <div class="content has-text-grey has-text-centered">
          <p>
            <b-icon icon="emoticon-sad" size="is-large"></b-icon>
          </p>
          <p>Nothing here.</p>
        </div>
      </section>
    </template>
  </b-table>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component({})
export default class ActiveVisits extends Vue {
  data = [
    {
      id: 1,
      firstName: "Jesse",
      lastName: "Simmons",
      agent: {
          name: "Agent Smith"
      },
      date: "2016/10/15 13:43:27"
    },
    {
      id: 2,
      firstName: "John",
      lastName: "Jacobs",
      agent: {
          name: "Agent Smith"
      },
      date: "2016/12/15 06:00:53"
    },
    {
      id: 3,
      firstName: "Tina",
      lastName: "Gilbert",
      agent: {
          name: "Agent Smith"
      },
      date: "2016/04/26 06:26:28"
    },
    {
      id: 4,
      firstName: "Clarence",
      lastName: "Flores",
      agent: {
          name: "Agent Smith"
      },
      date: "2016/04/10 10:28:46"
    },
    {
      id: 5,
      firstName: "Anne",
      lastName: "Lee",
      agent: {
          name: "Agent Smith"
      },
      date: "2016/12/06 14:38:38"
    }
  ];
}
</script>
