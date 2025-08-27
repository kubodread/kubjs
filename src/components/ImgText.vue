<template>

<div class="figt">
                <img :src="texto.imagen" :alt="texto.titulo">
                <div class="textf" >
                {{ texto.informacion }}
                </div>
</div>


</template>


<script>
export default {
    name: 'ImgText',
        props: {
         texto: {
            type: Object,
            required: true
        },
    },
};
</script>

<style scoped>
    .figt {
        display: flex;
        width: 280px;
        height: auto;
        justify-content: space-between;
        flex-direction: column;
        align-items: center;
        background-color: lightgray;
        border-radius: 15px;
        padding: 5px;
    }
    img.figtkubimg {
        filter: sepia(60%);

    }

    img.figtkubimg:hover {
        filter: saturate(180%);
    }

    div.figt img {
        filter: sepia(40%);

    }

    div.figt img:hover {
        filter: saturate(180%);

}
    .textf {
        text-align: justify;
        font-size: 15px;
        padding: 0 10px;
    }

        .figt img {
        width: 70%;
        border-radius: .61em;
        mask-image: linear-gradient( #1f2937 40%, transparent );
        justify-content: center;
        border-radius: 15px;

    }
</style>
