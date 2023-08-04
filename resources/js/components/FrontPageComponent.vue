<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="card">
                    <h1 class="card-header">TRACK ANALYZER</h1>

                    <div class="card-body">
                        Ever wanted to easily know what songs are included on a setlist or mix that is on a Youtube video?
                        Just enter the link to a Youtube video and find out what tracks you are bopping to!
                    </div>

                    <input id="videolink" class="textbox" name="videolink" type="text">
                    <button type="button" class="analyze">ANALYZE</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        mounted() {
            console.log('Component mounted.')
        }
    }
</script>

<style scoped>
    @font-face {
        font-family: "Lato";
        src: url("https://fonts.googleapis.com/css2?family=Lato&display=swap'");
    }
    .card {
        font-family: 'Lato', sans-serif;
        align-items: center;
        text-align: center;
    }
    .card-header {
        font-size: 34px;
        padding: 30px 10px 10px;
    }

    .textbox {
        margin: 20px 10px 20px;
        width: 30%;
        height: 30px;
    }

    .analyze {
        padding: 10px;
    }
</style>