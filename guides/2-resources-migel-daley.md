# Resources page – Migel Daley

You build `resources.html`: a page banner, the accordion (4 items) beside a help card, and 3 resource cards. The accordion is worth 6 marks on its own, so test it carefully.

Files Michiel will push: `images/resource-1.jpg` to `resource-3.jpg`, plus text for the 4 accordion items.

Open `resources.html`, find `<main ...>`, delete the `TODO` comment and `<h1>Resources</h1>`, and paste these three blocks in order.

## Block 1 – Page banner

```html
<!-- PAGE BANNER: Bootstrap border + background utilities -->
<section class="bg-light border-start border-warning border-5 p-4 mb-5 rounded">
  <h1 class="text-navy mb-1">Resources</h1>
  <p class="lead mb-0">Guides, tools and support for your studies.</p>
</section>
```

## Block 2 – Accordion and help card

```html
<!-- GRID: accordion 8 cols + help card 4 cols on large screens, stacked below (BREAKPOINT lg) -->
<section class="row g-4 mb-5">
  <div class="col-lg-8">
    <h2 class="text-navy mb-3">Student Resources</h2>

    <!-- ACCORDION: 4 items, first one open -->
    <div class="accordion" id="resourceAccordion">

      <!-- ACCORDION ITEM 1 (open) -->
      <div class="accordion-item">
        <h3 class="accordion-header">
          <button class="accordion-button" type="button" data-bs-toggle="collapse"
                  data-bs-target="#res1" aria-expanded="true" aria-controls="res1">
            Study Guides &amp; Past Papers
          </button>
        </h3>
        <div id="res1" class="accordion-collapse collapse show" data-bs-parent="#resourceAccordion">
          <div class="accordion-body">Text about study guides and where to find past papers.</div>
        </div>
      </div>

      <!-- ACCORDION ITEM 2 (closed) -->
      <div class="accordion-item">
        <h3 class="accordion-header">
          <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
                  data-bs-target="#res2" aria-expanded="false" aria-controls="res2">
            Labs &amp; Equipment
          </button>
        </h3>
        <div id="res2" class="accordion-collapse collapse" data-bs-parent="#resourceAccordion">
          <div class="accordion-body">Text about the labs.</div>
        </div>
      </div>

      <!-- ITEM 3: copy item 2, change res2 to res3, title "Software &amp; Tools" -->
      <!-- ITEM 4: copy item 2, change res2 to res4, title "Frequently Asked Questions" -->

    </div>
  </div>

  <div class="col-lg-4">
    <!-- CARD: help box -->
    <div class="card bg-navy text-white h-100 shadow-sm">
      <div class="card-body">
        <h2 class="h5 text-warning">Need Help?</h2>
        <p class="card-text">Can't find what you need? Our staff are happy to point you in the right direction.</p>
        <a href="contact.html" class="btn btn-warning">Contact Us</a>
      </div>
    </div>
  </div>
</section>
```

**Making items 3 and 4:** copy the whole ITEM 2 block (from `<div class="accordion-item">` to its closing `</div>`). In the copy, change `res2` to `res3` in **all three places** (`data-bs-target`, `aria-controls` and `id`), then change the title and text. Do the same with `res4` for item 4.

The 3 rules that make an accordion work:

1. Each button's `data-bs-target="#res2"` matches its panel's `id="res2"`. Every item needs a different number.
2. Every panel has `data-bs-parent="#resourceAccordion"`, so opening one closes the others.
3. Only item 1 has `show` on the panel and no `collapsed` on the button. Items 2–4: `collapsed` on the button, no `show`.

## Block 3 – Resource cards

```html
<!-- CARDS: 3 resources - 1 per row on phones, 3 on md and up (BREAKPOINT) -->
<section class="row g-4 mb-5">
  <div class="col-md-4">
    <!-- CARD -->
    <div class="card h-100 shadow-sm">
      <img src="images/resource-1.jpg" class="card-img-top" alt="Students in the library">
      <div class="card-body">
        <h3 class="card-title h5 text-navy">Library</h3>
        <p class="card-text">Short description.</p>
        <a href="contact.html" class="btn btn-navy">Visit</a>
      </div>
    </div>
  </div>
  <!-- Copy the col-md-4 block twice more (resource-2, resource-3) -->
</section>
```

If Michiel finds a real web page for a resource, point that card's `Visit` button there instead of `contact.html`.

This page needs **no custom CSS**: every look comes from Bootstrap classes.

## Check before you push

- [ ] All 4 accordion items open, and opening one closes the one before
- [ ] Placeholder text replaced with Michiel's real text
- [ ] F12 → Ctrl+Shift+M: on a phone the help card drops below the accordion and the cards stack
- [ ] Commit & Push
