<template lang="html">
    <div id="wrapper">
        <div id="sun">

        </div>

        <div id="mercury-orbit" v-on:click="handleMercuryClick">
            <div id="mercury">

            </div>
        </div>

        <div id="venus-orbit" v-on:click="handleVenusClick">
            <div id="venus">

            </div>
        </div>
        <div id="earth-orbit" v-on:click="handleEarthClick">
            <div id="earth">

            </div>
        </div>
        <div id="mars-orbit" v-on:click="handleMarsClick">
            <div id="mars">

            </div>
        </div>
    </div>

</template>

<script>
export default {
    name: "CanvasComponent",
    methods: {
        handleMercuryClick(){
            console.log("You clicked on Mercury!");
        },
        handleVenusClick(){
            console.log("Venus was clicked");
        },
        handleEarthClick(){
            console.log("Earth was clicked!");
        },
        handleMarsClick(){
            console.log("Mars was clicked!");
        }
    }
}
</script>

<style lang="css" scoped>


    #wrapper {
      align-items: center;
    }

    #sun {
      position: absolute;
      top: 45%;
      left: 45%;
      height: 120px;
      width: 120px;
      border-radius: 100%;
      background: radial-gradient(circle at 30px 100px, #ffd000, #ff6702);
    }

    #mercury-orbit {
        position: absolute;
        top: 260px;
        left: 600px;
        width: 220px;
        height: 220px;
        border: 2px #4A437F dashed;
        border-radius: 100%;
        -webkit-animation: spin-right 10s linear infinite;
        animation: spin-right 10s linear infinite;
        z-index: 3;
    }
    #mercury {
      position: absolute;
      top: 90px;
      left: -13px;
      height: 25px;
      width: 25px;
      border-radius: 100%;
      background: radial-gradient(circle at 2px 25px, #ffe526, #e29b28);
    }

    #venus-orbit {
        position: absolute;
        top: 230px;
        left: 560px;
        width: 320px;
        height: 320px;
        border: 2px #4A437F dashed;
        border-radius: 100%;
        -webkit-animation: spin-right 5s linear infinite;
        animation: spin-right 13s linear infinite;
        z-index: 2;
    }

    #venus {
        position: absolute;
        top: 80px;
        left: -13px;
        height: 45px;
        width: 45px;
        border-radius: 100%;
        background: radial-gradient(circle at 25px 25px, #ffa11e, #f76516);
    }

    #earth-orbit {
        position: absolute;
        top: 150px;
        left: 490px;
        width: 500px;
        height: 500px;
        border: 2px #4A437F dashed;
        border-radius: 100%;
        -webkit-animation: spin-right 5s linear infinite;
        animation: spin-right 15s linear infinite;
        z-index: 1;
    }

    #earth {
        position: absolute;
        top: 150px;
        left: -13px;
        height: 50px;
        width: 50px;
        border-radius: 100%;
        background: radial-gradient(circle at 5px 10px, #00ad62, #69b1f4);
    }

    #mars-orbit {
        position: absolute;
        top: 100px;
        left: 400px;
        width: 700px;
        height: 700px;
        border: 2px #4A437F dashed;
        border-radius: 100%;
        -webkit-animation: spin-right 5s linear infinite;
        animation: spin-right 20s linear infinite;
        z-index: 0;
    }

    #mars {
        position: absolute;
        top: 170px;
        left: 19px;
        height: 38px;
        width: 38px;
        border-radius: 100%;
        background: radial-gradient(circle at 5px 10px, #dda600, #bf7900);
    }

    @-webkit-keyframes spin-right {
      100% {
        -webkit-transform: rotate(360deg);
        -moz-transform: rotate(360deg);
        -ms-transform: rotate(360deg);
        -o-transform: rotate(360deg);
        transform: rotate(360deg);
      }
    }
</style>
