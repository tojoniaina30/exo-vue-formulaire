<script>
import Card from '../common/Card.vue';

export default {
    name:"Drawer",
    components: { Card }
}
</script>

<template >
    <div class="draw">
        <button class="close">X</button>
        <Card/>
        <div class="exp">
            <img src="../../assets/Ellipse 2.png" alt="">
            <p>2020 - 2023</p>
            <p>SAHA Technology</p>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
        </div>
        <div class="exp">
            <img src="../../assets/Ellipse 2.png" alt="">
            <p>2020 - 2023</p>
            <p>SAHA Technology</p>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
        </div>
    </div>
</template>

<style lang="scss" scoped>

p{
    font-weight: 400;
    font-size: 14px;
    line-height: 16px;
}

.draw{
    display: flex;
    flex-direction: column;
    width:592px;
    height: 100vh;
    position: absolute;
    right: 0;
    top: 0;
    bottom: 0;
    left: auto;
    box-shadow: -2px 0px 20px 20px rgba(0, 0, 0, 0.16);
}
.close{
    position: absolute;
    top: 5px;
    left: auto;
    right: 10px;
    padding: 10px 20px;
}
.exp{
    margin: 5px 59px 0px;
    padding: 0px 12px;
    position: relative;
    height: fit-content;
    

    & ::after{
        content: "";
        width: 2px;
        position: absolute;
        left: -5px;
        top: 33px;
        bottom: 3px;
        background-color: #9A9A9A;
    }

    img{
        position: absolute;
        top: 17.5px;
        left: -8.75px;

    }
}
</style>