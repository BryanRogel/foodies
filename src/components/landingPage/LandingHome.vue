<template>
    <main>
        <div class="container">
            <div class="row">
                <div class="col-lg-6 col-md-8 col-sm-12 col-12">
                    <div class="background"><h1>Un nuevo sabor esta en la ciudad</h1></div>
                    <p class="description">Estamos a punto de descubrir un mundo lleno de sabores y de emociones inigualables.</p>
                    <a href="#">Encuéntranos <i class="fa fa-arrow-right flechaIcon"/></a>
                </div>
            </div>
        </div>
    </main>
</template>

<script>
export default {
    data() {
        return {
        name: 'LandingHome',
        };
    },
}
</script>

<style lang="less" scoped>
    // variables
    @top: 84px;
    @tabSize: 992px;

    // colors
    @black: #000000;

    @font-face {
        font-family: "Druk Text Wide";
        src: url("/fonts/druk.text.wide.regular.ttf");
    }
    @font-face {
        font-family: "Open Sans";
        src: url("/fonts/openSans.regular.ttf");
    }
    main {
        min-height: 873px;
        background: url('../../assets/mask_hero.svg');
        background-repeat: no-repeat;
        background-position: right top;
        background-size: 47.9%;
        margin-top: -@top;
    }
    .col-lg-6 {
        margin-top: calc(267px + @top);
        padding: 0px;
    }
    .background {
        background: url('../../assets/bg_text.svg');
        background-repeat: no-repeat;
        background-position: bottom left;
        background-size: 70.9%;
    }
    h1 {
        font-family: 'Druk Text Wide';
        font-size: 60px;
        line-height: 60px;
        color: @black;
        margin-left: 20px;
        padding-bottom: 8px;
        margin-top: -@top;
    }
    .description {
        font-family: 'Open Sans';
        font-size: 18px;
        line-height: 25px;
        color: rgba(0, 0, 0, 0.4);
        padding: 0 40px;
        margin-top: 20px;
        margin-bottom: 46px;
        @media (max-width: @tabSize) {
            font-size: 16px;
            line-height: 22px;
            padding: 0 210px 0 0;
        }
    }
    a {
        font-family: 'Syne';
        font-size: 22px;
        line-height: 26px;
        color: @black;
    }
</style>