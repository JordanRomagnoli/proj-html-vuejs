<script>
    import JumbotronCarusell from '../components/JumbotronCarusell.vue';
    import SingleWork from '../components/SingleWork.vue';

    export default {
        data() {
            return { 
                listWork:[
                    {
                        img: 'image (14).svg',
                        title: 'array of equipment',
                        description: 'Lorem ipsum dolor amet, consectetur adipiscing. Pellentesque ultricies justo tellus.'
                    },
                    {
                        img: 'image (16).svg',
                        title: 'new technologies',
                        description: 'Lorem ipsum dolor amet, consectetur adipiscing. Pellentesque ultricies justo tellus.'
                    },
                    {
                        img: 'image (18).svg',
                        title: 'versitile actors',
                        description: 'Lorem ipsum dolor amet, consectetur adipiscing. Pellentesque ultricies justo tellus.'
                    },
                    {
                        img: 'image (15).svg',
                        title: 'top directors',
                        description: 'Lorem ipsum dolor amet, consectetur adipiscing. Pellentesque ultricies justo tellus.'
                    },
                    {
                        img: 'image (17).svg',
                        title: 'minute editing',
                        description: 'Lorem ipsum dolor amet, consectetur adipiscing. Pellentesque ultricies justo tellus.'
                    },
                    {
                        img: 'image (19).svg',
                        title: 'versitile actors',
                        description: 'Lorem ipsum dolor amet, consectetur adipiscing. Pellentesque ultricies justo tellus.'
                    },
                ]
            }
        },
        components :{

            JumbotronCarusell,
            SingleWork,
        },
        methods: {
            
        }
    }
    </script>

<template>
    <JumbotronCarusell/>
    <section>
        <div class="container text-center">
            <h6>
                pelicula studio
            </h6>
            <h2>
                this is what we do
            </h2>
            <div class="row flex-wrap">
                <SingleWork
                v-for="(elem, i) in listWork"
                :Image="elem.img"
                :Title="elem.title"
                :Description="elem.description"
                />
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
   section{
    padding: 40px 0;
    min-height: 500px;
    margin-top: 40px;

    .container{
        h6,h2{
            text-transform: uppercase;
        }
        > h6{
            
        }
        >h2{
            font-size: 2.8rem;
            font-weight: bold;
        }
        > div{
            margin-top: 40px;
        }
    }
   }
</style>
