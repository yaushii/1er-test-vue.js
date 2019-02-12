<template>
  <div class="promotion">
    <h1>{{ promotion.name }}</h1>
    <input type="text" v-model="promotion.name">
    <div> {{ promotion.id }}
      - Début: {{ promotion.startDate }}
      - Fin: {{ promotion.endDate }}</div><br>
      <Student 
      v-for="(studentURL, index) in promotion.students" 
      v-bind:myURL="studentURL" 
      v-bink:key="index"></Student>
    
  </div>
</template>

<script>
import Student from './Student'

  export default {
    name: 'Promotion',
    props: {
      promotion: Object,
    },

    components: {
        Student,
    },

    methods: {
      update(event) {
        console.log(event.target.value);
      }
    }
  };

</script>

<style scoped>
  .promotion {
    margin: 10px;
    background-color: #D499B9;
    border: solid 1px black;
    margin-left: 10em;
    margin-right: 10em;
  }

  .champ {
    margin-bottom: 15px;
  }

</style>
