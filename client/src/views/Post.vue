<template>
    <BasicLayouts>
        <section class="profile" >
            <div class="description grid-container profile-container" >
                <div  class="imgen">
                    <img  src="../assets/img/logo.png"  alt="" style="width: 250px;margin: 20px;">
                </div>
                <div style="margin-right: 166px;">
                    <h2>Hola, mi nombre es Marcela!</h2>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Id dolore velit commodi suscipit rerum sunt maxime aliquam laborum odit, temporibus reprehenderit? Esse numquam commodi saepe quis accusamus.</p>
                </div>
            </div>
        </section>
        <div class="container-fluid ui item">
            <div class="left container ui">
                <button  class="huge ui button" id="publish" @click="showPublish()">Publicar anuncios</button>
                <button  class="huge ui button" id="publications" @click="showPublication()">Ver anuncios</button>
            </div>
            <div class="divider ui"></div>
            <div class="cont container ui">
                <Publish v-if="showPublishForm"/>
                <div v-for="publication in publications" :key="publication._id">
                    <Publications v-if="showPublicationForm" :publication="publication"/>
                </div>
            </div>
        </div>
    </BasicLayouts>
</template>

<script>
import { computed, onMounted, ref } from 'vue'
import { useStore } from 'vuex'
import BasicLayouts from '../layouts/BasicLayouts.vue'
import Publish from '../components/Publish.vue'
import Publications from '../components/Publications.vue'
import { getPublications } from '../api/publish'
import { getTokenApi } from '../api/token';

export default {
    name: 'Post',
    components: {
        BasicLayouts,
        Publish,
        Publications,
    },
    props: {
        showPublish: Function,
        showPublication: Function,
    },
    setup() {
        let publications = ref(null);
        const store = useStore();
        const token = getTokenApi();


        const showPublishForm = computed(
            () => store.state.showPublishForm
        );
        const showPublicationForm = computed(
            () => store.state.showPublicationForm
        );
        const showPublish = () => {
            store.commit('setShowPublishForm', true)
            store.commit('setShowPublicationForm', false)
            //console.log('Mostrar Publicaciones', showPublicationForm)
        };
        const showPublication = () => {
            store.commit('setShowPublishForm', false)
            store.commit('setShowPublicationForm', true)
            //console.log('Publicar anuncio', showPublicationForm)
        };
        onMounted(async () => {
            const response = await getPublications(20);
            publications.value = response;
            if ( !token ) {
                document.getElementById("publish").disabled=true;
                document.getElementById("publications").disabled=true;
            }else{
                document.getElementById("publish").disabled=false;
                document.getElementById("publications").disabled=false;
            }

            
        })
        return {
            showPublish,
            showPublication,
            showPublishForm,
            showPublicationForm,
            publications,
        };
    },

}

</script>

<style lang="scss" scoped>
.ui.item {
    display: flex;
    flex-flow: column;
    .left {
        display: flex;
        flex-flow: row;
        justify-content: center;
        margin: 10px;
        .button {
            width: 40%;
            margin: 10px;
        }
    }
    .right {
        display: flex;
        flex-flow: row;
        justify-content: center;
    }
    .imgen{
        width: 320px;
    }
    .cont {
        width: 890px;
    }
    
}
.profile{
    padding: 14px 40px;background-color: #e6e9ed;margin-bottom: 50px;
}
.description {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-left: 141px;
}
</style>