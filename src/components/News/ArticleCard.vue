<template>
    <div>
        <div class="article">
            <div class="type ">
                <b-badge variant="default text-white p-2">{{type}}</b-badge>
                <span class="data">
                    {{data}}
                </span>
            </div>
            <div class="title">{{title}}</div>
            <div class="content" v-for="text in content[0].text" :key="text.id">{{text}}</div>
        </div>
    </div>
</template>
<script>
export default {
    name: "ArticleCard",
    props: ['title', 'type', 'data', 'content']
}
</script>
<style>
.article .type{
    display: flex;
    flex-flow: row nowrap;
    justify-content: space-between;
    font-size: 15px;
    font-weight: 600;
}
.article .data{
    color: rgba(255, 255, 255, 0.5);
    font-size: 15px;
    font-weight: 800;
}
.article .title{
    color: white;
    font-size: 25px;
    font-weight: 800;
}
</style>
