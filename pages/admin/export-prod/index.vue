<!-- <template>
  <layout>
    <div class="card-container">
      <div class="title-card">
        <h3 class="text-title">Danh sách xuất hàng</h3>
      
      </div>
      <!--  -->
      <!--
      <tableCustom
        :header="headerTable"
        :content="contentTable"
        :loadingTable="loadingTable"
        @reloadTable="reloadFetchData"
      />
    </div>
  </layout>
</template>

<script>
import tableCustom from "~/components/admin/export/tableCustom.vue";
import layout from "~/layouts/indexAdmin.vue";
export default {
  components: { layout, tableCustom },
  data() {
    return {
      loadingTable: false,
      headerTable: [
        {
          name: "Xuất hàng",
          width: "200px",
          align: "left",
        },
        {
          name: "Số lượng xuất kho",
          width: "200px",
          align: "left",
        },
        {
          name: "Ngày xuất",
          width: "150px",
          align: "center",
        },
      ],
      contentTable: [],
    };
  },
  watch: {},
  mounted() {
    this.$emit("pagePath", "/admin/export-prod");
    this.fetchExport();
  },
  methods: {


    async fetchExport() {
      this.loadingTable = true;
      const url = process.env.API_SERVER;
      const response = await this.$axios.get(url + "/prod/list-export");
      if (response.data && response.data.success == true) {
        console.log("get data res export", response.data);
        this.contentTable = response.data.data;
        setTimeout(() => {
          this.loadingTable = false;
        }, 1500);
      }
    },

    reloadFetchData(event) {
      if (event == true) {
        this.fetchCategory();
      }
    },
  },
};
</script>
<style lang="scss" scoped>
.title-card {
  margin-bottom: 20px;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  .text-title {
    margin-bottom: 0;
    font-size: 18px;
    font-weight: bold;
  }
}
</style>
-->