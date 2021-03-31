<template>
  <div class="hello">
    <div class="container mt-5 mr-5">
      <div class="row mr-4">
        <h1>{{ msg }}</h1>
          <div class="col-md-8 col-sm-4 mt-4">
                <div class="input-group mb-3">
                  <span class="input-group-text" id="basic-addon1">@</span>
                  <input type="text" class="form-control" v-model="username" placeholder="Username" aria-label="Username" aria-describedby="basic-addon1">
                </div>
                <button type="button" @onclick="Save()" class="btn btn-warning">Submit</button>
          </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },  
  data() {
      return {
        username: null,
      }
  },
  methods: {
    Save(){
      console.log(this.username);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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

</style>
