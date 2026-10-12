# Devdhar Dent Care Website

Static website for **Devdhar Dent Care**, Laknawali Main Rd, near Shaheed Bhagat Singh School, Surajpur, Greater Noida, Uttar Pradesh 201306. Phone: 081303 02102.

Plain HTML, CSS and a little JavaScript. No build step, no dependencies.

## What the website includes

- Sticky header with a "Book an appointment" button
- Hero with typing "We offer" effect, call and WhatsApp buttons
- Services (20 cards), treatments gallery, doctor profile, clinic photos
- Sliding patient photo slideshow, patient videos (play when scrolled into view)
- Scrolling Google reviews
- **Working booking form**: it checks the details, then opens WhatsApp with a ready message (name, contact, service, date, time) to the clinic
- Floating WhatsApp, Call and Book buttons

## Folder structure

```
devdhar-dent-care/
  index.html                    the whole website
  assets/                       photos and patient videos
  .github/workflows/pages.yml   automatic deploy to GitHub Pages
  .nojekyll
  .gitignore
  README.md
```

## Put it on GitHub and publish it

1. Create a free account at github.com and click **New repository**. Name it, for example, `devdhar-dent-care`. Keep it **Public**.
2. On the new repository page click **uploading an existing file**. Drag in everything from inside this folder (`index.html`, `assets`, `.github`, `.nojekyll`, `README.md`, `.gitignore`) and click **Commit changes**.
   - The `.github` folder is hidden on some phones and computers. If it won't upload, use the git commands below, or skip it and use "Deploy from a branch" in step 3.
3. Go to **Settings > Pages**. Under **Source** choose **GitHub Actions** (uses the included workflow). Or choose **Deploy from a branch**, branch `main`, folder `/ (root)`.
4. Wait about a minute. Your website is live at `https://YOUR-USERNAME.github.io/devdhar-dent-care/`.

### Same thing with git commands

```bash
cd devdhar-dent-care
git init
git add .
git commit -m "Initial website"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/devdhar-dent-care.git
git push -u origin main
```

## Your own domain (optional)

Buy a domain, then in **Settings > Pages > Custom domain** enter it and follow the DNS steps GitHub shows. Tick **Enforce HTTPS**.

## Edit the content

Open `index.html` in any text editor.

- **Phone and WhatsApp number:** search for `8130302102` and replace it (country code 91 included) everywhere. Also change `918130302102` in the `WA_NUMBER` line near the bottom, which controls the booking form.
- **Address and hours:** search for `Laknawali` and `10:00`.
- **Google Maps links:** search for `maps.app.goo.gl` and `maps/dir`.
- **Reviews:** search for `class="rc"`. The first set of cards is shown to visitors and the second set is a copy used for the endless scroll, so edit both.
- **Photos and videos:** replace files in `assets/` using the same file names, or change the names in `index.html`.
- **Doctor details:** search for `Meet your dentist`.
- **Typing words under "We offer":** search for `var words`.

After editing, upload the changed files again. The site updates in about a minute.

## Booking form note

Requests are sent through WhatsApp only. They are not stored in a database or emailed. To receive them by email too, connect a free form service such as Formspree or Google Forms.

## Notes

- Patient photos, videos and reviews are shown on a public website. Keep written consent from every patient who appears.
- Videos start muted when scrolled into view, because browsers block autoplay with sound.
- Fonts load from Google Fonts. The site still works without them, with a fallback font.
