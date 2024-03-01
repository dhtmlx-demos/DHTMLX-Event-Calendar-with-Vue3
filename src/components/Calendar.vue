<script>
import { EventCalendar } from "@dhx/trial-eventcalendar";
import "@dhx/trial-eventcalendar/dist/event-calendar.css";

export default {
  props: ["events", "date"],

  mounted() {
    new EventCalendar(this.$refs.cont, {
      events: this.events,
      date: this.date,
    });
  },
  unmounted() {
    this.$refs.cont.innerHTML = "";
  },
};
</script>

<template>
  <div ref="cont" style="width: 100%; height: 100%"></div>
</template>
