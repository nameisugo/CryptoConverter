<template>
    <ul>
        <li @click="setCrypto('BTC')" :className="cryptoNow == 'BTC' ? 'active' : ''">Bitcoin</li>
        <li @click="setCrypto('ETH')" :className="cryptoNow == 'ETH' ? 'active' : ''">Ethirium</li>
        <li @click="setCrypto('USDT')" :className="cryptoNow == 'USDT' ? 'active' : ''">USDT</li>
    </ul>
</template>
  
<script>
export default {
    props: {
        setCrypto: {
            type: Function,
            required: true
        },
        cryptoNow: {
            type: String,
            required: true
        }
    }
}
</script>
  
  
<style scoped>
  ul {
    list-style: none;
    width: 200px;
    padding: 0;
    border-radius: 3px;
    border: 3px solid darkgoldenrod;
}

li {
    display: block;
    background: rgb(229, 175, 39);
    color: white;
    padding: 20px 0;
}

li:hover, li.active {
    background: darkorange;
    cursor: pointer;
}
</style>
  