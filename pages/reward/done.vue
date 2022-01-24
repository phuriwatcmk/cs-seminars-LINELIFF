        <template>
  <v-card
    class="mx-auto"
    max-width="344"
    outlined
  >
    <v-list-item three-line>
      <v-list-item-content>
        <div class="text-overline mb-4">
          Reward card
        </div>
        <v-list-item-title class="text-h5 mb-0">
          ส่วนลดเมื่อซื้อเครื่องดื่มที่ร้าน
        </v-list-item-title>
        <v-list-item-subtitle>Pak Cafe</v-list-item-subtitle>
        <v-list-item-subtitle class="text-h5 mt-2">Redeem Code : {{ val }} </v-list-item-subtitle>
      </v-list-item-content>

      <v-list-item-avatar
        tile
        size="80"
        color="grey"
      ></v-list-item-avatar>
    </v-list-item>

    <v-card-actions>

    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  mounted(){
    gen()
  },
  data(){
    return {
      val : ''
    }
  },
  methods: {
    gen(){
      this.val = Math.floor(1000 + Math.random() * 9000);
    }
  }
}
</script>

<style>

</style>