<template>
  <div>
    <md-table v-model="users" @md-selected="onSelect">
      <md-table-row
        slot="md-table-row"
        slot-scope="{ item }"
      >
        <md-table-cell>{{ item.name }}</md-table-cell>
      </md-table-row>
    </md-table>
  </div>
</template>

<script>
export default {
  name: "nav-tabs-table2",
  data() {
    return {
      selected: [],
      users: [
        {
          name: 'SKT 갑질 논란에 대한 공식 사과문'
        },
        {
          name: "KT 채용 비리 사과문"
        },
        {
          name: 'LGU 장애 보고서'
        }
      ]
    };
  },
  methods: {
    onSelect: function(items) {
      this.selected = items;
    }
  }
};
</script>
