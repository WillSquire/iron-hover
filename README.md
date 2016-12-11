# \<iron-hover\>

Documentation and demo: http://willsquire.github.io/iron-hover/

A basic and fundamental component for tracking hover state in javascript

`iron-hover` is a utility element that detects the hover state of wrapped content in
Javascript. Use this element when the hover state is actionable via Javascript opposed
to only CSS (`:hover` styling covers this).

Whilst this element provides a convenient way to detect hover state, consider
implementing `IronHoverBehavior` on custom elements to avoid wrapping with
this element.

### Example

```html
<iron-hover hover="{{hover}}">
  <template is="dom-if" if="[[!hover]]">
    Not
  </template>
  Hover
</iron-hover>
```

# IronHoverBehavior
`IronHoverBehavior` is a utility behaviour that extends an element to detect the hover
state in Javascript. Inherit this behaviour when the hover state is actionable via
Javascript opposed to only CSS (`:hover` styling covers this).

### Example

The below example shows how to inherit IronHoverBehavior and trigger a function when
`hover` changes using a complex observer:

```javascript
Polymer({

  is: 'example-element',

  behaviors: [IronHoverBehavior],

  observers: ['_hoverChanged(hover)'],

  _hoverChanged: function(hover) {
    // do something with hover here...
  }

});
```
