<template>
    <div>
       <h1> testing </h1>
    </div>
</template>

<script>

    export default {
                data: function () {
            return {
                tweets: ['iam the best', 'first below', 'huh?'],
                num_friends: 99,
                logged_in: false,
            }
        },
        methods: {
            show_info: function() {
                document.body.insertAdjacentHTML(`beforeend`, `<h3>my num of friends: ${this.num_friends}</h3>
                <h3>is logged in? ${this.logged_in}</h3>`)
                for (let i = 0;i<this.tweets.length; i++) {
                    document.body.insertAdjacentHTML(`beforeend`, `the tweet ${i+1}: ${this.tweets[i]} <br>`)
                }

    
            
            }
        },

        mounted () {
            this.show_info();
            
        },
        name: 'script-example'
    }
</script>

<style scoped>

</style>