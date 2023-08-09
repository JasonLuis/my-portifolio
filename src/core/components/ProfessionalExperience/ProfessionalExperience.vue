<template>
  <q-card class="no-shadow">
    <q-card-section>
      <div class="text-h6 text-start">
        {{ props.name }}
      </div>
    </q-card-section>
    <q-card-section class="q-pt-none text-start">
      <span> {{ props.description }} </span>
    </q-card-section>
  </q-card>
</template>

<script setup lang="ts">

const props = defineProps<{
  name:string;
  description:string;
}>()
</script>

<style scoped lang="scss">
%inconsolata {
    font-family: "Inconsolata";
}

%fira-sans {
    font-family: 'Fira Sans';
}
%text-gradient {
    background: linear-gradient(320deg, #0087ff 0, #5080ff 6.25%, #7c78ff 12.5%, #9b6ffd 18.75%, #b465f1 25%, #c85be4 31.25%, #d951d5 37.5%, #e746c6 43.75%, #f23cb5 50%, #fa33a4 56.25%, #ff2d93 62.5%, #ff2c81 68.75%, #ff2e70 75%, #ff355f 81.25%, #ff3e4f 87.5%, #fb483e 93.75%, #f4522e 100%);
    -webkit-background-clip: text;
    -moz-background-clip: text;
    background-clip: text;
    color: transparent;
}

.q-card {
    width: 273px;
    height: 480px;
    background-color: #382444;
}

.q-card__section {
    @extend %fira-sans;
    color: #DAD1E6;
    font-weight: 400;
    &:deep(.text-h6) {
        @extend %inconsolata;
        @extend %text-gradient;
        font-size: 22px;
        font-weight: 700;
    }
    &:deep(span){
      font-size: 18px;
    }
}

@media (max-width: $breakpoint-sm) {

  .q-card {
    width: 260px;
    height: 380px;
    background-color: #382444;
  }

  .q-card__section {
    &:deep(.text-h6) {
      font-size: 18px;
      line-height: 23px;
    }
    &:deep(span){
      font-size: 12px;
    }
  }
}
</style>
