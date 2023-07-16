<script setup>
    import { RouterLink } from 'vue-router'
</script>
<template>
    <header>
        <div class="container">
        <div class="container-fluid">
            <nav class="navbar navbar-expand-lg bg-body-tertiary">
            <div class="container-fluid">
                <RouterLink to="/"
                ><img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="50" height="50"
                /></RouterLink>
                <button
                class="navbar-toggler"
                type="button"
                data-bs-toggle="collapse"
                data-bs-target="#navbarSupportedContent"
                aria-controls="navbarSupportedContent"
                aria-expanded="false"
                aria-label="Toggle navigation"
                >
                <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                    <li class="nav-item">
                    <RouterLink to="/about" class="nav-link" aria-current="page">About</RouterLink>
                    </li>
                    <li class="nav-item">
                    <RouterLink to="/crud" class="nav-link" aria-current="page">Crud</RouterLink>
                    </li>
                </ul>
                <form class="d-flex" role="search">
                    <input
                    class="form-control me-2"
                    type="search"
                    placeholder="Search"
                    aria-label="Search"
                    />
                    <button class="btn btn-outline-success" type="submit">Search</button>
                </form>
                </div>
            </div>
            </nav>
        </div>
        </div>
    </header>
</template>
