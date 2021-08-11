<template>
    <body>
        <div id="wrapper">
            <h1 :id="colorChange">TWEET LIST</h1>
            <button @click="changeDisplay()">Toggle Layout</button>
            <div :class="{ gridContainer: isActive }">
                <p class="tweetItem" v-for="i in allTweets" v-bind:key="i.id">{{ i.tweet }} &#128640;<br>{{ i.user}}<br>{{ i.dateCreated}}</p>
            </div>
        </div>
    </body>
</template>

<script>
    export default {
        name : "VueTweets",
        data : () => {
            return {
                isActive : false,
                allTweets : [
                    {   
                        id : 1,
                        tweet : "DOGE TO THE MOON",
                        user : "Elon Musk",
                        dateCreated : "7-20-2021"
                    },
                    {   
                        id : 2,
                        tweet : "BTC TO THE MOON",
                        user : "Jeff Bezos",
                        dateCreated : "7-21-2022"
                    },
                    {   
                        id : 3,
                        tweet : "ETH TO THE MOON",
                        user : "Richard Branson",
                        dateCreated : "1-11-2024"
                    },
                    {   
                        id : 4,
                        tweet : "XRP TO THE MOON",
                        user : "Mark Zuckerberg",
                        dateCreated : "12-23-2050"
                    },
                    {   
                        id : 5,
                        tweet : "SHIB TO THE MOON",
                        user : "Warren Buffett",
                        dateCreated : "08-20-2000"
                    },
                      {   
                        id : 6,
                        tweet : "ETC TO THE MOON",
                        user : "Bill Gates",
                        dateCreated : "08-20-1997"
                    }
                ]
            }
        },
        methods : {
            changeDisplay() {
                console.log("BUTTON CLICKED");
                this.isActive = !this.isActive;
            }
        }
    }

</script>

<style scoped>
    body {
        padding: 0;
        box-sizing: border-box;
        margin-left: 15vw;
        margin-right: 15vw;
    }

    #wrapper {
        background: azure;
    }
    .gridContainer {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
        background-color: rgb(155, 155, 199);
    }

    #special {
        color: brown;
    }
    
    button {
        box-shadow:inset 0px 1px 0px 0px #bbdaf7;
        background:linear-gradient(to bottom, #79bbff 5%, #378de5 100%);
        background-color:#79bbff;
        border-radius:6px;
        border:1px solid #84bbf3;
        display:inline-block;
        cursor:pointer;
        color:#ffffff;
        font-size:15px;
        font-weight:bold;
        padding:12px 24px;
        text-decoration:none;
        text-shadow:0px 1px 0px #528ecc;
    }

    .tweetItem {
        border-bottom: 1px black solid;
        padding: 4vh 0;
    }

</style>