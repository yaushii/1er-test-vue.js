<template>
    <div class="container">
        <div class="row">
        <h1>Gestion de promotion</h1>
            <h2 class="purple">{{firstmessage}}</h2>
        </div>
    </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      msg: 'Hello world',
      firstmessage: 'Bosse un peu',
    };
  },
};
</script>

<style scoped>
h1, h2 {
  font-weight: normal;
  font-size:90px;
  
}
h2{
  border: 1px solid black;
  margin-left: 10em;
  margin-right: 10em;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.purple {
  color: purple;
  font-size: 50px;
}
</style>
