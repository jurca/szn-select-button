# szn-select-button

UI button for the accessible HTML selectbox with customizable UI: szn-select.

This element is not meant to be used on its own; it is meant to be used by the
`szn-select` custom element.

## Usage

Create an empty `szn-select-button` element, the element is configured
entirely by its JavaScript API.

```html
<szn-select-button></szn-select-button>
```

The element must be linked to the `select` element it is to represent:

```js
selectButton.setSelectElement(selectElement)
```

The element adjusts its appearance based on whether the single-select dropdown
is currently opened and whether it's a dropdown or a dropup. However, the
element cannot determine the state of the dropdown on its own, so it has to be
notified using the following JavaScript API:

```js
// notifies the button that the dropdown is visible
selectButton.setOpen(true)
// notifies the button that the dropdown is no longer visible
selectButton.setOpen(false)

// notifies the button that the dropdown is actually a dropup
selectButton.setOpeningPosition(selectButton.OPENING_POSITION.UP)
// notifies the button that the dropdown is, well, a dropdown
selectButton.setOpeningPosition(selectButtonbutton.OPENING_POSITION.DOWN)
```
