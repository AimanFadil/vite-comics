<script>
export default {
    name: 'Header',
    data() {
        return {
            lista: [
                {
                    sezione: 'CHARACTERS',
                    attivo: true
                },
                {
                    sezione: 'COMICS',
                    attivo: true
                },
                {
                    sezione: 'MOVIES',
                    attivo: true
                },
                {
                    sezione: 'TV',
                    attivo: true
                },
                {
                    sezione: 'GAMES',
                    attivo: true
                },
                {
                    sezione: 'COLLECTIBLES',
                    attivo: true
                },
                {
                    sezione: 'VIDEOS',
                    attivo: true
                },
                {
                    sezione: 'FANS',
                    attivo: true
                },
                {
                    sezione: 'NEWS',
                    attivo: true
                },
                {
                    sezione: 'SHOP',
                    attivo: true
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
                        <li v-for="list, index in lista" :key="index" :class="list.attivo ? 'active' : ''">{{ list.sezione }}</li>
                    </ul>
                </div>
            </div>
        </div>
    </header>
  </div>
</template>

<style lang="scss" scoped>
header {
    height: 65px;
    margin: 30px;

    img {
        width: 25%;
    }

    .direction {
        display: flex;
        flex-direction: row;
        list-style: none;

    }

    li {
        padding: 10px 15px 15px 15px;
        line-height: 65px;

        &.active:hover {
            color: rgba(2, 130, 249, 255);

            border-bottom: 5px solid rgba(2, 130, 249, 255);

        }
    }
}
</style>