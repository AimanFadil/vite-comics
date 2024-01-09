<script>
export default {
    name: 'Cards',
    props: {
        comic: Object,
    }
}
</script>
<template lang="">
    <div class="content">
        <div class="cards">
            <img :src="comic.thumb">
            <p class="textWhite" >{{comic.series}}</p>
            <div class="overlay">
                <p class="textWhite">{{ comic.type}}</p>
                <p class="textWhite">{{ comic.price}}</p>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.content {
    background-color: rgba(28, 28, 28, 255);
    padding: 15px 50px;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;

    .cards {
        width: calc(100% / 6);
        margin: 15px 0;
        position: relative;


        .textWhite {
            color: white;

        }

        img {
            width: 160px;
        }

        .overlay {
            position: absolute;
            bottom: 178px;
            left: 0;
            background-color: rgba(0, 0, 0, 0.582);
            transition: 1s;

            align-items: center;
            width: 160px;
            height: 28%;
            opacity: 0;

            &:hover {
                opacity: 1;
            }


        }

    }

}
</style>