<script>
export default {
    name: 'Header',
    data() {
        return {
            lista: [
                {
                    sezione: 'CHARACTERS',
                    attivo: false
                },
                {
                    sezione: 'COMICS',
                    attivo: true
                },
                {
                    sezione: 'MOVIES',
                    attivo: false
                },
                {
                    sezione: 'TV',
                    attivo: false
                },
                {
                    sezione: 'GAMES',
                    attivo: false
                },
                {
                    sezione: 'COLLECTIBLES',
                    attivo: false
                },
                {
                    sezione: 'VIDEOS',
                    attivo: false
                },
                {
                    sezione: 'FANS',
                    attivo: false
                },
                {
                    sezione: 'NEWS',
                    attivo: false
                },
                {
                    sezione: 'SHOP',
                    attivo: false
                },
            ]
        }
    }
}
</script>
<template lang="">
  <div>
    <header>
        <div class="container">
            <div class="row">
                <div class="col-3">
                    <img src="../assets/img/dc-logo.png" alt="Logo">
                </div>
                <div class="col-9">
                    <ul class="direction">
                        <li v-for="list, index in lista" :key="index" >{{ list.sezione }}</li>
                    </ul>
                </div>
            </div>
        </div>
    </header>
  </div>
</template>

<style lang="scss" scoped>
header {
    height: 100px;
    margin: 30px;

    .direction {
        display: flex;
        flex-direction: row;
        list-style: none;
    }

    li {
        padding: 15px;
    }
}
</style>