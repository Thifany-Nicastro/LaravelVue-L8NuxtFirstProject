<template>
	<b-container>
		<b-row>
			<b-col> 
                <b-card>
                    <template #header>
                        <h6 class="mb-0">Header Slot</h6>
                    </template>
                    <b-card-body>
                        <b-card-title>Card Title</b-card-title>
                        <b-card-sub-title class="mb-2">Card Sub Title</b-card-sub-title>
                        <b-card-text>
                            Some quick example text to build on the card title and make up the bulk of the card's
                            content.
                        </b-card-text>
                        <b-table striped hover responsive :items="items"></b-table>
                    </b-card-body>
                    <template #footer>
                        <em>Footer Slot</em>
                    </template>
                </b-card>
            </b-col>
		</b-row>
	</b-container>
</template>

<script>
    export default {
        data() {
            return {
                items: []
            }
        },

        // async fetch() {
        //     // this.items = await fetch(
        //     //     'https://jsonplaceholder.typicode.com/posts'
        //     // ).then(res => res.json())

        //     let { data } = await this.$axios.get("https://jsonplaceholder.typicode.com/posts");
        //     this.items = data;
        // }

        async asyncData({ $axios }) {
            let { data } = await $axios.get("https://jsonplaceholder.typicode.com/posts")
            return { items: data };
        },
    }
</script>