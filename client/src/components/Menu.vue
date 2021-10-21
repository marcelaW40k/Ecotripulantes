<template>  
    <header>
        <div class="menu visible">
            <div class="ui contenedor ">
                <div class="left menu">
                    <router-link class="item" to="/">
                        <img class="ui small image space" src="../assets/img/logo.png" alt="">

                    </router-link>
                    <router-link class="item" to="/post">
                    Anuncios
                </router-link>
                </div>
                <div class="right menu" >
                    <router-link class="item" to="/login" v-if="!token"><i class="user icon"></i>
                        Iniciar sesión
                    </router-link>
                    <template v-if="token">
                        <span class="ui item logout" @click="logout">
                            <i class="sign-out icon"></i>
                        </span>
                    </template>
                </div>
                
            </div>
        </div>
    

    </header>
</template>

<script>

import { getTokenApi, deleteTokenApi } from '../api/token';
export default {
    name: 'Menu',  
    setup() {

        const token = getTokenApi();

        const logout = () => {
            deleteTokenApi();
            location.replace('/');
        };

        return {
            token,
            logout,
        };
    },
    


};


</script>

<style lang="scss" scoped >
@import url('https://fonts.googleapis.com/css2?family=IM+Fell+English+SC&family=Open+Sans:wght@500;600&display=swap');
    
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Open Sans', sans-serif;
}
header {
    width: 100%;
    height: 70px;
    background-color: #41b12cb8;
    box-shadow:  0 1px 4px 0;
    position: relative;
    z-index: 100;
    
}

.contenedor{
    display: flex;
    justify-content: space-between;
    
  
    align-items: center;
}
.space {
    margin-top: 5px;
}


    .menu.left{
        display: flex;
        .ui.image {
            width: 70px;
        }
    }
    .menu {
        margin-left: 60px;
        margin-right: 60px;
        align-items: center;
    }
    .item{
        color: white !important;
        font-size: 16px;
        margin-left: 30px;
    }
</style>