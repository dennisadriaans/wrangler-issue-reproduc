<script lang="ts" setup>
import { VisXYContainer, VisLine, VisAxis } from "@unovis/vue";

type DataRecord = { x: number; y: number };

const data: DataRecord[] = [
  { x: 0, y: 0 },
  { x: 1, y: 2 },
  { x: 2, y: 1 },
];
</script>

<template>
  <div>
    <TestSlot>
      <ClientOnly>
        <VisXYContainer :height="600">
          <VisLine :data="data" :x="(d) => d.x" :y="(d) => d.y" />
          <VisAxis type="x" />
          <VisAxis type="y" />
        </VisXYContainer>
      </ClientOnly>
    </TestSlot>
  </div>
</template>
