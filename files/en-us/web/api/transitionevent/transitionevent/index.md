---
title: TransitionEvent()
slug: Web/API/TransitionEvent/TransitionEvent
tags:
  - API
  - CSS
  - CSS3 Transitions
  - CSSOM
  - Constructor
  - Experimental
  - Reference
  - TransitionEvent
browser-compat: api.TransitionEvent.TransitionEvent
---
{{APIRef("CSSOM")}}{{SeeCompatTable}}

The **`TransitionEvent()`** constructor returns a newly created
{{domxref("TransitionEvent")}}, representing an event in relation with a transition.

## Syntax

```js
new TransitionEvent(type, {propertyName : aPropertyName,
                           elapsedTime  : aFloat,
                           pseudoElement: aPseudoElementName})
```

### Parameters

_The `TransitionEvent()` constructor also inherits arguments from
{{domxref("Event.Event", "Event()")}}._

- _type_
  - : A {{domxref("DOMString")}} representing the name of the type of the
    `TransitionEvent`. It is case-sensitive and can only be:
    `'transitionend'`.
- `propertyName` {{optional_inline}}
  - : A {{domxref("DOMString")}} containing the value of the
    {{cssxref("property-name")}} CSS property associated with the transition. It defaults
    to `""`.
- `elapsedTime` {{optional_inline}}
  - : Is `float` giving the amount of time the animation has been running, in
    seconds, when this event fired, excluding any time the animation was paused. For an
    `"animationstart"` event, `elapsedTime` is `0.0`
    unless there was a negative value for
    [`animation-delay`](/en-US/docs/Web/CSS/animation-delay),
    in which case the event will be fired with `elapsedTime` containing
    `(-1 * delay)`. It defaults to `0.0`.
- `pseudoElement` {{optional_inline}}
  - : A {{domxref("DOMString")}}, starting with `"::"`, containing the name
    of the [pseudo-element](/en-US/docs/Web/CSS/Pseudo-elements) the animation
    runs on. If the animation doesn't run on a pseudo-element but on the element, an empty
    string: ` ""``. ` It defaults to `""`.

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- [Using CSS transitions](/en-US/docs/Web/CSS/CSS_Transitions/Using_CSS_transitions)
- CSS properties: {{cssxref("transition")}}, {{cssxref("transition-delay")}},
  {{cssxref("transition-duration")}}, {{cssxref("transition-property")}},
  {{cssxref("transition-timing-function")}}.
