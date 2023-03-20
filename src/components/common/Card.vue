<script>
export default {
    name:"Card",
    props:['allUsers','msg'],
}
</script>

<template >
    
 <div class="card" v-for="(user, index) in allUsers" :key="index">
        <div class="card__header">
            <div>
                <img :src="user.avatar" alt="">
            </div>
            <div>
                <h2>{{ user.firstname }}  {{ user.lastname }} </h2>
                <h3> {{ user.email }}</h3>
            </div>
            
        </div>
        <div class="card__exp">
            <h2><img src="../../assets/Untitled (22)/Frame-1.png" alt="">{{ user.role }}</h2>
            <h2><img src="../../assets/Untitled (22)/Frame-2.png" alt="">{{ user.age }}</h2>
            <h2><img src="../../assets/Untitled (22)/Frame.png" alt="">{{ user.skills }}</h2>
        </div>
</div>

</template>

<style lang="scss" scoped>
h2 {
    font-size: 14px;
    line-height: 16px;
    color: #000000;
}

h3{
    font-size: 12px;
    color: #9A9A9A;
    line-height: 14px;
}
.card{
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    width: 227px;
    height: 200px;
    border: 2px solid red;
    cursor: pointer;

}

.card__header {
    display: flex;
    align-items: center;
    gap: 21px;

    img{
        width: 45px;
        height: 45px;
    }
    }
.card__exp {

    h2 {
        display: flex;
        flex-direction: row;
        align-items: center;
        font-size: 14px;
        line-height: 16px;
        color: #000000;
    }
    }
</style>