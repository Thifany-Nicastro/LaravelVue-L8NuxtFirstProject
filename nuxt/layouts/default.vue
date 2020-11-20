<template>
	<div>
       <header>
            <b-navbar toggleable="lg" type="light" variant="light">
                <b-navbar-brand href="#">NavBar</b-navbar-brand>
                <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
                <b-collapse id="nav-collapse" is-nav>
                    <b-navbar-nav>
                        <b-nav-item href="/">Home page</b-nav-item>
                        <b-nav-item href="/products">Products</b-nav-item>
                        <b-nav-item href="/products/create">Create</b-nav-item>
                    </b-navbar-nav>
                </b-collapse>
            </b-navbar>
        </header>

        <main class="mt-4">
            <Nuxt />
        </main>
	</div>
</template>