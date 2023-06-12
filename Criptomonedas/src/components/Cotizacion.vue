<script setup>
defineProps({
    cotizacion:{
        type: Object,
        required: true
    }
})
</script>

<template>
    <div class="contenedor-resultado">
        <h2>Cotizacion</h2>
            <div class="resultado">
          <img 
          :src="'https://cryptocompare.com/' + cotizacion.IMAGEURL" alt="imagen cripto">
          <div>
            <p>El precio actual es de: <span>{{ cotizacion.PRICE }}</span></p>
            <p>El precio mas alto de hoy fue de: <span>{{ cotizacion.HIGH24HOUR }}</span></p>
            <p>El precio mas bajo de hoy fue de: <span>{{ cotizacion.LOW24HOUR }}</span></p>
            <p>La variacion del precio respecto al dia anterior: <span>{{ cotizacion.CHANGEPCT24HOUR }}%</span></p>
            
          </div>
          </div>
        </div>
</template>
