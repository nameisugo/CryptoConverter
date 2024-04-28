<template>
    <input min="0" type="number" @input="changeAmount($event.target.value)" placeholder="Input value"><br>
    <button @click="convert()">Convert</button>
    <button @click="favourite()" className="favButton">Favourite</button>
</template>
  
<script>
export default {
    props: {
        changeAmount: {
            type: Function,
            required: true
        },
        convert: {
            type: Function,
            required: true
        },
        favourite: {
            type: Function,
            required: true
        }
    }
}
</script>
  
  
<style scoped>
input {
    outline: none;
    width: 500px;
    position: relative;
    top: -50px;
    font-size: 1.25em;
    border-radius: 5px;
    border: 3px solid rgb(255, 156, 74);
    padding: 15px 20px;
    background: #f5ee98;
    color: black;
}

button {
    position: relative;
    top: -20px;
    padding: 15px 20px;
    color: rgb(255, 255, 255);
    text-transform: uppercase;
    cursor: pointer;
    background: rgb(255, 156, 74);
    border: 0;
    border-radius: 20px;
    transition: transform 500ms ease;
}

button:hover {
    transform: scale(1.1) translateY(-5px);
}

button.favButton {
    background: rgb(0, 41, 70);
    margin-left: 5px;
}
  
</style>