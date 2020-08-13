<template>
        <div class="row">
            <div class="col-lg-7 col-md-12 col-sm-12 col-12 none contact-container">
                <span class="contact-text">
                    <h1>
                        LA COMIDA ES 
                    <span class="background-yellow">
                        NUESTRO ARTE
                    </span>
                    </h1>
                    </span>
                <img alt="contact" src="../../assets/contact.svg"  height="100%" width="100%">
            </div>
            <div class="col-lg-5 col-md-12 col-sm-12 col-12 none background">
                    <span class="text">
                        <h1>¿Quién es Foodies?</h1>
                        <p>
                            Elit irure ad nulla id elit laborum nostrud mollit irure.
                            Velit reprehenderit sunt nulla enim aliquip duis tempor est culpa fugiat consequat culpa consectetur Lorem.
                            Reprehenderit dolore culpa irure eiusmod minim occaecat et id minim ullamco.
                        </p>
                        <a href="#">Contáctanos <i class="fa fa-arrow-right flechaIcon"/></a>
                        </span>
            </div>
        </div>
</template>

<script>
export default {
    data() {
        return {
        name: 'LandingContact',
        };
    },
}
</script>

<style lang="less" scoped>
    // colors
    @black: #000000;

    .none, .row {
        padding: 0px;
        margin: 0px;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .contact-container {
        display: block;
    } 
    img {
        vertical-align: middle;
    }
    .background{
        position: relative;
        display: inline-block;
        background: url('../../assets/contactDecorator.svg');
        min-height: 351px;
        background-position: right -120px top;
    }
    .contact-text {
        position: absolute;
        bottom: 60px;
        right: 40px;
        color: white;
        text-align: end;
        width: 535px;
        h1 {
            font-family: 'Druk Text Wide';
            font-size: 50px;
            line-height: 50px;
        }
        .background-yellow {
            color: #ffd600;
        }
        @media (max-width: 600px){
            bottom: 30px;
            right: 20px;
            width: 100%;
        }
        @media (max-width: 450px){
            bottom: 15px;
            right: 10px;
            h1 {
                font-size: 30px;
            }
        }
    }
    .text {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        width: 450px;
        h1, a {
            font-family: 'Syne';
            font-size: 22px;
            line-height: 26px;
            color: @black;
        }
        h1 {
            margin-bottom: 27px;
        }
        p {
            font-family: 'Open Sans';
            font-size: 18px;
            line-height: 25px;
            color: rgba(0, 0, 0, 0.4);
            margin-bottom: 54px;
        }
        @media (min-width: 1367px){
            width: 570px;
        }
        @media (max-width: 1100px){
            width: 570px;
        }
        @media (max-width: 992px){
            width: 570px;
        }
        @media (max-width: 600px){
            width: 100%;
            padding: 0 0px;
        }
    }
</style>