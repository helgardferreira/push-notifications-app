<template>
  <q-page class="flex flex-center">
    <div>
      <img alt="Quasar logo" src="~assets/quasar-logo-full.svg" />

      <q-dialog v-model="alert" full-width>
        <q-card>
          <q-card-section>
            <div class="text-h6">{{ submitStatus }}</div>
          </q-card-section>

          <q-card-section>{{ submitMessage }}</q-card-section>

          <q-card-actions align="right">
            <q-btn label="OK" color="primary" v-close-popup />
          </q-card-actions>
        </q-card>
      </q-dialog>
    </div>
  </q-page>
</template>

<style></style>

<script>
export default {
  name: "PageIndex",
  data() {
    return {
      alert: false,
      submitStatus: "",
      submitMessage: ""
    };
  },
  created() {
    this.alert = true;
    this.submitStatus = "Trace";
    this.submitMessage = window.PushNotification.init;
  }
};
</script>
