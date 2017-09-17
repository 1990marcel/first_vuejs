<template>
  <div class="hello">
    <input type="text" v-model="title"><br>
    <h1>{{title}}</h1>
    <p v-if="showName">{{user.firstName}}</p>
    <ul>
      <li v-for="item in items">{{item.title}}</li><br>
    </ul>
    <label><input type="text" v-model="user.firstName"></label>
    <br>
    <label><input type="text" v-model="user.lastName"></label>
    <h3>{{fullName}}</h3>
    
  </div>
</template>

<script>
export default {
  name: 'test',
  data () {
    return {
      title: 'this is new',
      user: {
        firstName: 'marcel',
        lastName: 'Nwamadi'
      },
      showName: true,
      items: [
        {title: 'Item One'},
        {title: 'Item Two'},
        {title: 'Item Three'}
      ]
    }
  },
  methods: {
  },
  computed: {
    fullName: function () {
      return this.user.firstName + ' ' + this.user.lastName
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
ul {
  list-style-type: none;
  padding: 0;
}

</style>
