<template>
    <nav class="header">
        <div class="max-size">
            <img alt="Vue logo" src="../assets/foodiesLogo.svg"  height="100%" width="148px" />
            <input class="menu-btn" type="checkbox" id="menu-btn" v-model="checked"  />
            <label class="menu-icon" htmlFor="menu-btn" @click="checked = !checked"><span class="navicon"></span></label>
            <ul class="menu">
                <router-link to="/" >
                <li @click="checked = false" id="first">
                    Acerca de
                </li>
                </router-link>
                <router-link to="/restaurant" >
                <li @click="checked = false" id="second">
                    Restaurantes
                </li>
                </router-link>
                <router-link to="/menu" >
                <li @click="checked = false" id="third">
                    Menú
                </li>
                </router-link>
                <router-link to="/contact" >
                <li @click="checked = false" id="fourth">
                    Contáctanos
                </li>
                </router-link>
            </ul>
        </div>
    </nav>
</template>

<script>
export default {
    data() {
        return {
        name: 'Navbar',
        checked: false,
        };
    },
};
</script>

<style lang="less" scoped>
    // variables
    @tabSize: 992px;
    @leftLogo: 101px;
    @LeftLogoTab: 40px;
    @LeftLogoMovil: 16px;
    @heightLogo: 27px;
    @top: 57px;
    @topTab: 30px;
    @topMovil: 47px;
    @topRoutesMovil: 50px;
    @leftRoutes: 86px;
    @leftRoutesMovil: 17px;
    @leftRoutes: 39px;
    @fontA: 18px;
    @lineA: 22px;
    @borderRadius: 50px;

    // Colors
    @black: #000000;
    @white: #ffffff;

    @font-face {
        font-family: "syne";
        src: url("/fonts/syne.bold.ttf");
    }

    .header {
        background-color: transparent;
        width: 100%;
        z-index: 300;
    }

    img {
        margin-left: @leftLogo;
        @media (max-width: @tabSize) {
            margin-left: @LeftLogoTab;
        }
        @media (max-width: 600px) {
            margin-left: @LeftLogoMovil;
        }
    }

    .max-size {
        height: @heightLogo;
        margin-top: @top;
        display: flex;
        max-width: 1366px;
        @media (max-width: 600px) {
            margin-top: @topMovil;
        }
        @media (max-width: calc(@tabSize - 1px)) {
            display: block;
            margin-top: @topTab;
        }
    }

    .active {
        color: #979797 !important;
    }

    .header ul {
        margin: 0;
        padding: 0;
        list-style: none;
        overflow: hidden;
        background-color: @white;
        @media (max-width: @tabSize) {
            border-bottom-left-radius: @borderRadius;
            border-bottom-right-radius: @borderRadius;
        }
    }

    ul {
        margin: 10px 0px;
        position: relative;
        margin-left: @leftRoutes;
    }
    ul li {
        display: inline;
        list-style: none;
    }

    .header li a {
        display: block;
        padding: 20px;
        border-right: 1px solid #f4f4f4;
        text-decoration: none;
    }

    .header .logo {
        display: block;
        float: left;
        font-size: 2em;
        padding: 10px 20px;
        text-decoration: none;
    }

    a {
        margin-left: @leftRoutes;
    }

    li {
        font-family: "syne";
        font-size: @fontA;
        line-height: @lineA;
        color: @black;
        text-decoration: none;
    }

    /* menu */

    .header .menu {
        clear: both;
        max-height: 0;
        transition: max-height 0.2s ease-out;
        display: flex;
        align-items: center;
        @media (max-width: calc(@tabSize - 1px)) {
            display: grid;
        }
    }

    .header .menu-icon {
        cursor: pointer;
        float: right;
        top: 12px;
        padding-right: 40px;
        position: relative;
        user-select: none;
    }

    .header .menu-icon .navicon {
        background: #333;
        display: block;
        height: 2px;
        position: relative;
        transition: background 0.2s ease-out;
        width: 18px;
    }

    .header .menu-icon .navicon:before,
    .header .menu-icon .navicon:after {
        background: #333;
        content: "";
        display: block;
        height: 100%;
        position: absolute;
        transition: all 0.2s ease-out;
        width: 100%;
    }

    .header .menu-icon .navicon:before {
        top: 5px;
    }

    .header .menu-icon .navicon:after {
        top: -5px;
    }

    .header #menu-btn {
        display: none;
    }

    #menu-btn:checked ~ .menu {
        @media (max-width: calc(@tabSize - 1px)) {
            min-height: 240px;
        }
    }

    .header #menu-btn:checked ~ .menu-icon .navicon {
        background: transparent;
    }

    .header #menu-btn:checked ~ .menu-icon .navicon:before {
        transform: rotate(-45deg);
    }

    .header #menu-btn:checked ~ .menu-icon .navicon:after {
        transform: rotate(45deg);
    }

    .header #menu-btn:checked ~ .menu-icon:not(.steps) .navicon:before,
    .header #menu-btn:checked ~ .menu-icon:not(.steps) .navicon:after {
        top: 0;
    }

    li:after {
        position: absolute;
        content: "";
        top: 50%;
        height: 4px;
        border-bottom: 6px solid #ffd600;
        transform: scale(0);
        opacity: 50%;
        @media (max-width: @tabSize) {
            left: @leftRoutes;
        }
    }

    #first:after{
        width: 102px;
        @media (max-width: @tabSize) {
            top: 13%;
        }
    }
    #second:after{
        width: 133px;
        @media (max-width: @tabSize) {
            top: 38%;
        }
    }
    #third:after{
        width: 57px;
        @media (max-width: @tabSize) {
            top: 63%;
        }
    }
    #fourth:after{
        width: 130px;
        @media (max-width: @tabSize) {
            top: 88%;
        }
    }

    li:hover:after {
        transition: transform 0.3s cubic-bezier(0.11, 0.7, 0, 1);
        transform: scale(1);
        color: #333;
    }

    a:hover {
        text-decoration: none;
    }

    @media (min-width: @tabSize) {
    .header li {
        float: left;
        color: #000;
    }
    .header .menu {
        clear: none;
        max-height: none;
        margin-left: @leftRoutes;
    }
    .header .menu-icon {
        display: none;
    }
    ul li {
        display: flex;
    }
    }

    @media (max-width: 500px) {
    ul li {
        display: block;
        color: #000000;
    }
    a {
        text-decoration: none;
    }
    }
</style>