<script>
  import marked from "marked";
  $: mdown = `# Publication

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
    height: 100%;
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
    width: 40%;
    height: 90vh;
    border: 3px dashed #000;
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

    article {
      max-height: 75%;
    }
  }
  
</style>

<main>
  <section>
  <h2>Markdown</h2>
    <textarea bind:value={mdown} />
  </section>
  
  <section class="view">
  <h2>View</h2>
    <article>
      {@html marked(mdown)}
    </article>
  </section>
</main>
