<template>
    <div class="card">
        <div class="">
            <div class="header">
                <i class="user icon"/>
                user name
            </div>
            <div class="meta">
                <i class="recycle icon"></i>
                user role
            </div>
            <div class="container">
                <div class="ui one column grid">
                        <div class="conte  ui segment" style="margin-left: 30px;margin-top: -30px">
                            <div class="ui column" v-for="image in publication.prodImage" :key="image._id">
                                <img class="medium ui image" type="image" :src="API_URL + image.url" :alt="publication.materialType">
                            </div>
                        </div>
                </div>
                <div class="ui grid center">
                    <div class="fourteen wide column name">
                        <h4 style="padding: initial" >Descripción</h4>
                        <p style="padding: initial" >{{ publication.description }}</p>
                        </div>
                        <table class=" ui celled table fourteen wide column " style="background: #9c4fe3;color: white; margin-left: 30px; margin-bottom: 36px">
                        <tbody>
                            <tr>
                                <td><strong>Tipo de material</strong></td>
                                <td>{{ publication.materialType }}</td>
                            </tr>
                            <tr>
                                <td><strong>Cantidad</strong></td>
                                <td>{{ publication.quantity }}</td>
                            </tr>
                            <tr>
                                <td><strong>Periodicidad</strong></td>
                                <td>{{ publication.frecuency }}</td>
                            </tr>
                            <tr>
                                <td><strong>Dirección</strong></td>
                                <td>{{ publication.address }}</td>
                            </tr>
                            <tr>
                                <td><strong>Departamento</strong></td>
                                <td>{{ publication.deptLoc }}</td>
                            </tr>
                            <tr>
                                <td><strong>Ciudad</strong></td>
                                <td>{{ publication.cityLoc }}</td>
                            </tr>
                        </tbody>
                    </table>
                    
                </div>

                
            </div>
            <div class="content">
                <span class="left floated">
                    <i class="heart outline like icon"></i>
                    <i class="add icon"></i>
                    <router-link to="/post"><i class="trash icon ui eli" @click="deletePublication(publication._id)"></i></router-link>
                </span>
                <div type="right floated col">
                    
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { API_URL } from '../utils/constants';
// import { getPublicationsApi } from '../api/publish';
import { deletePublicationApi } from '../api/publish';
export default {
    name: 'Publications',
    props: {
        publication: Object,
    },
    setup(props) {
        const deletePublication = async (id) => {
            try {
                const response = await deletePublicationApi(id);
                console.log("La publicación se ha eliminado", response);
            } catch (error) {
                console.log("Ocurrió un error en el proceso...", error.statusCode)
            };
            return id;
            
        };
        
        return {
            API_URL,
            deletePublication,
        }
    }
}
</script>

<style lang="scss" scoped>
.card {
    margin: 20px;
    padding: 20px;
    border: 2px solid rgb(82, 68, 82);
    border-radius: 10px;
    box-shadow:  0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
    .container {
        
        flex-direction: row;
        align-items: center;
        .col-1 {
            width: 30%;
        }
        .col-2 {
            width: 70%;
        }
    }
}
p, h4 {
    margin: 10px;
    padding: 10px;
}
.conte {
    display: flex;
    margin-top: -80px;
}
.name {
    padding: initial;
    margin-left: 20px;
    margin-top: 5px;
}
.pad {
    padding: initial
}

.icon {
    color: #2939e3;
    &:hover {
        cursor: pointer;
        color: red;
    }
}

</style>