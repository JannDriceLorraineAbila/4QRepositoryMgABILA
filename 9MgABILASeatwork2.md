With default static positioning, the element stays in its normal place and you can’t move it using top or left. When you change the position (like relative or absolute), you can move the element using top, left, bottom, or right. So the change is that the element becomes movable and no longer stuck in its original position.
When you scroll the page, the footer stays fixed at the bottom of the screen and does not move.This happens because position: fixed; attaches the element to the viewport, not the page.Unlike position: relative;, which moves with the page, fixed keeps the footer always visible in the same spot.
`position: absolute;` lets you place an element anywhere using `top`, `left`, etc., and it moves relative to its nearest positioned parent. It scrolls with the page and doesn’t stay in one place.In contrast, `position: fixed;` stays stuck to the screen and does not move when you scroll.
The notice appears on top because it has a higher `z-index`, so it is layered above the other content.`z-index` controls which element is in front when they overlap.If you swap the values, the other content will appear on top and the notice will go behind.

guide questions:
a.
static is the default and cannot be moved.
relative can be moved but still stays in its original space.
absolute is placed anywhere based on its parent, while fixed stays in place on the screen even when you scroll.

b.
absolute positioning depends on its nearest positioned parent (not static).
If there is none, it uses the whole page as its reference.
That’s why its position changes depending on its parent.

c.
sticky acts like relative at first, but when you scroll, it sticks to a position (like top: 0).
fixed stays in one place the whole time, even before scrolling.
So sticky only “sticks” when you reach a certain point, while fixed is always stuck.

d.
I would use fixed for a header so important info (like event name) is always visible.
I could use absolute to place a “Register Now” button on top of a banner.
I might use sticky for a schedule so it stays visible while scrolling through details.