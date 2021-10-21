<template>
    <footer>
        <div class="ui inverted  vertical footer segment">
            <div class="ui container">
            <div class="ui  inverted divided center aligned  stackable grid">
                <div class="three wide column">
                <h4 class="ui inverted header">Contáctenos</h4>
                <div class="ui inverted link list">
                    <span class="ui item cart">
                        <a href="#" class="item" ><i class="phone icon space"></i>2345645</a>
                    </span>
                    <span class="ui item cart">
                        <a href="https://accounts.google.com/signin/v2/identifier?passive=1209600&continue=https%3A%2F%2Faccounts.google.com%2FEditPasswd%3Fhl%3Des&followup=https%3A%2F%2Faccounts.google.com%2FEditPasswd%3Fhl%3Des&hl=es&flowName=GlifWebSignIn&flowEntry=ServiceLogin"
                        class="item" ><i class="envelope outline icon space"></i>ecotripulantes@gmail.com</a>
                    </span>
                </div>
                </div>
                <div class="six wide center aligned column">
                    <img class="ui  logo" src="../assets/img/logo.png" alt="">
                    <h4 class="ui  name inverted ">EcoTripulantes</h4>
                    <p>El objetivo de la plataforma es ser un aliado de todas aquellas personas  en las cuales 
                        exista un interés de trabajar en la preservación del medio ambiente o del reciclaje.</p>
                </div>
                <div class="three wide column">
                <h4 class="ui inverted header">Redes Sociales</h4>
                <div class="ui inverted link list">
                    <span class="ui item cart">
                        <a href="#" class="item" ><i class="facebook icon"></i></a>
                        <a href="#" class="item" ><i class="instagram icon"></i></a>
                        <a href="#" class="item" ><i class="twitter icon"></i></a>
                    </span>
                    
                </div>
                </div>
        
            </div>
        </div>
    <div class="ui footer ">
        <div class="copyright">
            <p>© 2021 Todos los  derechos reservados | EcoTripulantes</p>
        </div>
            
    </div>
    </div>
    </footer>
</template>

<script>
export default {
    name: 'Footer',

}
</script>

<style>

footer {
    position: absolute;
    width: 100%;
}

.copyright p{
    text-align: center;
    font-size: 15px;
    margin-bottom: 15px;
}


.copyright{
    width: 100%;
    height: 50px;
    text-align: center;
    display: grid;
    align-items: center;
    
    
}
.footer{
    color: white !important;
    margin-top: 25px;
    border-top: 1px solid rgb(255 255 255 / 100%) !important;

   
}
.ui.name {
    margin-top: 7px;
}
.ui.logo{
    width: 114px;
}

</style>