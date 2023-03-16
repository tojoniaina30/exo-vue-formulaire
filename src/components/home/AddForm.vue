<script>
export default {
    name:"AddForm",
    data() {
        return {
            firstname:'',
            lastname:'',
            email:'',
            role:'',
            age:'',
            skills:'',
            title:'',
            desc:'',
            date:'',
        }
    },
    methods: {
        handleAddUser() {
            this.$emit('addUser', {name: this.name, age:this.age, role:this.role})
        },
    },
}
</script>

<template >
    <div class="form" v-on:submit.prevent="handleAddUser">
        <h1>User Info</h1>
        <input type="text" placeholder="First Name" v-model="firstname">
        <input type="text" placeholder="Last Name" v-model="lastname">
        <input type="text" placeholder="Email" v-model="email">
        <input type="text" placeholder="Age" v-model="age">
        <input type="text" placeholder="Role" v-model="role">
        <div class="form__skills">
            <input type="text" placeholder="Skills" v-model="skills">
            <button >+</button>
            
        </div>
        <div class="form__exp">
            <input type="text" placeholder="Experience Title" v-model="title">
            <input type="text" placeholder="Experience description" v-model="desc">
            <input type="text" placeholder="Experience date" v-model="date">
            <button >+</button>
        </div>
        <button type="submit">Add user info</button>
    </div>
</template>

<style lang="scss" scoped>
input {
    height: 45px;
    width: 286px;
    border: 2px solid black;
    color: black;
    padding-left: 20px;
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
    justify-content: space-around;
    align-items: center;
    border-right: 2px solid grey;
    
    &__skills {
        width: auto;
        height: auto;
        display: flex;
        position: relative;
        flex-direction: column;
        align-items: center;
        justify-content: space-around;

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