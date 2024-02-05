# Accessible Modals v1.0
Modal windows setup enhanced for accessibility using the `<role>` attribute.

A modal window is a graphical component that is displayed when executing a control, link or button of a web page, with content inside it and that visually meets the following conditions:
1. The modal window and its content are shown in the foreground.
2. The content that remains in the background, within which the control that launched the modal window is located, is darkened and user interaction is disabled. Users *must* interact with the modal window before they can return to the parent window.

Navigation should be available only through the browser's system components, and through the elements contained in the modal. The document has the concept of a focus ring, which is the order in which elements obtain focus. All content outside the modal window should be ignored and interactive elements should be locked for user manipulation: clicking, focusing and navigating.

System-dependent input facilities (e.g., the `Tab` key on most desktop computers) should be supported to allow navigation between elements that can obtain focus, and conversely, going back with `Shift + Tab`, preventing the user from navigating to other parts of the document outside of the modal window. The focus is said to be “trapped” inside the dialog until the user explicitly decides to leave it.

In order to transmit this experience to blind people and people with reduced mobility, it will be necessary to develop the programming logic on the client side (frontend).

## Features
- Control that launches the modal window, preferably a `<button>`.
- Button description:
  - `aria-label` attribute for assistive technologies.
  - Show description with the `hover` and `focus` events.
- Container (light box):
  - `<div>` tag with `tabindex="-1"` attribute.
  - `role="dialog"` attribute for assistive technologies (modal window type component).
  - `aria-label` attribute to inform in which modal window the user is.
  - Level 1 section heading, `<h1>`. Inform assistive technologies that new content is being displayed.
  - Closing when pressing `ESC`, closing when clicking the close button, closing when clicking the background overlay.
  - `display: none` property. When it remains hidden, it is completely invisible.
  - If there is a lot of content, you must be able to **scroll** with the arrow keys.
- Keep reference to the element that opened the dialog: to return navigation focus to its original location when closing it.
- `aria-hidden="true"` attribute. Content in the background should be hidden from screen readers.
- Light/Dark mode color-scheme enabled.

## Sources
Javier Rodríguez en www.tecnologiaaccesible.com

Sunny Geek Beach (SGB) https://tech-es.netlify.app/articles/es526016/index.html

Usable y accesible. Blog de Olga Carreras (https://olgacarreras.blogspot.com/)

ARIAmodal 3.4.0 by Scott O'Hara (https://github.com/scottaohara/accessible_modal_window)

a11y-dialog  (https://github.com/HugoGiraudel/a11y-dialog)

module dialog.js 1.0.0 by Mads Stoumann (https://codepen.io/stoumann/pen/bGovmLa)

The Incredible Accessible Modal Window (https://github.com/gdkraus/accessible-modal-dialog)

w3.org	 Modal Dialog Example (https://www.w3.org/TR/wai-aria-practices/examples/dialog-modal/dialog.html)

## Try demo
[Accessible Modals](https://mixtim.github.io/accessModals/) 🔗
