<script>
import { nanoid } from 'nanoid'

export default {
    name:"AddForm",
    data:function() {
        return {
            firstname:'',
            lastname:'',
            email:'',
            role:'',
            age:'',
            avatar:'',
            skills:'',
            title:'',
            desc:'',
            date:'',
            language:'',
            languages:[],
            user:{},
            users:[],

        }
    },
    methods: {
        handleAddUser(event) {
            event.preventDefault();
            this.$emit('addUser', {
                firstname: this.firstname,
                lastname: this.lastname,
                age:this.age,
                email:this.email,
                role:this.role,
                avatar:this.avatar,
                skills:this.skills,
                title:this.title,
                desc:this.desc,
                date:this.date,
                id:nanoid()
            })
        },
        showSkill: function (skill) {
            this.languages.push(skill)
        },
        deleteSkill: function () {
            if (this.language){
                this.language = false
            }
        }
    },
}
</script>

<template >
    <div class="form" >
        <h1>User Info</h1>
        <input type="text" placeholder="First Name" v-model="firstname">
        <input type="text" placeholder="Last Name" v-model="lastname">
        <input type="text" placeholder="Email" v-model="email">
        <input type="text" placeholder="Age" v-model="age">
        <input type="text" placeholder="Role" v-model="role">
        <input type="text" placeholder="Avatar" v-model="avatar">
        <div class="form__skills">
            <input type="text" placeholder="Skills" v-model="skills">
            <button v-on:click="showSkill(skills)">+</button>
            <div class="skills-added">
                <p v-for="language in languages"> {{ language }}
                    <img v-if="language" v-on:click="deleteSkill()" src="../../assets/trash.png" alt="">
                </p>
            </div>
            
        </div>
        <div class="form__exp">
            <input type="text" placeholder="Experience Title" v-model="title">
            <input type="text" placeholder="Experience description" v-model="desc">
            <input type="text" placeholder="Experience date" v-model="date">
            <button >+</button>
        </div>
        <button type="submit" v-on:click="handleAddUser">Add user info</button>
    </div>
</template>

<style lang="scss" scoped>
div {
    font-size: 14px;
    line-height: 16px;
    color: #000000;

}
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
    height: auto;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;
    border-right: 2px solid grey;
    gap: 16px;
    
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
            height: 50px;
            border: inherit;
        }
    }
    &__exp {
        display: flex;
        flex-direction: column;
        gap: 16px;
        padding: 5px;

    }
}
.skills-added{
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 274px;
    margin-top: 26px;
    
    p {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding-left: 9px;
        width: 234px;
        background: #DDE3EB;
    }

    img {
        padding-left: 12px;
        padding-right: 12px;
        width: 16px;
        height: 16px;
        display: flex;
        align-items: center;
        justify-content: center;
        cursor: pointer;
        background-color: #DDE3EB;
    }
}


</style>