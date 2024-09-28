<style>
    * {
        font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    }

    div {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: space-between;
        align-items: center;
        padding: 1rem;
        background-color: rgb(0, 71, 102);
        color: white;
    }

    nav a {
        color: white;
        text-decoration: none;
        margin-right: 1rem;
    }

    nav a:hover {
        text-decoration: underline;
    }

    .header {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        padding: 1rem;
        background-color: rgb(0, 71, 102);
        color: white;
    }

    @media(prefers-color-scheme: dark) {
        .header {
            background-color: #333;
            color: rgb(104, 149, 222);
        }

        .header-link {
            color: rgb(104, 149, 222);
        }
    }
</style>

<div class="header">
    <h1 class="site-name">MyBlog</h1>
    <nav>
        <a id="posts" class="header-link" href="/">Posts</a>
        <a id="top" class="header-link" href="/top">Top Posts</a>
        <a id="author"class="header-link" href="/contact">About the Author</a>
    </nav>
</div>