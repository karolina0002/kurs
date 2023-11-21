<template>
<p>start</p>
</template>
<script>
export default {
 data() {
   return {
     number: ''
   }
 },
 methods: {
   async call() {
     await fetch(`${process.env.VUE_APP_SERVER_URL}/call`, {
       method:  "POST",
       headers: {
         "Content-type" : "application/json; charset=UTF-8"
       },
       body: JSON.stringify({number:  this.number})
     });
   },
 },
}
</script>