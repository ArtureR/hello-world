<template>
    <div class="searchWrapper">        
        <input id="search" name="search" v-model="searchValue" @input="handleInput"/>
         <ul>
            <li v-for="item in results" :key="item.data[0].nasa_id">
            <p>
                {{ item.data[0].description }}
            </p>
             </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'SearchInput',
};
</script>

<style lang="scss" scoped>
.searchWrapper {
    margin-top: 50px;
    display: flex;
    flex-direction: column;
    width: 250px;
  
    input {
      height: 30px;
      border: 0;
      border-bottom: 1px solid black;
      background: none;
    }
}
</style>

