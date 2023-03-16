<script>
export default {
    name:"name",
    props:'allUsers',
}
</script>

<template >
    <div class="main">
        <div class="card">
            <div class="card__header">
                <img src={{ avatar }} alt="">
                <h2>{{ firstName }}  {{ lastName }}</h2>
                <h3> {{ email }}</h3>
            </div>
            <div class="card__exp">
                <h2><img src="../../assets/Untitled (22)/roles.png" alt="">{{ role }}</h2>
                <h2><img src="../../assets/Untitled (22)/age.png" alt="">{{ age }}</h2>
                <h2><img src="../../assets/Untitled (22)/skills.png" alt="">{{ skills }}</h2>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    .main{
        width: max-content;
        height: 100vh;
        padding: 25px;
        gap: 16px;
        display: flex;
        flex-wrap: wrap;
        align-items: center;
    }
    .card{
        width: 227px;
        height: 200px;
    }
</style>