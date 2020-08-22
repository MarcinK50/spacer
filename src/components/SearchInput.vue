<template>
    <input id="search"
           name="search"
           :value="value"
           @input="handleChange"
     />
</template>
<script>
export default {
  name: 'SearchInput',
  props: {
    value: {
      type: String,
      required: true,
    },
  },
  methods: {
    handleChange(e) {
      this.$emit('input', e.target.value);
    },
  },
};
</script>
<style lang="scss" scoped>
    input {
      margin-top: 50px;
      display: flex;
      width: 300px;
      color: white;
      text-align: center;
      font-size: 18px;
      font-weight: 300;
      height: 50px;
      border: 0;
      background: none;
      border-bottom: 1px solid #fff;
      transition: box-shadow .3s ease-out;
    }
    input:focus {
      outline: none;
      box-shadow: 0 10px 20px -8px rgba(255, 255, 255, .5);
    }
</style>
