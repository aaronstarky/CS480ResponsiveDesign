<script>
    export let pubDate;
    export let author;
    export let readingEstimate;
    export let postTitle;
    export let contentPreview;
    export let imagePath;
    export let likeCount;

    /**
     * @param {string} numLikes
     */
    export function createLikeString(numLikes) {
        return numLikes == "1" ? numLikes + " like" :  numLikes + " likes"
    }
</script>

<style>
    #card {
        display: flex;
        flex-direction: column;
        border-radius: 5px;
        border-width: 2px;
        border-style: solid;
        padding: 10px 10px;
        margin: 10px;
        max-width: 300px;
        height: 350px;

        border-width: 2px;
        border-radius: 5px;
        border-color: grey;
        color: #000;
    }

    #author {
        font-weight: bold;
    }

    #pubDate, #reading-estimate {
        color: rgb(106, 106, 106);
    }

    img {
        object-position: 100% 50%;
        max-height: 150px;
        object-fit:cover;
        border-radius: 5px;
    }

    #post-info {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
    }

    @media(prefers-color-scheme: dark) {
        #card {
            background-color: #000;
            color: rgb(104, 149, 222);
            border-color: rgb(112, 126, 144);
        }

        #pubDate, #reading-estimate {
            color: rgb(106, 106, 106);
        }

        img {
            filter: brightness(75%);
        }
    }
</style>

<div id="card">
    <img src={imagePath} alt="banner"/>
    <br>
    <div id="post-info">
        <div id="text">
            <div id="author">
                {author}
            </div>
            <div id="pubDate">
                {pubDate}
            </div>
            <div id="reading-estimate">
                {readingEstimate}
            </div>
        </div>
        <div id="likes">
            {createLikeString(likeCount)}
        </div>
    </div>
    <h3 id="post-title">
        {postTitle}
    </h3>    
    <div id="content-preview">
        {contentPreview}
    </div>  
</div>
  