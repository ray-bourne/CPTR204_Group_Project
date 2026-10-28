# About Us page – Adrian Hamilton

You build `about.html`: a page banner, Mission and Vision, History with the department video, and 4 faculty cards. This page supplies the video the rubric asks for, so get it working early.

Files Michiel will push: `video/department-video.mp4`, `images/video-poster.jpg`, `images/faculty-1.jpg` to `faculty-4.jpg`, plus the mission, vision and history text. Until they arrive, the code still works; the pictures just show as broken.

Open `about.html`, find `<main ...>`, delete the `TODO` comment and `<h1>About Us</h1>`, and paste these four blocks in order.

## Block 1 – Page banner

```html
<!-- PAGE BANNER: Bootstrap border + background utilities -->
<section class="bg-light border-start border-warning border-5 p-4 mb-5 rounded">
  <h1 class="text-navy mb-1">About Us</h1>
  <p class="lead mb-0">Who we are and what we stand for.</p>
</section>
```

## Block 2 – Mission and Vision

```html
<!-- GRID: mission + vision side by side on md and up, stacked on phones (BREAKPOINT) -->
<section class="row g-4 mb-5">
  <div class="col-md-6">
    <!-- UTILITIES: bg-navy, text-white, p-4, rounded, shadow-sm -->
    <div class="p-4 h-100 bg-navy text-white rounded shadow-sm">
      <h2 class="h4 text-warning">Our Mission</h2>
      <p class="mb-0">Mission statement here.</p>
    </div>
  </div>
  <div class="col-md-6">
    <div class="p-4 h-100 bg-light rounded shadow-sm">
      <h2 class="h4 text-navy">Our Vision</h2>
      <p class="mb-0">Vision statement here.</p>
    </div>
  </div>
</section>
```

- `row` starts a grid row; `col-md-6` = half the width (6 of 12 columns) from 768 px up. On phones each box takes the full width and they stack.
- `h-100` makes both boxes the same height.

## Block 3 – History and video

```html
<!-- GRID: history text + video, 6 + 6 on large screens -->
<section class="row align-items-center g-4 mb-5">
  <div class="col-lg-6">
    <h2 class="text-navy">Our History</h2>
    <p>Two or three short paragraphs about the department.</p>
  </div>
  <div class="col-lg-6">
    <!-- VIDEO: ratio-16x9 keeps the video's shape on any screen -->
    <div class="ratio ratio-16x9 rounded overflow-hidden shadow">
      <video controls poster="images/video-poster.jpg">
        <source src="video/department-video.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
    </div>
  </div>
</section>
```

- The lecturer wants a downloaded .mp4 in a `<video>` tag, not a YouTube embed.
- `controls` shows play/pause; `poster` is the picture before it plays.

## Block 4 – Faculty cards

```html
<!-- CARDS: faculty - 1 per row on phones, 2 on sm, 4 on lg (BREAKPOINT) -->
<section class="mb-5">
  <h2 class="text-navy text-center mb-4">Meet Our Faculty</h2>
  <div class="row g-4">

    <div class="col-sm-6 col-lg-3">
      <!-- CARD -->
      <div class="card h-100 text-center shadow-sm">
        <!-- UTILITIES: rounded-circle + object-fit-cover make a round photo -->
        <img src="images/faculty-1.jpg" class="rounded-circle object-fit-cover mx-auto mt-4" width="120" height="120" alt="Photo of faculty member">
        <div class="card-body">
          <h3 class="card-title h6 text-navy mb-1">Name</h3>
          <p class="card-text small text-muted">Position</p>
        </div>
      </div>
    </div>

    <!-- Copy the col-sm-6 col-lg-3 block 3 more times (faculty-2 to faculty-4) -->

  </div>
</section>
```

Copy the whole `<div class="col-sm-6 col-lg-3"> ... </div>` block three more times. In each copy change the picture number, the name and the position.

This page needs **no custom CSS**: every look comes from Bootstrap classes.

## Check before you push

- [ ] Swap every placeholder line (`Mission statement here.`, `Name`, `Position`) for Michiel's real text
- [ ] Video plays and the poster shows
- [ ] Press F12 → Ctrl+Shift+M: at phone width everything stacks; at laptop width the faculty cards sit 4 across
- [ ] Commit & Push
