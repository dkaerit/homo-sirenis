<template>
  <Bar/>
  <div class="wrap md-2-11 sm-1-12 xs-1-12 ">
    <Header/>
    <div class="contain">
      <h1>Aparato locomotor</h1>
      <Markdown :source="home" class="setp meskeletal"/>
      <router-link to="/" tag="button" class="button-back">Atrás</router-link>
    </div>
    
  </div>
</template>

<script>
import Bar from "@/components/Bar.vue";
import Header from "@/components/Header.vue";
import Markdown from 'vue3-markdown-it';
import home_md from '@/markdown/meskeletal.md';
import $ from 'jquery';

export default {
  name: 'Meskeletal',
  data: function() {
    return {
      home: home_md,
    }
  },
  methods: {
  },
  components: { Bar, Header, Markdown },
  async mounted() {

  },

}
</script>

<style lang="scss">
.meskeletal {
  column-count: 1;
  img {
    width: 30%;
  }
}
</style>
