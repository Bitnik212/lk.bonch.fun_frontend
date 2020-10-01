<template>
    <div class="label mb-4" v-bind:style="{background: 'url('+img+')'}" :class="{'bg-gradient-success': !isBackground(img)}">
        <div class="bg py-4 px-4">
            <div class="type mb-2 ">
                <span>
                    {{type}}
                </span>
                <span class="data">
                    {{data}}
                </span>
            </div>
            <div class="title mb-2">{{title}}</div>
            <div class="text">{{content[0].text[0]}}</div>
            <router-link to='/news/1'>
                <base-button class="mt-3" type="secondary">Читать далее</base-button>
            </router-link>
        </div>
    </div> 
</template>

<script>
export default {
    name: "NewsCard",
    props: ['title', 'img', 'content', 'type', 'data'],
    data () {
        return {
            bg: 'url("'+this.img+'");'
        }
    },
    methods: {
        isBackground(img) {
            if (img === 'none') {
                return false
            } else if (img) {
                return true
            }
        }
    }
}

</script>

<style>
.label{
    border-radius: 0.5em;
    background-repeat: no-repeat !important;
    background-size: cover !important;
    background-position: center !important;
    /* background-image: url('https://files.bitapp.me/illust_73591991_20200716_232154.png') !important; */
}
.label> .bg{
    border-radius: 0.5em;
    background: rgba(0, 0, 0, 0.5);
    backdrop-filter: blur(7px);
}
.label .data{
    color: rgba(255, 255, 255, 0.5);
    font-size: 15px;
    font-weight: 800;
}
.label  .title{
    color: white;
    font-size: 25px;
    font-weight: 800;
}
.label  .type{
    color: rgba(255, 255, 255, 0.5);
    font-size: 15px;
    font-weight: 600;
    display: flex;
    justify-content: space-between;
}
.label  .text{
    color: rgba(255, 255, 255, 0.7);
    font-size: 18px;
    font-weight: 400;
    max-height: 87px;
    overflow-y: hidden;
}
</style>