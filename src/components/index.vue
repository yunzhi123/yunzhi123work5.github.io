<template>
  <div id="app">
  <h1 id="title" > 白吐司價格查詢 </h1>

  <form id="products" >
    <label for="date">日期:</label>
    <input type="text" id="date" name="date">
    <label for="product_name">商品名稱:</label>
    <input type="text" id="product_name" name="product_name">
    <label for="price">價格:</label>
    <input type="text" id="price" name="price">

    <button type="submit">Submit</button>
  </form>

  <p id="log"></p>

  <button name="show" id="showdata" >顯示資料</button>

  <table id="table"></table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      date: '',
      product_name: '',
      price: '',
    }
  },

  method: {
    addItem() {
      let item = {
        Date: this.date,
        product: this.product_name,
        Price: this.Price
      }
      this.table.push(item);
      this.date = '';
      this.product_name = '';
      this.price = '';
    }
  }
}
</script>

<style scoped>

</style>