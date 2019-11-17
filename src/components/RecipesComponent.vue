<template>
    <div class="[ row ]">
        <div class="[ col-sm-4 ]">

        </div>
        <div class="[ col-sm-4 ]">
            <div class="[ recipe ]">
                <div>
                    <img v-bind:src="thumbnail" v-bind:alt="title">
                </div>  
                <div class="[ recipe--information ]"><br />
                    <h2><a v-bind:href="href">{{ title }} </a></h2>
                    <span>Ingredients: </span> {{ ingredients }}
                </div>
            </div>

        </div>
        <div class="[ col-sm-4 ]">

        </div>
    </div>
</template>

<script>
    export default {
        name: 'RecipesComponent',
        props: ['title', 'href','ingredients','thumbnail']
    }
</script>

<style scoped>
    .recipe {
        border: solid 1px black;
        border-radius: 4px;
        padding: 0px 20px 30px;
        margin-top: 30px;
    }

    .recipe img {
        padding-top: 20px;
    }

    .recipe span {
        font-weight: bold;
    }
</style>



