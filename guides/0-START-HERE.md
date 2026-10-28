# Math & Engineering Website – Team Guides

We're building a 4-page Bootstrap 5 website for NCU's **Department of Mathematics & Engineering**. Moodle deadline: **Nov 9, 11:59 PM**, no late submissions. Read this first, then open your own guide in this `guides` folder.

## Who does what

| Person | Job | Your files |
| --- | --- | --- |
| Ray-Shaun Bourne | Wireframe, Home page, header/navbar/footer, repo owner | `index.html`, `css/style.css` |
| Adrian Hamilton | About Us page | `about.html` |
| Migel Daley | Resources page | `resources.html` |
| Adrian Hinds | Contact Us page | `contact.html` |
| Michiel Williams | Images, video, department facts; demo support | `images/`, `video/` |

## Deadlines

- Michiel's content pushed: Oct 30, 2026
- Your page's first draft pushed: Nov 3, 2026
- Your page finished: Nov 6, 2026
- Ray submits to Moodle (a day early): Nov 8, 2026

## One-time setup

1. Send Ray your GitHub username.
2. Accept Ray's GitHub invite (check your email). Without it you can't save to the repo.
3. That's it: we use **github.dev**, VS Code in the browser, so there's nothing to install.

## Every time you work

1. Open the repo on github.com and press `.` (full stop). It opens in github.dev.
2. Click your file in the Explorer on the left and edit it.
3. To add images or the video, drag them from your computer onto the `images` or `video` folder in the Explorer.
4. When you stop: click the **Source Control** icon (third icon down on the left), type a short message (e.g. `Added faculty cards`), click **Commit & Push**.
5. To see your page, open the GitHub Pages link Ray posts, about a minute after you commit. github.dev can't preview the page itself.
6. Close the tab when done. Next time open github.dev fresh so you get everyone's latest work.

## Rules

- Only touch your own page. The header, navbar and footer are already done and must stay the same on every page; ask Ray for any change there.
- Build only inside `<main class="container py-5 flex-grow-1"> ... </main>`. Delete the `TODO` comment and placeholder `<h1>` first.
- Put a searchable comment above every Bootstrap feature, like `<!-- ACCORDION -->`, so Ray can find it fast in the demo.
- Image and video names: lowercase, no spaces (`lab-1.jpg`).
- Open github.dev fresh before you start; Commit & Push when you stop.

## Use Bootstrap, not custom CSS

The lecturer wants us using Bootstrap 5.3 classes, so **don't write CSS** for your page. The one shared CSS file (`css/style.css`) only adds our NCU navy and fonts. Docs: [getbootstrap.com/docs/5.3](https://getbootstrap.com/docs/5.3/getting-started/introduction/).

| For | Use |
| --- | --- |
| NCU navy | `bg-navy`, `text-navy`, `btn-navy` (ours) |
| Gold | `text-warning`, `btn-warning`, `border-warning` (Bootstrap's) |
| Light background | `bg-light` |
| Spacing | `p-4`, `mb-5`, `g-4` |
| Look | `rounded`, `shadow-sm`, `opacity-75`, `bg-opacity-50` |
