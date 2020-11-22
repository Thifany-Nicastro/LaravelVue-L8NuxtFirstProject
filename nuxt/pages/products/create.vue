<template>
    <b-container>
		<b-row>
			<b-col> 
                <b-card>
                    <template #header>
                        <h6 class="mb-0">Header Slot</h6>
                    </template>
                    <b-card-body>
                        <b-form @submit.prevent="onSubmit" @reset="onReset">
                            <b-form-group id="input-group-1" label="Title" label-for="input-1" description="idk.">
                                <b-form-input id="title" v-model="post.title" type="text" placeholder="Enter title"></b-form-input>
                            </b-form-group>
                            <b-form-group id="input-group-1" label="Body" label-for="input-1" description="idk.">
                                <b-form-input id="body" v-model="post.body" type="text" placeholder="Enter Body"></b-form-input>
                            </b-form-group>

                            <b-button type="submit" variant="primary">Submit</b-button>
                            <b-button type="reset" variant="danger">Reset</b-button>
                        </b-form>
                    </b-card-body>
                </b-card>
            </b-col>
        </b-row>
    </b-container>
</template>

<script>
    export default {
        data() {
            return {
                post: {
                    title: '',
                    body: '',
                    userId: 1,
                }
            }
        },

        methods: {
            onSubmit () {
                console.log(this.post);
            },

            onReset () {
                this.post.title = '',
                this.post.body = ''
            },
        }
    }
</script>