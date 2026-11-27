# Kitabash Academy website

A one-page website where learners post what they want to learn (coding, engineering subjects, school academics, English, money skills or anything else) along with their contact details. Each request comes to you so you can contact the learner personally.

It is a plain static site (HTML, CSS and JavaScript, with no build step), so GitHub Pages can host it for free.

## How requests reach you

GitHub Pages can't store form data, so the site sends each request one of two ways:

1. **By email through [Web3Forms](https://web3forms.com)** (recommended, free for 250 requests a month). Each request arrives in your inbox with all the details and a reference number like `KA-261127-AB12`. If the learner gave an email address, you can reply straight to them.
2. **By WhatsApp.** If you add your WhatsApp number, the site shows WhatsApp buttons. If Web3Forms isn't set up yet, submitting the form opens WhatsApp with the request already written out, ready for the learner to send to you.

## Setup (about 10 minutes, all in the browser)

### 1. Get your Web3Forms key
1. Go to https://web3forms.com, type the email address where you want to receive requests and click **Create Access Key**.
2. Copy the key they email you. It is safe to put in a public website.

### 2. Create the new GitHub repository
1. Sign in to your **new** GitHub account and click **+ → New repository**.
2. Name it, for example `kitabash-academy`, choose **Public** and click **Create repository**.
3. Click **uploading an existing file**. Drag in everything inside this folder (`index.html`, `config.js`, `favicon.svg`, `README.md` and the `assets` folder), not the folder itself. Click **Commit changes**.

### 3. Add your details to `config.js`
In the repository, open `config.js`, click the pencil icon and fill in:

```js
web3formsKey: "your-key-here",
whatsappNumber: "919876543210",   // country code + number, digits only
contactEmail: "hello@yourdomain.com",
contactPhone: "+91 98765 43210",
```

Click **Commit changes**.

### 4. Turn on GitHub Pages
1. Go to **Settings → Pages**.
2. Under **Build and deployment → Source**, choose **Deploy from a branch**.
3. Choose branch **main** and folder **/ (root)**, then click **Save**.
4. After a minute or two, the address appears at the top of that page, for example `https://<your-username>.github.io/kitabash-academy/`.

GitHub Pages is free for public repositories. Nothing in this website is secret, so public is fine.

### 5. Use your own domain (optional)
In **Settings → Pages → Custom domain**, enter something like `academy.kitabash.com`, then add the DNS record GitHub shows you at your domain provider.

### 6. Test it
Open the site, submit a test request and check that it arrives in your email.

## Changing the content
- **Subjects and areas:** edit the `CATEGORIES` list at the top of `assets/app.js`. The subject cards and the form drop-downs both read from this list.
- **Text, FAQ and form questions:** `index.html`.
- **Colours and fonts:** the variables at the top of `assets/styles.css` (they match the main Kitabash site).

## Preview on your computer
Open `index.html` in a browser. Everything works except sending email, which needs the Web3Forms key and an internet connection.
