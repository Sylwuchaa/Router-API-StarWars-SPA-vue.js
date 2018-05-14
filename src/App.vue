<template>
  <div id="app">
    <h3>{{title}}</h3>
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
    
    export default {
        name: 'app',
        data() {
            return {
                title: 'Generate Your Team',
                inital_ids: [1, 13, 14, 16]
            }
        },
        components: {
          Character  
        }
            
    }
</script>
