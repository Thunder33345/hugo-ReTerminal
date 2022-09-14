+++
title = "Showcase"
date = "2018-07-18"
author = "Hello Robot"
toc = true
+++

## Header 2

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam nec interdum metus. Aenean rutrum ligula sodales ex auctor, sed tempus dui mollis. Curabitur ipsum dui, aliquet nec commodo at, tristique eget ante. **Donec quis dolor nec nunc mollis interdum vel in purus**. Sed vitae leo scelerisque, sollicitudin elit sed, congue ante. In augue nisl, vestibulum commodo est a, tristique porttitor est. Proin laoreet iaculis ornare. Nullam ut neque quam.

> Fusce pharetra suscipit orci nec tempor. Quisque vitae sem sit amet sem mollis consequat. Sed at imperdiet lorem. Vestibulum pharetra faucibus odio, ac feugiat tellus sollicitudin at. Pellentesque varius tristique mi imperdiet dapibus. Duis orci odio, sodales lacinia venenatis sit amet, feugiat et diam.

### Header 3

Nulla libero turpis, lacinia vitae cursus ut, auctor dictum nisl. Fusce varius felis nec sem ullamcorper, at convallis nisi vestibulum. Duis risus odio, porta sit amet placerat mollis, tincidunt non mauris. Suspendisse fringilla, `odio a dignissim pharetra`, est urna sollicitudin urna, eu scelerisque magna ex vitae tellus.

```css
/* PostCSS code */

pre {
  background: #1a1a1d;
  padding: 20px;
  border-radius: 8px;
  font-size: 1rem;
  overflow: auto;

  @media (--phone) {
    white-space: pre-wrap;
    word-wrap: break-word;
  }

  code {
    background: none !important;
    color: #ccc;
    padding: 0;
    font-size: inherit;
  }
}
```

```js
// JS code

const menuTrigger = document.querySelector('.menu-trigger')
const menu = document.querySelector('.menu')
const mobileQuery = getComputedStyle(document.body).getPropertyValue('--phoneWidth')
const isMobile = () => window.matchMedia(mobileQuery).matches
const isMobileMenu = () => {
  menuTrigger.classList.toggle('hidden', !isMobile())
  menu.classList.toggle('hidden', isMobile())
}

isMobileMenu()

menuTrigger.addEventListener('click', () => menu.classList.toggle('hidden'))

window.addEventListener('resize', isMobileMenu)
```

```html
<!-- HTML code -->

<section id="main">
  <div>
   <h1 id="title">{{ .Title }}</h1>
    {{ range .Pages }}
      {{ .Render "summary"}}
    {{ end }}
  </div>
</section>
```

#### Header 4

Curabitur scelerisque felis viverra varius scelerisque. Ut enim libero, molestie gravida blandit at, mollis ornare tellus. Cras arcu mi, ultrices vel pulvinar vel, volutpat eu tortor. Nullam nec eros quis massa ultrices iaculis sed in metus. Praesent sollicitudin sem sit amet orci tempor gravida.

- Maecenas elementum vitae nibh vitae porttitor.
- Aenean consequat, risus ut cursus placerat, arcu nulla sodales risus, ut molestie tellus tellus et dui.
- Integer imperdiet turpis vitae lacus imperdiet, ut ornare ligula auctor. Integer in mi eu velit vehicula suscipit eget vulputate nulla.
- Etiam vitae enim quis velit lobortis placerat a ut sem.
  - Curabitur lobortis ante sit amet orci pulvinar, sollicitudin viverra nunc accumsan.
  - Praesent fermentum orci quis leo facilisis posuere.

Aliquam erat volutpat. In hac habitasse platea dictumst. Nunc ut tincidunt mauris. Sed at gravida risus, id semper magna. Nullam vitae enim mattis, sodales neque non, pharetra elit. Cras sit amet sagittis augue, et finibus turpis. Ut tempus tincidunt diam vel pharetra. Nulla porttitor odio sit amet nulla scelerisque, quis aliquam mi imperdiet. Sed tincidunt dui vel tellus vestibulum rhoncus. Donec tempus ultrices velit.

### Checkboxes

Pharetra pharetra massa massa ultricies mi quis hendrerit.

- [ ] Ut consequat semper viverra nam libero.
- [ ] Mattis vulputate enim nulla aliquet porttitor lacus luctus accumsan.
- [X] Etiam dignissim diam quis enim lobortis scelerisque fermentum dui faucibus.
- [ ] Mi quis hendrerit dolor magna eget est lorem. Pellentesque eu tincidunt tortor aliquam.
- [X] Interdum velit euismod in pellentesque massa placerat duis.
- [X] A cras semper auctor neque vitae tempus quam pellentesque nec.

At ultrices mi tempus imperdiet nulla malesuada.


### Lists

- Morbi a purus id eros ornare porttitor non nec arcu.
- Etiam in mi feugiat, semper ipsum quis, rutrum dui.
- - Sed sollicitudin orci vel sapien tristique semper.
- - Duis vitae lacus in dolor rutrum sollicitudin eget sit amet erat.
- Sed sit amet elit malesuada, faucibus nibh sit amet, laoreet ligula.
- - Ut ut eros suscipit neque tincidunt vulputate.
- Fusce laoreet nisl scelerisque, vehicula tellus eget, maximus leo.
- - Vestibulum eget risus in mi ultrices consequat non in mi.
- - Quisque commodo dui sed erat imperdiet, eget tristique leo laoreet.
- Sed ullamcorper leo ac justo pellentesque porta.
- - Fusce eget odio efficitur, bibendum tortor id, tempus metus.
- - Maecenas ut lectus porttitor, tincidunt ipsum eget, vulputate erat.
- - Cras ac nunc aliquet, condimentum diam ac, posuere velit.

1. Vivamus posuere purus eu arcu scelerisque, sit amet molestie odio tempor.
1. Vestibulum euismod ante ornare hendrerit vehicula.
1. 1. Aliquam tristique massa eu fermentum ullamcorper.
1. 1. Curabitur convallis libero sit amet tortor maximus, sit amet mattis lorem consectetur.
1. 1. Nulla dapibus felis eu leo posuere consectetur.
1. 1. 1. Nullam viverra dolor vel lectus pulvinar mollis.
1. 1. 1. Sed sit amet risus in velit vehicula feugiat eget id augue.
1. 1. 1. Maecenas pulvinar dui vel porta ornare.
1. Mauris vitae elit quis massa tempor imperdiet sed eu tellus.
1. - Phasellus quis dolor eu tortor sagittis mattis.
1. - Aliquam ullamcorper risus vel nibh aliquet, at dapibus justo consequat.

- Vivamus posuere purus eu arcu scelerisque, sit amet molestie odio tempor.
- Vestibulum euismod ante ornare hendrerit vehicula.
- 1. Aliquam tristique massa eu fermentum ullamcorper.
- 1. Curabitur convallis libero sit amet tortor maximus, sit amet mattis lorem consectetur.
- 1. Nulla dapibus felis eu leo posuere consectetur.
- 1. 1. Nullam viverra dolor vel lectus pulvinar mollis.
