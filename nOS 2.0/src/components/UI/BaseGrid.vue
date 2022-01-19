<template>
    <ul class="list-of-apps">
        <li v-for="app in apps"
        :key="app.id">
            <div >
                <img :src="require(`@/assets/${app.source}`)" :alt="app.name" class="desk-item">
                <h3>{{ app.name }}</h3>
            </div>
        </li>
    </ul>
</template>

<script>


export default {
    props:["id", "name", "source"],
    data(){
        return{
            apps:[
                {
                    id: "finder",
                    name: "Finder",
                    source: "finder.png",
                    
                },
                {
                    id: "settings",
                    name: "Settings",
                    source: "settings.png",
                    
                },
                {
                    id: "youtube",
                    name: "YouTube",
                    source: "youtube.png",
                    
                },
                {
                    id: "music",
                    name: "Music",
                    source: "music.png",
                    
                },
                {
                    id: "telegram",
                    name: "Telegram",
                    source: "telegram.png",
                    
                }
            ]
        }
    },
}
</script>

<style scoped>
    #list-of-apps{
    position: absolute;
    display: block;
    z-index: 2;
    }

    li{
        color: #fff;
        padding: 7px;
    }
    li:hover{
        background-color: rgba(119, 119, 119, 0.24);
    }
    ul{
        list-style: none;
    }
    a{
        text-decoration: none;
    }
    img{
        display: block;
        margin: 0 auto;
    }
    h3{
        font-size: 0.9rem;
        text-align: center;
        margin: 0;
        padding-top: 5px;
        padding-bottom: 7px;
    }

    .desk-item{
        height: 50px;
    }

    
</style>>

