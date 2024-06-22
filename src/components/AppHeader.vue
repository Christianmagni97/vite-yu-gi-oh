<script>
export default {
    data() {
    return {

        }
    }
}
</script>

<template>
    <header>
        <nav>
            <ul>
                <li>
                    <img src="../assets/img/progetto tu gi oh .webp" alt="">
                </li>
                <li>
                    <p>
                        Title  Yu-Gi-Oh Api
                    </p>
                </li>
            </ul>
        </nav>
    </header>
</template>

<style lang="scss" scoped>
    @use './style/partials/mixins.scss' as*;
    @use './style/partials/variabls.scss' as*;

    img {
        width: 280px;
    }

    nav ul {
        padding: 5rem;
        display: flex;
        align-items: center;

        p{
            font-size: 3rem;
        }
    }
</style>