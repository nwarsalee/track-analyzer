<template>
    <h1>TRACK ANALYZER</h1>
    <p>Want to find out what tracks are being played in a playlist or DJ mix on a Youtube video?</p>
    <p>Enter the URL to a Youtube video and find out!</p>

    <div>
        <input type="text" 
        v-model="urltext"
        placeholder="Insert URL...">
        <button type="button" @click="analyze">ANALYZE</button>
    </div>
</template>

<script>
export default {
  data() {
    return {
      urltext: '',
    };
  },
  methods: {
    analyze() {
        console.log("Textbox content: ", this.urltext);
        
        // TODO: Make appropriate error...
        if (!this.urltext) {
            console.log("No value entered for URL...");
        }

        // TODO: Parse Youtube link to ensure it works
        let videoId = this.parseLink(this.urltext)

        // TODO: Make call to backend
    },
    parseLink(url) {
        // Check if link is a youtube link
        if (!url.includes('https://www.youtube.com')){
            console.log("Bad link, doesn't direct to youtube...");
            return false;
        }
        // Parse video ID from URL
        let id = url.split("watch?v=")[1]

        console.log("Video ID is:", id)
    }
  },
};
</script>

<style>

</style>