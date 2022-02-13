<template>
    <main>
        <div class="container">
            <ul>
                <li v-for="(disc, index) in discs" :key='index'>{{ disc.title }}</li>
            </ul>
        </div>
    </main>
   
</template>

<script>
export default {
    name: 'Main',
    data() {
      return {
        discs: []
      }
    },
    created() {
        this.getDiscs();
    },
    methods: {
        async getDiscs(){
            const res = await fetch('https://flynn.boolean.careers/exercises/api/array/music');
            const {response} = await res.json();
            this.discs=response;
        }
    },  
}

</script>

<style scoped lang='scss'>
    main{
        background-color: lightblue;
        height: 100vh;
        .container{
            width: 1200px;
            margin: auto;
            li{
                padding: 30px;
                background-color: grey;
                display: flex;
                flex-direction: column;
                align-items: center;
            }
        }

    }
</style>