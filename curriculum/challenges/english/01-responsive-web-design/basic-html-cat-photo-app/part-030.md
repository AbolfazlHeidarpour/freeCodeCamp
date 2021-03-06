---
id: 5efae16e3cbd2bbdab94e334
title: Part 30
challengeType: 0
isHidden: true
---

## Description
<section id='description'>

After the last `img` element, add a `figcaption` element with the text `Cats hate other cats.`

</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: "Your `figcaption` element should have an opening tag. Opening tags have the following syntax: `<elementName>`."
    testString: assert( document.querySelectorAll('figcaption').length === 2 );
  - text: Your `figcaption` element should have a closing tag. Closing tags have a `/` just after the `<` character.
    testString: assert( code.match(/<\/figcaption\>/g).length === 2 );
  - text: There should be a `figure` element right above the second `section` element's closing tag.
    testString: assert( $('main > section')[1].lastElementChild.nodeName === 'FIGURE' );
  - text: The last `img` element should be nested in the `figure` element.
    testString: const catsImg = document.querySelectorAll('figure > img')[1]; assert( catsImg && catsImg.getAttribute('src').toLowerCase() === 'https://bit.ly/fcc-cats');
  - text: "Your `figure` element should have an opening tag. Opening tags have the following syntax: `<elementName>`."
    testString: assert( document.querySelectorAll('figure').length === 2 );
  - text: Your `figure` element should have a closing tag. Closing tags have a `/` just after the `<` character.
    testString: assert( code.match(/<\/figure\>/g).length === 2 );
  - text: The `figcaption` element should be nested in the `figure` element.
    testString: assert( document.querySelectorAll('figure > figcaption').length === 2);
  - text: The `figcaption` element nested in the `figure` element should be below the `img` element. You have the `img` element and the `figcaption` element in the wrong order.
    testString: assert( document.querySelectorAll('figcaption')[1].previousElementSibling.nodeName === 'IMG');
  - text: The `figcaption` element should have the text `Cats hate other cats.` You have omitted a word or have a typo.
    testString: assert( document.querySelectorAll('figcaption')[1].innerText.toLowerCase().match(/Cats hate other cats\.?$/i));
    
```

</section>

## Challenge Seed
<section id='challengeSeed'>
<div id='html-seed'>

```html
<html>
  <body>
    <h1>CatPhotoApp</h1>
    <main>
      <section>
        <h2>Cat Photos</h2>
        <!-- TODO: Add link to cat photos -->
        <p>Click here to view more <a target="_blank" href="https://freecatphotoapp.com">cat photos</a>.</p>
        <a href="https://freecatphotoapp.com"><img src="https://bit.ly/fcc-relaxing-cat" alt="A cute orange cat lying on its back."></a>
      </section>
      <section>
        <h2>Cat Lists</h2>
        <h3>Things cats love:</h3>
        <ul>
          <li>cat nip</li>
          <li>laser pointers</li>
          <li>lasagna</li>
        </ul>
        <figure>
          <img src="https://bit.ly/fcc-lasagna" alt="A slice of lasagna on a plate.">
          <figcaption>Cats <em>love</em> lasagna.</figcaption>  
        </figure>
        <h3>Top 3 things cats hate:</h3>
        <ol>
          <li>flea treatment</li>
          <li>thunder</li>
          <li>other cats</li>
        </ol>
        <figure>
          --fcc-editable-region--
          <img src="https://bit.ly/fcc-cats" alt="Five cats looking around a field.">
          --fcc-editable-region--
        </figure>
      </section>
    </main>
  </body>
</html>
```

</div>
</section>
