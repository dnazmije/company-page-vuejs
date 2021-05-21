<template>
  <div>
    <p><small>Sort by: {{currentSort.toUpperCase()}}</small></p>
  </div>
  <table>
    <tr>
      <th v-for='(title, index) in titles' :key='index'
        @click='sortedProducts(title)' >
        {{ title.toUpperCase() }}
      </th>
    </tr>

    <tr v-for='(product, index) in products' :key='index'>
      <td>{{ product.title }}</td>
      <td>{{ product.type }}</td>
      <td>{{ product.description }}</td>
      <td>{{ product.filename }}</td>
      <td>{{ product.height }}</td>
      <td>{{ product.width }}</td>
      <td>{{ product.price }}</td>
      <td>{{ product.rating }}</td>
    </tr>
  </table>
</template>

<script>
import data from '../data/data.json';

export default {
  name: 'ProductsTable',
  data() {
    return {
      products: data.products,
      titles: null,
      currentSort: 'title',
      sorted: null,
    };
  },
  created() {
    this.getTitles();
    this.sorted = this.sortedProducts(this.currentSort);
  },
  methods: {
    getTitles() {
      this.titles = Object.keys(this.products[0]);
    },
    sortTitle(item) {
      this.currentSort = item;
      console.log(this.currentSort);
    },

    sortedProducts(item) {
      this.sortTitle(item);
      this.products.sort((a, b) => {
        let firstItem = a[item];
        let secondItem = b[item];
        if (firstItem < secondItem)  return -1;
        if (firstItem > secondItem)  return 1;
        return 0;
      });
    },
  },
};
</script>

<style scoped>
table {
  border-collapse: collapse;
  width: 100%;
}

table td, 
table th {
  border: 1px solid #999999;
  padding: 8px;
}

table tr:nth-child(even) { 
  background-color: #f9f9f9;
}

table tr:nth-child(odd) { 
  background-color: #ddecf0;
}

table th {
  padding: 16px 8px;
  color: #def3f7;
  background-color: #04778b;
  text-align: left;
}
</style>
