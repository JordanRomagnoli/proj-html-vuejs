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
    <section class="our-work">
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

    <section class="about-us">
        <div>
            <div class="container">
                <div class="row g-0 ">
                    <div class="col-6">
                        <h3>
                            about us
                        </h3>

                        <h2>
                            high quality cinematics
                        </h2>

                        <p>
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Totam repellendus delectus tempore facere hic. Enim incidunt commodi maiores quod pariatur corporis, ducimus sequi, facere excepturi temporibus hic perferendis illum aut?
                        </p>
                        
                        <a>read more</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

</template>

<style lang="scss" scoped>
   .our-work{
    padding: 40px 0;
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

   .about-us{
    background-color: #0a1010;
    background-image: url(../assets/img/About-Us.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    background-position: left;
        > div{
        
        .row{
            justify-content: flex-end;
            align-items: center;
            min-height: 500px;
                .col-6{
                    color: white;

                    >h3,h2,a{
                        text-transform: uppercase;
                        margin-bottom: 20px;
                    }

                    > h3{
                        font-size: 0.8rem;
                    }
                    > h2{
                        font-size: 2.2rem;
                        font-weight: bold;
                    }
                    >p{
                        line-height: 40px;
                        font-weight: 500;
                        margin-bottom: 40px;

                    }

                    > a{
                        background-color: white;
                        cursor: pointer;
                        color: black;
                        padding: 10px 40px;
                        font-size: 0.8rem;
                        border: none;
                        text-decoration: none;
                        font-weight: bold;
                        transition: all .2s ease-in-out;
                        &:hover{
                            background-color: black;
                            color: white;
                            border: 1px solid white;
                        }
                    }
                }
        }
    }
   }
   
</style>
