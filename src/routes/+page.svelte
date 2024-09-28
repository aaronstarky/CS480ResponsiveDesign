<script>
    import Header from "./header.svelte";
    import Footer from "./footer.svelte";
    import Post from "./post.svelte";
    import louvreCourtyard from '$lib/louvre-courtyard.jpg';
    import pingpong from '$lib/pingpong.jpg';
    import parisBridge from '$lib/paris-bridge.jpg';
</script>

<style>
    * {
        font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    }


    #posts {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        flex-wrap: wrap;
        padding: 1rem;
        color: black;
    }

    @media (prefers-color-scheme: dark) {
        :root {
            --background-color: #333;
            --color: rgb(104, 149, 222);
        }
        
        #posts {
            background-color: #222222;
            color: var(--color);
        }
        
        body {
            background-color: #222222;
        }
    }
</style>

<body>
    <Header/>
    <div id="posts">
        <Post
            imagePath={louvreCourtyard}
            pubDate="2021-01-01"
            author="John Doe"
            readingEstimate="5 minutes"
            postTitle="My First Post"
            contentPreview="To give you a preview of what I am about to tell you would be criminal."
            likeCount="1"
        />
        <Post
            imagePath={pingpong}
            pubDate="2021-01-02"
            author="Jane Shrek"
            readingEstimate="10 minutes"
            postTitle="My Second Post"
            contentPreview="It all started when I watched Shrek for the first time..."
            likeCount="5"
        />
        <Post
            imagePath={parisBridge}
            pubDate="2021-01-03"
            author="Hunter Henrichsen"
            readingEstimate="7 minutes"
            postTitle="My Third Post"
            contentPreview="I am learning so much while learning Svelte! Here are the top three things I have learned."
            likeCount="25"
        />
    </div>
    <Footer/>
</body>