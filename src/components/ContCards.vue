<script>
export default {
    name: 'ContCards',
    data() {
        return {
            comics: [
                {
                    "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book",
                },
                {
                    "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book",
                },
                {
                    "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel",
                },
                {
                    "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    "price": "$4.99",
                    "series": "Batman:  White Knight Presents: Harley Quinn",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel",
                },
            ],

        }
    },
}
</script>
<template lang="">
    <div>
        <div class="topContent"><h3 class="blueBut posizione" >CURRENT SERIES</h3></div>
        <div class="content">
            <div class="cards " v-for="comic, index in comics" :key="index">
                <img :src="comic.thumb">
                <p class="textWhite" >{{comic.series}}</p>
                <div class="overlay">
                    <p class="textWhite">{{ comic.type}}</p>
                    <p class="textWhite">{{ comic.price}}</p>
                </div>
            </div>
            
            <p class="blueBut center " >Load More</p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.topContent {
    height: 400px;
    background-image: url('../assets/img/jumbotron.jpg');



    .posizione {
        position: absolute;
        bottom: 360px;
        left: 60px;
    }

}

.blueBut {
    background-color: rgba(2, 130, 249, 255);
    border: solid rgba(2, 130, 249, 255);
    color: white;
    width: fit-content;


}

.content {
    background-color: rgba(28, 28, 28, 255);
    padding: 120px;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;

    img {
        width: 50%;
    }

    .cards {
        width: calc(100% / 6);
        margin: 15px 0;
        position: relative;
    }


    .textWhite {
        color: white;

    }

    .overlay {
        position: absolute;
        bottom: 89px;
        left: 0;
        background-color: rgba(0, 0, 0, 0.582);
        transition: 1s;

        align-items: center;
        width: 50%;
        height: 28%;
        opacity: 0;

        &:hover {
            opacity: 1;
        }


    }


}
</style>