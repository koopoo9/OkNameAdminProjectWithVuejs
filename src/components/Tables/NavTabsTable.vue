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
  name: "nav-tabs-table",
  data() {
    return {
      selected: [],
      users: [
        {
          name: '2019년 7월 1일 02:00 ~ 04:00 휴대폰 본인확인 작업 안내'
        },
        {
          name: "2019년 7월 10일 02:00 ~ 04:00 휴대폰 본인확인 작업 안내"
        },
        {
          name: '2019년 7월 21일 02:00 ~ 04:00 휴대폰 본인확인 작업 안내'
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
