<template>
  <div class="input">
    <i class="fa fa-search icon"></i>
    <input class="input-field" placeholder="Search Videos" @change="onChange" />
  </div>
</template>

<script>
export default {
  name: "SearchBar",
  methods: {
    onChange: function(event) {
      this.$emit("termChange", event.target.value);
    },
  },
};
</script>

<style scoped>
input {
  width: 75%;
}
div {
  text-align: center;
  margin: 20px;
}
.fa {
  color: #aaa;
}
.input-field {
  width: 100%;
  padding: 4px 10px 5px 35px;
  text-align: left;
}
.input i {
  position: absolute;
}

.input {
  width: 100%;
  margin-bottom: 10px;
}

.icon {
  padding: 10px;
  min-width: 40px;
}
</style>
