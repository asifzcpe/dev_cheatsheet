# Passing only single column value such as id in multiselect plugin in vue js
## When we bind a data variable to multiselect, all columns values are passed as object into the data variable but sometimes, we actually need only ids or a single value instead of object. Below is the trick to do it.

```js
<trmplate>
<multiselect v-model="selectedObjects"
    :options="options"
    :multiple="true" 
    label="name" 
    track-by="id">
</multiselect>
</template>
<script>
export default {
  data() {
    return {
      options: [
        {id: 1, name: 'Ashraf'},
        {id: 2, name: 'Imrul'},
        {id: 3, name: 'Razib'},
      ],
      selectedObjects: [],
      selectedIds: [],
    }
  },
  watch: {
    selectedObjects(newValues) {
      this.selectedIds = newValues.map(obj => obj.id);
    }
  }
}
</script>
```
