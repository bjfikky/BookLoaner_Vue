<template>
    <v-app id="inspire" dark>

        <AppBar/>

        <v-content>
            <v-container fluid fill-height>
                <v-layout>
                    <v-flex shrink>
                        <router-view/>
                    </v-flex>
                </v-layout>
            </v-container>
        </v-content>

        <v-footer app fixed class="footer">
            <span>&copy; 2018 - Mary Pate | <small>Developed by Benjamin Orimoloye</small></span>
        </v-footer>
    </v-app>
</template>

<script>
    import AppBar from './components/navigation/AppBar'

    export default {
        components: {
            AppBar
        }
    }
</script>

<style scoped>
    .footer{
        padding: 20px;
    }
</style>