<template>
    <img @mouseenter="endreHover" @mouseleave="endreReverse"
     :class="{shake: hover, shakeReverse: reverse}" src="../assets/logo.png">

    <p >{{hover}}</p>
    <p>{{hallo}}</p>
</template>




<script>
export default {
    name: 'AnimasjonZoom',
    data(){
        return {
            test: "test",
            hover: false,
            reverse: true

        };
    },

    props: {
        hallo: String
    },

    methods: {
        endreHover: function () {
            this.hover = !this.hover
        },

        endreReverse: function () {
            this.hover = !this.hover
            this.reverse = !this.reverse
        }
    }
}
</script>







<style scoped>
.shake {
  animation: shake 0.82s both;;
}

@keyframes shake {
    0% {
            transform: scale(1.0);
            -webkit-transform: scale(1.0);
        }
        100% {
            transform: scale(2.0);
            -webkit-transform: scale(2.0);
        }
    
}

.shakeReverse {
  animation: shake 0.82s reverse;
}

</style>



<!--<template>
    <Transition name="bounce">
    <img v-if="hover"  src="../assets/logo.png">

    </Transition>
    <p @click="endreHover">{{hover}}</p>
</template>

<script>
export default {
    data(){
        return {
            test: "test",
            hover: false

        };
    },

    name: 'AnimasjonZoom',
    props: {
    },

    methods: {
        testMetode: function () {
            alert("hallo");
        },

        endreHover: function () {
            this.hover = !this.hover;
        }
    }
}
</script>

<style scoped>

.bounce-enter-active {
  animation: bounce-in 0.5s;
}
.bounce-leave-active {
  animation: bounce-in 0.5s reverse;
}
@keyframes bounce-in {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.25);
  }
  100% {
    transform: scale(1);
  }
}
</style>-->