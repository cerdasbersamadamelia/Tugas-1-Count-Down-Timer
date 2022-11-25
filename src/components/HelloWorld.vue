<template>
  <p>Halo Damelia [041643527], detik berjalan mundur dari:  {{ countDown }} </p>
</template>

<script>
   export default {
       data () {
           return {
               countDown: 30
           }
       },
       methods: {
           countDownTimer () {
               if (this.countDown > 0) {
                   setTimeout(() => {
                       this.countDown -= 1
                       this.countDownTimer()
                   }, 1000)
               }
           }
       },
       created () {
           this.countDownTimer()
       }
   }
</script>