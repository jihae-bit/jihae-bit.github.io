## Final Project – Artist Website

This is my final project for the Intro to Programming class.  
I made a single page website using HTML and CSS. 
The website has three main parts:
  
- An About section  
- A Music section with YouTube videos  
- Link hub section

My original goal was to make a clean and simple website.

Good Outcome (Guaranteed) : 

A single-page site built with HTML and CSS that displays my name, a short introduction, embedded music links from spotify or Youtube. This project will help me practice web fundamentals while also creating something professional and personal.


### 1. HTML 
I created an `index.html` file and added the main sections for structure:

```html
<header> ... </header>
<section id="hero"> ... </section>
<section id="videos"> ... </section>
<section id="links"> ... </section>
<footer> ... </footer>
```
And I filled in these sections. 

For Hero section (about + portrait) :

```html
<section class="hero" id="hero">
  <div class="hero__content">
    <p class="eyebrow">Singer–Songwriter · Composer · Producer</p>
    <h1>Jihae Kimm</h1>
    <p>
     Jihae Kimm is a singer–songwriter, composer and producer based in Seoul and Boston.  Her work includes songs featured in films and Netflix original series. She has also directed music for a short film by renowned Korean producer Min Kyu-dong. She is currently attending Berklee College of Music on a full ride. <br><br> 
    </p>
    <div>
      <a class="btn btn-primary" href="#videos">Watch Featured Video</a>
      <a class="btn btn-secondary" href="#links">Explore Links</a>
    </div>
  </div>

  <div class="hero__visual">
    <img src="./portrait.jpg" alt="Jihae Kimm portrait" loading="lazy" />
  </div>
</section>
```

For Youtube Embeds: 

```html
<section class="section" id="videos">
  <div class="section__header">
    <p class="eyebrow">Featured Videos</p>
    <h2>OST and Scoring</h2>
  </div>

  <div class="videos__grid">
    <article class="video-card">
      <h3>Love in the Big City OST - Friends</h3>
      <div class="embed-container embed-16x9">
        <iframe
          src="https://www.youtube.com/embed/3_KVteYIq-M?rel=0"
          title="Jihae Kimm - Friends | 영화 LOVE in the BIG CITY 대도시의 사랑법 OST"
          allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
          loading="lazy"
          referrerpolicy="strict-origin-when-cross-origin"
        ></iframe>
      </div>
    </article>
```
   

For link hub section :
```html
 <section class="section" id="links">
        <div class="section__header">
          <p class="eyebrow">Link Hub</p>
        </div>
        <div class="links__actions">
          <div class="links__buttons">
            <a href="https://open.spotify.com/artist/1KWyMzq5aZmAVGNzNZru7A" target="_blank" rel="noreferrer">
              <span class="socicon socicon-spotify"></span>
              <span>Spotify</span>
            </a>
            <a href="https://music.apple.com/kr/artist/jihae-kimm/1770937091?l=en-GB" target="_blank" rel="noreferrer">
              <span class="socicon socicon-apple"></span>
              <span>Apple Music</span>
            </a>
            <a href="https://www.youtube.com/@jihae724" target="_blank" rel="noreferrer">
              <span class="socicon socicon-youtube"></span>
              <span>YouTube</span>
            </a>
            <a href="https://instagram.com/jihae.kimm" target="_blank" rel="noreferrer">
              <span class="socicon socicon-instagram"></span>
              <span>Instagram</span>
            </a>
            <a href="https://www.soundcloud.com/user-358391477" target="_blank" rel="noreferrer">
              <span class="socicon socicon-soundcloud"></span>
              <span>SoundCloud</span>
            </a>
          </div>
        </div>
      </section>
```
For footer section :
```html
<footer class="site-footer">
  <p>© 2025 Jihae Kimm</p>
</footer>
```


This gives the website its basic layout. And I added images and videos.
I used the `<img>` tag for the profile photo and `<iframe>` for YouTube videos.

HTML was for placing things on the page in the right order.

### 2. CSS

I used css to style and design the page.

I used simple CSS rules to control colors, font styles, spacing, and layout. 

To show social media icons, I used Socicons:
```css
@font-face {
  font-family: "Socicon";
  src: url("./socicon.woff") format("woff");
  font-weight: normal;
  font-style: normal;
  font-display: swap;
}
```
Here are some of the global CSS rules I used:

```css
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: "Cormorant Garamond", Georgia, "Times New Roman", serif;
  color: #1e1a16;
  background-color: #f5f0eb;
  line-height: 1.78;
}
 ``` 

Also, the hero section uses CSS Grid to create a two-column layout :
```css
.hero {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 3rem;
  align-items: center;
  padding: 4rem 5vw 5rem;
}
```
On wide screens: text and image sit side-by-side.
On narrow screens: it automatically stacks into one column.

Buttons share a .btn style. 

At the bottom of the CSS, I added media queries to adapt the layout on smaller screens.

##  Problems I Had (and How I Fixed Them)

### 1. Profile picture not loading
Even though I saved everything correctly with right names, image did not show on GitHub Pages.

Then I realized that might be because my original file name was in Korean, and GitHub had trouble reading it.

I renamed the file in English and updated the HTML and now it worked. 



###  2.YouTube video not loading
Even though the YouTube link was corret, the embed did not work at first. I didn't know how to fix this specific problem so I kept on working and after I hosted the page, the embed preview was available. 


##  Outcome

https://jihae-bit.github.io

