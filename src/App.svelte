<script>
  import marked from "marked";
  let value = `# Publication

Publishing in StackEdit makes it simple for you to publish online your files. Once you're happy with a file, you can publish it to different hosting platforms like **Blogger**, **Dropbox**, **Gist**, **GitHub**, **Google Drive**, **WordPress** and **Zendesk**. With [Handlebars templates](http://handlebarsjs.com/), you have full control over what you export.

> Before starting to publish, you must link an account in the **Publish** sub-menu.`;

</script>

<style>

  main {
    display: flex;
    justify-content: center;
    align-items: center;
    margin: auto;
    width: 100%;
    height: 90%;
  }

  textarea {
    border: none;
    width: 100%;
    height: 90%;
  }

  textarea:focus {
    outline: none;
  }

  textarea {
    margin-top: 1rem;
  }

  section {
    display: inline-block;
    margin: 1rem;
    padding: 1.5rem;
    width: 45%;
    height: 70vh;
    border: 3px dashed #000;
  }

  h1 {
    text-align: center;
    margin: 15px 0;
  }

  h2 {
    display: inline;
    text-decoration: underline;
    font-size: 2rem;
  }

  article {
    padding: 1rem;
    height: 90%;
    overflow: auto;
  }

  @media (max-width:720px) {
    main {
      display: block;
      width: 100%;
      margin: auto;
    }

    section {
      display: block;
      margin: 1rem;
      padding: 0.5rem;
      width: 85%;
      height: 45vh;
    }

    textarea {
    border: none;
    width: 100%;
    height: 80%;
  }

    article {
      max-height: 75%;
    }
  }

</style>

<h1>Online Markdown Editor</h1>
<main>
  <section>
  <h2>Markdown</h2>
    <textarea bind:value />
  </section>

<!-- <section>
  <h2>Html</h2>
  <article>
      {marked(value)}
    </article>
</section> -->

  <section class="view">
  <h2>Document</h2>
    <article class="post-description">
    <div>
      {@html marked(value)}
    </div>
      
    </article>
  </section>
</main>
