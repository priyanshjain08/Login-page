# Lamp Login

An interactive login page where you pull a lamp's rope to turn the light on and reveal the login form. Pull it again and the lamp switches off and the form disappears.

Built with plain HTML, CSS and JavaScript in a single file. No libraries or build step.

## Features

- Pull-the-rope interaction (drag the knob down, or tap it) to toggle the lamp
- Lamp glow and warm background light when on
- Glassmorphism login card with a gold "Sign In" button
- Username and password validation
- Redirects to `sign-in.html` after a successful login
- Responsive layout: lamp beside the card on desktop, stacked on mobile
- Works with mouse and touch

## Files

```
project/
├── lamp-login.html   # the login page (this project)
├── sign-in.html      # the page opened after login (you provide this)
└── README.md
```

## How to run

1. Put `lamp-login.html` and `sign-in.html` in the same folder.
2. Open `lamp-login.html` in any modern browser.
3. Pull the rope to turn the lamp on, then log in.

## Default credentials

| Field    | Value          |
|----------|----------------|
| Username | `Priyansh Jain` (not case-sensitive) |
| Password | `pj_08` (case-sensitive) |

## Customisation

All of these are in the `<script>` at the bottom of `lamp-login.html`.

**Change the credentials**

```js
if(u.toLowerCase()==='priyansh jain'&&p==='pj_08'){
```

**Change the page opened after login**

```js
setTimeout(()=>{window.location.href='sign-in.html'},600)
```

**Change the colours**: edit the gradient values in the CSS (`button.sign` for the gold button, `body.on .scene` for the warm background light).

**Rope sensitivity**: a pull of more than 35px toggles the lamp. Change `pull>35` in the `end()` function.

## Notes

- The credentials are stored in the page's JavaScript, so anyone can read them with "View source". This is fine for a demo or learning project, but a real login must check credentials on a server.
- The redirect uses a relative link, so `sign-in.html` must sit next to `lamp-login.html`.

## Browser support

Any current version of Chrome, Edge, Firefox or Safari, on desktop and mobile.
