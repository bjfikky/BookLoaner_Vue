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

        <v-footer app fixed>
            <span>&copy; 2017</span>
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