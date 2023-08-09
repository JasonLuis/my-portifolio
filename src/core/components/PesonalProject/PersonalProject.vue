<template>
  <q-card class="no-shadow">
    <div class="row justify-center">
      <q-img :src="getImage(props.image)" class="rounded-borders" />
    </div>
    <q-card-section>
      <div class="text-h6 text-center">
        {{ props.name }}
      </div>
    </q-card-section>
    <q-card-section class="q-pt-none text-center">
      <span> {{ props.description }} </span>
    </q-card-section>
  </q-card>
</template>

<script setup lang="ts">

const props = defineProps<{
  image: string;
  name: string;
  description: string;
}>()

const getImage = (image: string) => {
  const getImage = new URL(`../../assets/images/projects/${image}`, import.meta.url).href
  return getImage
}
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
    -webkit-background-clip: text; /* Para navegadores baseados em WebKit (Chrome, Safari) */
    -moz-background-clip: text; /* Para navegadores baseados em Gecko (Firefox) */
    background-clip: text;
    color: transparent;
}

.q-card {
    width: 267px;
    background-color: transparent;
    border: 0px;
    align-items: center;
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
.q-img {
    width: 267px;
    height: 234px;
}

</style>
