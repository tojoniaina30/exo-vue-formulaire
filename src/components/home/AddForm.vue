<script>
export default {
    name:"AddForm",
}
</script>

<template >
    <div class="form">
        <h1>User Info</h1>
        <input type="text" placeholder="First Name">
        <input type="text" placeholder="Last Name">
        <input type="text" placeholder="Email">
        <input type="text" placeholder="Age">
        <input type="text" placeholder="Role">
        <div class="form__skills">
            <input type="text" placeholder="Skills">lol
            <button >+</button>
            
        </div>
        <div class="form__exp">
            <input type="text" placeholder="Experience Title">
            <input type="text" placeholder="Experience description">
            <input type="text" placeholder="Experience date">
            <button >+</button>
        </div>
        <button>Add user info</button>
    </div>
</template>

<style lang="scss" scoped>
input {
    height: 45px;
    width: 286px;
    border: 2px solid black;
    color: black;
}
button{
    background: #2444B5;
    color: aliceblue;
    text-align: center;
    border-radius: inherit;
}
.form {
    width: 348px;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    border-right: 2px solid grey;
    
    &__skills {
        width: auto;
        height: auto;
        display: flex;
        position: relative;

        button{
            position:absolute;
            right: 0;
            top: 0;
            bottom: 0;
            
        }
    }
    &__exp {
        display: flex;
        flex-direction: column;
        gap: 16px;
        padding: 5px;

    }
}



</style>