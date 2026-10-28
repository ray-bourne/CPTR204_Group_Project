# Contact Us page – Adrian Hinds

You build `contact.html`: a page banner, the contact form beside a contact-details card, and a Google Map. The form is worth 4 marks, and the map has to be an iframe (the lecturer's rule).

From Michiel: the office phone, email and hours, and the department's programme names for the dropdown.

Open `contact.html`, find `<main ...>`, delete the `TODO` comment and `<h1>Contact Us</h1>`, and paste these four blocks in order.

## Block 1 – Page banner

```html
<!-- PAGE BANNER: Bootstrap border + background utilities -->
<section class="bg-light border-start border-warning border-5 p-4 mb-5 rounded">
  <h1 class="text-navy mb-1">Contact Us</h1>
  <p class="lead mb-0">Questions about our programmes? Get in touch.</p>
</section>
```

## Block 2 – Contact form

This starts a 2-column row: the form on the left (7 columns), the details card on the right (5 columns, Block 3).

```html
<!-- GRID: form 7 cols + contact details 5 cols on large screens (BREAKPOINT lg) -->
<section class="row g-4 mb-5">
  <div class="col-lg-7">
    <!-- FORM: Bootstrap form classes (form-label, form-control, form-select, form-check) -->
    <form class="p-4 bg-light rounded shadow-sm" action="#" method="post">
      <h2 class="h4 text-navy mb-3">Send Us a Message</h2>
      <!-- FORM GRID: two fields side by side on md and up -->
      <div class="row g-3">
        <div class="col-md-6">
          <label for="fullName" class="form-label">Full Name</label>
          <input type="text" class="form-control" id="fullName" name="fullName" required>
        </div>
        <div class="col-md-6">
          <label for="email" class="form-label">Email</label>
          <input type="email" class="form-control" id="email" name="email" placeholder="name@example.com" required>
        </div>
        <div class="col-md-6">
          <label for="programme" class="form-label">Programme of Interest</label>
          <select class="form-select" id="programme" name="programme">
            <option selected disabled value="">Choose...</option>
            <option>Electrical &amp; Electronic Engineering</option>
            <option>Computer Systems Engineering</option>
            <option>Mathematics</option>
            <option>Other</option>
          </select>
        </div>
        <div class="col-md-6">
          <label for="phone" class="form-label">Phone (optional)</label>
          <input type="tel" class="form-control" id="phone" name="phone" placeholder="876-123-4567" pattern="[0-9]{3}-[0-9]{3}-[0-9]{4}">
        </div>
        <div class="col-12">
          <label for="subject" class="form-label">Subject</label>
          <input type="text" class="form-control" id="subject" name="subject" required>
        </div>
        <div class="col-12">
          <label for="message" class="form-label">Message</label>
          <textarea class="form-control" id="message" name="message" rows="5" required></textarea>
        </div>
        <div class="col-12">
          <div class="form-check">
            <input class="form-check-input" type="checkbox" id="news" name="news">
            <label class="form-check-label" for="news">Send me department news</label>
          </div>
        </div>
        <div class="col-12">
          <button type="submit" class="btn btn-warning px-4">Send Message</button>
        </div>
      </div>
    </form>
  </div>
  <!-- the contact details card (Block 3) goes here, still inside the section -->
</section>
```

- Every `<label for="email">` matches its input's `id="email"`, so clicking the label puts the cursor in the box.
- `required`, `type="email"` and `pattern` are Unit 6 validation: the browser blocks a bad submit by itself.
- The form has its own `row g-3` + `col-md-6` inside it: a grid inside a grid.

## Block 3 – Contact details card

```html
<!-- Paste this INSIDE the <section> from Block 2, right after the form's closing </div> -->
  <div class="col-lg-5">
    <!-- CARD: contact details -->
    <div class="card bg-navy text-white h-100 shadow-sm">
      <div class="card-body p-4">
        <h2 class="h5 text-warning">Department Office</h2>
        <ul class="list-unstyled mb-0">
          <li class="mb-2"><strong>Address:</strong> Northern Caribbean University, Manchester Road, Mandeville, Jamaica</li>
          <li class="mb-2"><strong>Phone:</strong> (confirm with Michiel)</li>
          <li class="mb-2"><strong>Email:</strong> (confirm with Michiel)</li>
          <li><strong>Office hours:</strong> Mon – Thu, 9:00 AM – 5:00 PM (confirm)</li>
        </ul>
      </div>
    </div>
  </div>
```

Delete the line `<!-- the contact details card (Block 3) goes here... -->` once you've pasted this in its place.

## Block 4 – Google Map

```html
<!-- MAP: Google Map iframe, ratio keeps its shape on any screen -->
<section class="mb-5">
  <h2 class="text-navy mb-3">Find Us</h2>
  <div class="ratio ratio-16x9 rounded overflow-hidden shadow-sm">
    <iframe src="PASTE-THE-EMBED-LINK-HERE" title="Map of Northern Caribbean University" allowfullscreen></iframe>
  </div>
</section>
```

To get the link: open Google Maps, search `Northern Caribbean University`, click **Share → Embed a map → Copy HTML**. Paste it into Notepad, copy only the long link inside `src="..."`, and put that where it says `PASTE-THE-EMBED-LINK-HERE`.

This page needs **no custom CSS**: every look comes from Bootstrap classes.

## Check before you push

- [ ] Click **Send Message** with empty boxes: the browser stops you
- [ ] Type `abc` as the email: the browser stops you
- [ ] Every `(confirm...)` placeholder replaced with real details
- [ ] Map shows NCU
- [ ] F12 → Ctrl+Shift+M: on a phone the details card drops below the form
- [ ] Commit & Push
