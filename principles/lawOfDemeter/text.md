<link rel="stylesheet" href="{{baseUrl}}/css/textbook.css">

<div class="website-content">

<div id="path">Principles :arrow_right: </div>

<div id="title">

#### Law of Demeter :three:

</div>

<div id="body">

<tip-box type="primary">

<include src="../../common/definitions.md#def-law-of-demeter" />

</tip-box>

More concretely, a method m of an object O should invoke only the methods of the following kinds of objects:

* The object `O` itself
* Objects passed as parameters of `m`
* Objects created/instantiated in `m`
* Objects from the direct association of `O`

<tip-box>

Example:

The following code fragment violates LoD due to the reason: while `b` is a ‘friend’ of `foo` (because it receives it as a parameter), `g` is a ‘friend of a friend’ (which should be considered a ‘stranger’), and `g.doSomething()` is analogous to ‘talking to a stranger’.

```java
void foo(Bar b) {
    Goo g = b.getGoo();
    g.doSomething();
}
```

</tip-box>

Limiting the interaction to a closely related group of classes aims to reduce coupling. In the example able, `foo` is already coupled to `Bar`. Upholding LoD avoids `foo` being coupled to `Goo`.

An analogy for LoD can be drawn from Facebook. If Facebook followed LoD, you would not be allowed to see posts of friends of friends, unless they are your friends as well. If Jake is your friend and Adam is Jake’s friend, you should not be allowed to see Adam’s posts unless Adam is a friend of yours as well.

</div>

<div id="extras">

<include src="exercises.md" />

</div>

</div>
