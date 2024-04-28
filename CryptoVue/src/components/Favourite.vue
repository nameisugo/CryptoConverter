<template>
    <h2>Options of favourites</h2>
    <div @click="getFromFavs(index)" v-for="(el, index) in favs" :key="index">
       <span>{{ el.from }}</span>
       <span>{{ el.to }}</span>
    </div>
</template>
  
<script>
export default {
    props: {
        favs: {
            type: Array,
            required: true
        },
        getFromFavs: {
            type: Function,
            required: true
        }
    }
}
</script>
  
  
<style scoped>
h2 {
    color: rgb(255, 255, 255);
}

div {
    display: flex;
    justify-content: space-between;
    width: 400px;
    margin: 3px auto;
    transition: all 500ms ease;
}

span {
    padding: 10px 15px;
    background: rgb(0, 41, 70);
    color: white;
    border-radius: 10px;
}

div:hover {
    opacity: 0.7;
    transform: scale(1.1);
    cursor: pointer;
}
</style>