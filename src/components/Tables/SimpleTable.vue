<template>
  <div>
    <md-table v-model="users" :table-header-color="tableHeaderColor">
      <md-table-row slot="md-table-row" slot-scope="{ item }">
        <md-table-cell md-label="회원사명">{{ item.name }}</md-table-cell>
        <md-table-cell md-label="회원사코드">{{ item.cpCd }}</md-table-cell>
        <md-table-cell md-label="사용일">{{ item.dt }}</md-table-cell>
        <md-table-cell md-label="서비스 구분코드">{{ item.svc }}</md-table-cell>
        <md-table-cell md-label="명의 인증 성공 건수">{{ item.suc }}</md-table-cell>
        <md-table-cell md-label="최종 인증 성공 건수">{{ item.finalSuc }}</md-table-cell>
        <md-table-cell md-label="총 건수">{{ item.total }}</md-table-cell>
      </md-table-row>
    </md-table>
  </div>
</template>

<script>
export default {
  name: "simple-table",
  props: {
    tableHeaderColor: {
      type: String,
      default: ""
    }
  },
  data() {
    return {
      selected: [],
      users: [

            {
              name: 'KCB',
              cpCd: 'K00001111000',
              dt: '2019/08/01',
              svc: '12',
              suc: 4,
              finalSuc: 2,
              total : 12
            },
            {
              name: 'KCB',
              cpCd: 'K00001111000',
              dt: '2019/08/01',
              svc: '10',
              suc: 3,
              finalSuc: 1,
              total : 10
            },
                        {
              name: 'KCB',
              cpCd: 'K00001111000',
              dt: '2019/08/01',
              svc: '11',
              suc: 2,
              finalSuc: 0,
              total : 4
            },
            {
              name: 'KCB',
              cpCd: 'K00001111000',
              dt: '2019/08/02',
              svc: '10',
              suc: 3,
              finalSuc: 1,
              total : 10
            },
            {
              name: 'KCB',
              cpCd: 'K00001111000',
              dt: '2019/08/02',
              svc: '03',
              suc: 1,
              finalSuc: 1,
              total : 2
            },
            {
              name: 'KCB',
              cpCd: 'K00001111000',
              dt: '2019/08/03',
              svc: '10',
              suc: 3,
              finalSuc: 1,
              total : 10
            },
            {
              name: 'KCB',
              cpCd: 'K00001111000',
              dt: '2019/08/04',
              svc: '10',
              suc: 2,
              finalSuc: 2,
              total : 5
            },
            {
              name: 'KCB',
              cpCd: 'K00001111000',
              dt: '2019/08/05',
              svc: '10',
              suc: 17,
              finalSuc: 10,
              total : 30
            },
            {
              name: 'KCB',
              cpCd: 'K00001111000',
              dt: '2019/08/06',
              svc: '10',
              suc: 3,
              finalSuc: 3,
              total : 12
            },
            {
              name: 'KCB',
              cpCd: 'K00001111000',
              dt: '2019/08/07',
              svc: '10',
              suc: 7,
              finalSuc: 1,
              total : 22
            },
            {
              name: 'KCB',
              cpCd: 'K00001111000',
              dt: '2019/08/08',
              svc: '10',
              suc: 3,
              finalSuc: 1,
              total : 10
            },
            {
              name: 'KCB',
              cpCd: 'K00001111000',
              dt: '2019/08/09',
              svc: '10',
              suc: 3,
              finalSuc: 1,
              total : 10
            },
            {
              name: 'KCB',
              cpCd: 'K00001111000',
              dt: '2019/08/10',
              svc: '10',
              suc: 3,
              finalSuc: 1,
              total : 10
            },
            {
              name: 'KCB',
              cpCd: 'K00001111000',
              dt: '2019/08/11',
              svc: '10',
              suc: 3,
              finalSuc: 1,
              total : 10
            },
            {
              name: 'KCB',
              cpCd: 'K00001111000',
              dt: '2019/08/12',
              svc: '10',
              suc: 3,
              finalSuc: 1,
              total : 10
            },
            {
              name: 'KCB',
              cpCd: 'K00001111000',
              dt: '2019/08/13',
              svc: '10',
              suc: 3,
              finalSuc: 1,
              total : 10
            },
            {
              name: 'KCB',
              cpCd: 'K00001111000',
              dt: '2019/08/14',
              svc: '10',
              suc: 3,
              finalSuc: 1,
              total : 10
            },
            {
              name: 'KCB',
              cpCd: 'K00001111000',
              dt: '2019/08/15',
              svc: '10',
              suc: 3,
              finalSuc: 1,
              total : 10
            },
            {
              name: 'KCB',
              cpCd: 'K00001111000',
              dt: '2019/08/16',
              svc: '10',
              suc: 3,
              finalSuc: 1,
              total : 10
            }
      ]
    };
  }
};
</script>
