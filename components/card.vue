<template>    
  <article class="card">
    <div class="cover" v-if="cover" :style="{backgroundImage: 'url(' + cover + ')'}"></div>
    <div class="card-body">
        <div class="card-title-row">
            <div class="thumbnail" v-if="thumbnail" :style="{backgroundImage: 'url(' + thumbnail + ')'}"></div>
            <div class="title-text" v-if="title || subTitle">
                <h1 v-if="title">{{ title }}</h1>
                <p v-if="subTitle">{{ subTitle }}</p>
            </div>
        </div>
        <div class="card-text" v-if="text">{{ text }}</div>
    </div>
    <footer v-if="footer">{{ footer }}</footer>
  </article>
</template>

<script>
export default {
    props: ['cover', 'thumbnail', 'title', 'subTitle', 'footer', 'text']
}
</script>

<style>
    .card {
        box-sizing: border-box;
        width: 280px;
        border: 1px solid #ccc;
        border-radius: 3%;
        margin: 10px;
    }

    .card:hover {
        background-color: #f7f7f7;
    }

    .card:active {
        background-color: #fff;
        border: 1px solid #443F98;
    }

    .card-body {
        margin: 10px;
        padding: 8px;
    }

    .card-text {
        padding: 5px;
    }

    .cover {
        background-color: #F0F0F0;
        width: 100%;
        height: 200px;
        background-position: center;
        background-size: cover;
        border-top-left-radius: 3%;
        border-top-right-radius: 3%;
    }

    .card-title-row {
        display: flex;
        flex-flow: row wrap;
        height: 55px;
        padding: 5px;
    }

    .title-text {
        width: 70%;
        padding-left: 10px;
    }
     p {
        font-size: 12px;
        color: #6E6E6E;
     }

    .thumbnail {
        background-color: #F0F0F0;
        background-position: center;
        background-size: cover;
        width: 20%;
        border-radius: 50%;
        margin-right: 15px;
    }

    footer {
        border-top: 1px solid #ccc;
        height: 50px; 
        display: flex;
        align-items: center;
        padding: 10px;
        font-size: 12px;
        color: #777777;
    }
</style>