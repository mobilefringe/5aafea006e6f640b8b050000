<template>
    <div v-if="dataLoaded" id="overlay">
        <div class="loading-container">
            <vue-simple-spinner size="huge" :message="property.name + 'is loading...'"></vue-simple-spinner>
        </div>
    </div>
</template>

<script>
var _extends=Object.assign||function(e){for(var t=1;t<arguments.length;t++){var n=arguments[t];for(var r in n)Object.prototype.hasOwnProperty.call(n,r)&&(e[r]=n[r])}return e};define(["Vue","vuex","vue-simple-spinner"],function(e,t,n){return e.component("vue-simple-spinner",n),e.component("loader",{template:template,data:function(){return{dataLoaded:!1}},created:function(){this.dataLoaded=!0},computed:_extends({},t.mapGetters(["property"]))})});
</script>

<style>
    #overlay {
        position: fixed;
        /* Sit on top of the page content */
        width: 100%;
        /* Full width (cover the whole page) */
        height: 100%;
        /* Full height (cover the whole page) */
        overflow: hidden;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        background-color: #ffffff;
        z-index: 999;
        display: -webkit-box;
        display: -webkit-flex;
        display: -moz-box;
        display: -moz-flex;
        display: -ms-flexbox;
        display: flex;
    }
    .loading-container .vue-simple-spinner-text{
        line-height: 1;
    }
</style>