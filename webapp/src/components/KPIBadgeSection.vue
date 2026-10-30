<template>
  <h1>KPI essentielles</h1>
  <div class="all-kpis">
    <div class="kpi" v-for="{ label, value } in KPIs" :key="label">
      <p>
        <span class="label">{{ label }}</span> :
        <span class="value">{{ value }}</span>
      </p>
    </div>
  </div>
</template>

<script setup lang="ts">
import { reactive } from "vue";
import dayjs from "dayjs";

interface KPI {
  label: string;
  value: any;
}

const coffeeCountStartDate = dayjs("2019-09-01");

const KPIs = reactive<KPI[]>([
  {
    label: "Cafés consommés",
    value: dayjs().diff(coffeeCountStartDate, "day") * 3,
  },
]);
</script>

<style scoped>
.all-kpis {
  display: flex;
  flex-wrap: wrap;
}
.kpi {
  background-color: black;
  color: white;
  padding: 0.5rem 1rem;
  border-radius: 50px;
}

.label {
  color: gainsboro;
}
</style>
