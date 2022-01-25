<template>
<div>
    <v-app-bar
      color="#655D8A"
      dense
      flat
      dark
    >
    <v-toolbar-title>Reward Card</v-toolbar-title>
    </v-app-bar>
        <v-container class="pt-0 pb-0">
      <v-row>
        <v-col>
  <v-card
    class="mx-auto justify-center"
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
            <v-btn class="w-100 text-center my-btn outlined text-primary mt-5" @click="close">Close</v-btn>                    
    </v-card-actions>
  </v-card>
        </v-col>
      </v-row>
        </v-container>
  </div>
</template>

<script>
export default {
  async mounted(){
    await this.gen()
  },
  data(){
    return {
      val : null
    }
  },
  methods: {
    gen(){
      this.val = Math.floor(1000 + Math.random() * 9000);
    },
    close(){
      liff.closeWindow();
    }
  }
}
</script>

<style>

</style>