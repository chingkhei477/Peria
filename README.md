# Periva website

Static website for periva.in: plain HTML, CSS and JavaScript with no build step, plus one small PHP file for the contact form. There are no outside dependencies. The heading font is built into the stylesheet, so the site makes no requests to Google or other third parties.

## Preview on your computer

Unzip the folder and double-click `index.html`. Every page, link, menu and style works offline. The contact form opens your email app when used from your computer, because sending needs the live server.

## Upload

Upload everything in this folder to the web root of periva.in (for example `public_html` on Hostinger or any cPanel host), then turn on HTTPS (free SSL) in your hosting panel. Set `404.html` as the custom error page if your host does not pick it up automatically.

## Contact form

- On hosting with PHP (most shared hosting), messages go to support@periva.in through `contact.php`.
- Create the mailbox `no-reply@periva.in`, or change `PERIVA_FROM` at the top of `contact.php` to an address on your domain.
- If the server cannot send, or the host has no PHP, the form opens the visitor's email app with the message ready to send to support@periva.in.
- Send one test message after uploading.

## Adding offers

Open `assets/js/offers.js` and add one entry for each store you are approved to promote, with your affiliate tracking link. The format is described at the top of the file. The "Current offers" section and category filters appear automatically when the list has entries.

## Before launch, please check

1. **Legal review.** The policies are written for Indian law (DPDP Act 2023, IT Act 2000, Consumer Protection Act 2019). Have a lawyer review them.
2. **Grievance Officer.** The Consumer Protection (E-Commerce) Rules 2020 and the IT Rules may require you to publish the Grievance Officer's name and designation. If they apply, add them to the Grievance sections of `privacy-policy.html` and `terms.html`.
3. **Business rules assumed in the policies. Change any that differ:**
   - Joining, earning and redeeming are free.
   - Members must be 18+ and live in India, and must be signed in when they click through to a store.
   - Points are redeemed to UPI or an Indian bank account in the member's own name, or for gift vouchers. The account shows the value of points, any minimum redemption, any points validity period, and the number of points each voucher needs.
   - Referral points are earned when an invited friend's first eligible order is Confirmed. The number of points is shown in the member's account.
   - Issued gift voucher codes cannot be cancelled, but a faulty code is replaced or the points are restored.
   - Disputes are heard by courts with jurisdiction in Manipur.
4. **Member area.** The policies describe signing in, the points balance, redemptions and referral links. Add a "Sign in" link to the header once your member area is live.
5. **Analytics.** The site sets no cookies. If you add analytics or a Meta Pixel, update `cookie-policy.html` and add a consent banner.

## Files

| Path | Purpose |
| --- | --- |
| `*.html` | Home, Discover offers, How cashback works, About, Contact, five policies, 404 |
| `assets/css/periva.css` | All styles, light and dark themes, with the heading font built in |
| `assets/js/periva.js` | Mobile menu, contact form and offers list |
| `assets/js/offers.js` | Your offers list |
| `assets/img/` | Logo files (SVG), favicon, app icons and social sharing image |
| `assets/fonts/LICENSE-Lora.txt` | Licence note for the Lora typeface (SIL Open Font License) |
| `contact.php` | Contact form handler |
| `sitemap.xml`, `robots.txt` | For search engines. Submit the sitemap in Google Search Console |

## Brand

- Colours: Periva ink `#161B3D`, Periva blue `#3B47C4`, periwinkle `#8C97FF`, points gold `#E9A92B`, porcelain `#F6F6FB`
- Type: Lora SemiBold for headings, the device's system font for body text
- Logo: a "P" whose bowl is an orbit, with a gold point travelling around it. `logo.svg` (light backgrounds), `logo-white.svg` (dark backgrounds) and `logo-mark.svg` (app icon or profile picture)
