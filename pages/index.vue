<template>
    <div>
        <header>
            <nav>
                <NuxtLink to="/">Home</NuxtLink>
                <NuxtLink to="/about">About</NuxtLink>
                <NuxtLink to="/skills">Skills</NuxtLink>
                <NuxtLink to="/projects">Projects</NuxtLink>
                <NuxtLink to="/contact">Contact</NuxtLink>
            </nav>
        </header>

        <main>
            <Nuxt />
        </main>

        <Footer>
            <p>&copy; 2024 My Portfolio</p>
        </Footer>
    </div>
</template>