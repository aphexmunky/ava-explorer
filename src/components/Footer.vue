<template>
    <v-footer color="#000">
        <div class="powered_by">
            <div class="header">
                <img src="@/assets/ava_logo_white.png">
                <h4>Powered by AVA</h4>
            </div>
            <p class="ava_desc">The AVA Explorer is a block explorer and analytics tool for AVA,
                a next-gen smart contracts platform for decentralization applications and the Internet of Finance.
            </p>
            <img class="yeti" src="@/assets/yeti_footer.png">
        </div>
        <div class="list">
            <h4>Menu</h4>
            <router-link to="/">Home</router-link>
            <router-link to="/validators">Validators</router-link>
            <router-link to="/tokens">Tokens</router-link>
            <router-link to="/resources">Resources</router-link>
<!--            <router-link to="/developers">Developers</router-link>-->
        </div>
        <div class="list">
            <h4>Social</h4>
            <a href="https://twitter.com/avalabsofficial" target="_blank"><fa :icon="['fab','twitter']"></fa> Twitter</a>
            <a href="https://discord.gg/Ja3CSs7" target="_blank"><fa :icon="['fab','discord']"></fa> Discord</a>
            <a href="https://www.reddit.com/r/ava/" target="_blank"><fa :icon="['fab','reddit']"></fa> Reddit</a>
        </div>
    </v-footer>
</template>
<style scoped lang="scss">
    @use '../main';
    .v-footer{
        padding-bottom: 0px !important;
        color: #fff !important;
        /*display: flex;*/
        align-items: flex-start;
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        column-gap: 60px;

        /*> div{*/
        /*    width: 100%;*/
        /*}*/
    }
    .powered_by{
        /*margin-right: 90px;*/
        /*width: 300px;*/


        .header{
            display: flex;
            align-items: center;
            font-size: 24px;

            h4{
                margin: 0;
            }

            img{
                width: auto;
                margin-right: 10px;
                height: 22px;
                object-fit: contain;
            }
        }
        p{
            margin: 24px 0px;
            font-size: 13px;
            font-weight: lighter;
        }

        img.yeti{
            width: 60%;
            max-width: 240px;
        }
    }

    .ava_desc{
        line-height: 1.5em;
    }

    .list{
        display: flex;
        flex-direction: column;
        /*min-width: 200px;*/
        /*margin-right: 60px;*/
        padding-bottom: 30px;

        font-size: 14px;

        &:last-of-type{
            margin: 0;
        }

        h4{
            padding-bottom: 8px;
            border-bottom: 1px solid #fff7;
        }

        a{
            font-weight: lighter;
            color: #fff !important;
            margin-bottom: 14px;
            text-decoration: none;


            svg{
                font-size: 16px;
                margin-right: 8px;
            }
        }
    }

    @media only screen and (max-width: main.$mobile_width) {
        .v-footer{
            grid-template-columns:none;
            grid-template-rows: max-content max-content max-content;

            padding: 20px 30px;
            padding-bottom: 0;
            flex-direction: column-reverse;
            justify-content: center;
        }

        .list{
            width: 100%;
        }


        .powered_by{
            grid-row: 3;
        }
    }
</style>
