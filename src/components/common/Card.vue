<script>
export default {
    name:"Card",
    props:['allUsers','msg'],
}
</script>

<template >
    <div class="card" v-for="(user, index) in allUsers" :key="index">
        <div class="card__header">
            <img src={{ user.avatar }} alt="">
            <h2>{{ user.firstName }}  {{ user.lastName }}</h2>
            <h3> {{ user.email }}</h3>
        </div><!--  -->
        <div class="card__exp">
            <h2><img src="../../assets/Untitled (22)/roles.png" alt="">{{ user.role }}</h2>
            <h2><img src="../../assets/Untitled (22)/age.png" alt="">{{ user.age }}</h2>
            <h2><img src="../../assets/Untitled (22)/skills.png" alt="">{{ user.skills }}</h2>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    
.card{
    display: flex;
    align-items: center;
    justify-content: space-around;
    width: 227px;
    height: 200px;
    border: 2px solid red;
    &__header {
        
    }
}
</style>