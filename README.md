# Accessible Modals v1.0
Modal windows setup enhanced for accessibility using the `<role>` attribute.

A modal window is a graphical component that is displayed when executing a control, link or button of a web page, with content inside it and that visually meets the following conditions:
1. The modal window and its content are shown in the foreground.
2. The content that remains in the background, within which the control that launched the modal window is located, is darkened and user interaction is disabled. Users must interact with the modal window before they can return to the parent window.

Navigation should be available only through the browser's system components, and through the elements contained in the modal. The document has the concept of a focus ring, which is the order in which elements obtain focus. By default the focus ring shall be obtained using document order. All focusable elements must be part of the default focus ring.

It is essential that a container maintain a usable and consistent strategy when focus leaves a container and is then later refocused, by dynamically modifying elements' navigation attributes. All content outside the modal window should be ignored and interactive elements should be locked for user manipulation: clicking, focusing and navigating.

System-dependent input facilities (e.g., the `Tab` key on most desktop computers) should be supported to allow navigation between elements that can obtain focus, and conversely, going back with `Shift + Tab`, preventing the user from navigating to other parts of the document outside of the modal window. The focus is said to be “trapped” inside the dialog until the user explicitly decides to leave it.

In order to transmit this experience to blind people and people with reduced mobility, it will be necessary to develop the programming logic on the client side (frontend).

## Features
