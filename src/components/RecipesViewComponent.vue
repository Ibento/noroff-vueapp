<template>
    <div class="[ row ]">
        <div v-for="(recipe, index) in recipes" v-bind:key="index" class="[ col-sm-12 ]">
            <recipes-component
                v-bind:title="recipe.title" 
                v-bind:href="recipe.href" 
                v-bind:ingredients="recipe.ingredients" 
                v-bind:thumbnail="recipe.thumbnail" 
            >
            </recipes-component>        
        </div>
    </div>
</template>
<script>
    import RecipesComponent from './RecipesComponent.vue'
    
    export default {
        name: 'RecipesViewComponent',
        components: {
            RecipesComponent
        },
        data() {
            return {
                recipes: []
            }
        },
        created: function() {
            const app = this;
            
            const conversionURL = 'https://cors-anywhere.herokuapp.com/';
            const url = 'http://www.recipepuppy.com/api';
        
            fetch(conversionURL + url)
             .then(response => response.json())
             .then(data => (app.recipes = data.results));
            
        }
    }
</script>
