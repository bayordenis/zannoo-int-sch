# Zannoo International School Website

The public website for Zannoo International School. It presents the school, supports the admissions and social media campaign, and links staff to the academic portal.

## What's included

- **One file:** `zannoo-website.html` holds all the page content, styling and scripts.
- **Sections:** Home, About, Academics (Early Years, Primary, JHS), School Life, News & Events, Parent Testimonials, Follow & Share, Admissions, Contact.
- **Social media:** links to Facebook, Instagram, TikTok, YouTube, X and WhatsApp, a floating WhatsApp chat button, and share buttons for the `#ChooseZannoo` campaign.
- **Staff Portal:** links to the school management system at https://zannoo.adesua360.com (top bar, main menu and footer).
- **Works on phones, tablets and computers**, in light and dark mode.

## Plugins used

Both load from the internet, so nothing needs installing.

| Plugin | Purpose |
| --- | --- |
| Font Awesome 6.5.1 | Icons and social media logos |
| Google Fonts (Fraunces, Nunito Sans) | Headings and body text |

The menu, testimonial slider, share buttons and form checks use plain JavaScript.

## Putting the site online

1. Add these lines to the very top of `zannoo-website.html` so the page displays correctly on phones:
   ```html
   <!DOCTYPE html>
   <meta charset="utf-8">
   <meta name="viewport" content="width=device-width, initial-scale=1">
   ```
2. Rename the file to `index.html`.
3. Upload it to the school's web hosting (cPanel, Netlify, GitHub Pages or similar), in the main folder of the domain, for example `zannooschool.edu.gh`.

## Before going live

Replace these placeholders in `zannoo-website.html`:

- [ ] **School colours:** edit `--brand` (main colour) and `--accent` (second colour) at the top of the `<style>` section. The dark-mode versions are in the two lines just below.
- [ ] **Social media links:** each link currently points to the platform's home page (for example `https://www.facebook.com/`). Replace with the school's own pages.
- [ ] **WhatsApp number:** replace `233000000000` with the school's number in international format, without `+` or spaces.
- [ ] **Phone, email, address and GhanaPost GPS** in the top bar and Contact section.
- [ ] **Crest:** replace the drawn "Z" crest with the school logo.
- [ ] **Photos:** replace the coloured tiles in School Life with real photos.
- [ ] **Testimonials:** replace the sample quotes with real ones, with parents' permission.
- [ ] **News items:** update with current events and dates.

## Making the enquiry form send messages

The admissions form checks the entries and shows a thank-you message, but it does not send anything yet. To receive enquiries by email:

1. Create a free form at [formspree.io](https://formspree.io) and copy its form address.
2. In the file, change `<form id="enquiry" novalidate>` to `<form id="enquiry" action="YOUR-FORMSPREE-ADDRESS" method="POST">`.
3. In the script near the bottom of the file, remove the line `e.preventDefault();` so the form submits.

## Updating the site

- **Text:** find the words in the file and edit them directly.
- **News:** each news item is an `<article class="post">` block. Copy one and change its text.
- **Staff Portal address:** search for `adesua360` and update all three links if it ever changes.
