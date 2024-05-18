<template>
  <div>
    <h1 class="text-3xl mb-4">Parent Component</h1>
    <grandfather-component @sendData="showNotification" />
    <grandmother-component @sendData="showNotification" />
    <uncle-component @sendData="showNotification" />
    <aunt-component @sendData="showNotification" />
    <child-component @sendData="showNotification" />

    <notification-component
      :isVisible="isNotificationVisible"
      :message="notificationMessage"
      @close="isNotificationVisible = false"
    />

    <div class="mt-4">
      <slot></slot>
    </div>
  </div>
</template>

<script>
import GrandfatherComponent from './GrandfatherComponent.vue';
import GrandmotherComponent from './GrandmotherComponent.vue';
import UncleComponent from './UncleComponent.vue';
import AuntComponent from './AuntComponent.vue';
import ChildComponent from './ChildComponent.vue';
import NotificationComponent from './NotificationComponent.vue';

export default {
  components: {
    GrandfatherComponent,
    GrandmotherComponent,
    UncleComponent,
    AuntComponent,
    ChildComponent,
    NotificationComponent,
  },
  data() {
    return {
      isNotificationVisible: false,
      notificationMessage: '',
    };
  },
  methods: {
    showNotification(message) {
      this.notificationMessage = message;
      this.isNotificationVisible = true;
    },
  },
};
</script>

<style scoped>
h1 {
  color: #FFFBF0;
}
</style>
