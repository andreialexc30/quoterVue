<template>
    <div class="content_wrapper">
        <!-- Main display -->
        <!-- Quote retrieved from API -->
        <blockquote class="displayed_quote">
            {{ displayedQuote }}
        </blockquote>
        <!-- Author retrieved from API -->
        <h2 class="displayed_author">{{ displayedAuthor }}</h2>
        <!-- API call -->
        <button @click="quote()" class="generator">Get a Quote</button>
    </div>
</template>

<script>
export default {
    data() {
        return {
            displayedQuote: '',
            displayedAuthor: ''
        }
    },
    methods: {
        async quote() {
            const quote = document.querySelector('.displayed_quote')
            const quoteAuthor = document.querySelector('.displayed_author')
            const endpoint = 'https://free-quotes-api.herokuapp.com'
            let res = await fetch(endpoint)
             if(!res.ok) {
                throw new Error(`HTTP Error. Status ${res.status}`)
            }

            let data = await res.json()
            this.displayedQuote = data.quote
            this.displayedAuthor = data.author || 'Unknown'
        }
    }
}
</script>