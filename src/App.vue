<template>
  <div id="app">
    <h3>{{title}}</h3>
    <h4>
    <router-link class="link" to="/data/planets">Explore the Planets</router-link> |
    <router-link class="link" to="/data/people">Meet the Characters</router-link>
    </h4>
    <router-view></router-view>
    <div class="col-md-12 d-flex flex-wrap">
        <Character 
            v-for="(id, ind3) in inital_ids"
            :id="id"
            key="index"
        />
    </div>
 
  </div>
</template>
<script>
    import Character from './components/Character.vue'
    import Data from './components/Data.vue'
    export default {
        name: 'app',
        data() {
            return {
                title: 'Generate Your Team',
                inital_ids: [1, 13, 14, 16]
            }
        },
        components: {
          Character,
          Data  
        }
            
    }
</script>
