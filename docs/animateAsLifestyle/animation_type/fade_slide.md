# FadeAndSlide

FadeAndSlide AnimationType:
```kotlin
AnimationType.FadeAndSlide(
    fromAlpha: Float = 0f,
    toAlpha: Float = 1f,
    fromOffset: Float = 100f,
    toOffset: Float = 0f,
    animationSpec: AnimationSpec<Float> = spring(),
    slideDirection: SlideDirection = SlideDirection.Vertical
)
```
=== "Light"

    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fadeslide-light.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
=== "Dark"
    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fadeslide-dark.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>


## Specs
|Parameter       |Description             |Type    |Default value      |Allowed values      |
|----------------|------------------------|--------|-------------------|-----------|
|*fromAlpha*          |Alpha when element is *not* visible|Float|0f|[0f; 1f]|
|*toAlpha*            |Alpha when element is visible|Float|1f|[0f; 1f]|
|*fromOffset*          |Offset when element is *not* visible|Float|0f|(∞; ∞)|
|*toOffset*            |Offset when element is visible|Float|1f|(∞; ∞)|
|*animationSpec* |General animationSpec for animation|AnimationSpec<Float\>|spring()|-|
|*slideDirection*|Direction of animation|SlideDirection|Vertical|Vertical, Horizontal|


## Samples

With [AnimateVisibility](../animate_visibility.md):
```kotlin
var visible by remember { mutableStateOf(false) }
LaunchedEffect(Unit) {
    visible = true
    delay(2000)
    visible = false
}
Button(
    onClick = {  }, modifier = Modifier.animateVisibility(
        visible, animationType = AnimationType.FadeAndSlide(
            /*
            fromAlpha = 0f,
            toAlpha = 1f,
            fromOffset = 100f,
            toOffset = 0f,
            animationSpec = spring(),
            slideDirection = SlideDirection.Vertical
            */
        )
    )
) {
    Text(text = "Send")
}
```

=== "Light"

    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fadeslide-animateVisibility-light.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
=== "Dark"
    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fadeslide-animateVisibility-dark.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>

### Custom *fromOffset* and *slideDirection*

=== "Light `300f vertical`"

    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fadeslide-fromplus-light.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
=== "Dark `300f vertical`"
    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fadeslide-fromplus-dark.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
    
    
=== "Light `-300f vertical`"

    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fadeslide-fromminus-light.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
=== "Dark `-300f vertical`"
    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fadeslide-fromminus-dark.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>

=== "Light `300f horizontal`"

    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fadeslide-fromplushorizontal-light.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
=== "Dark `300f horizontal`"
    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fadeslide-fromplushorizontal-dark.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
    
    
=== "Light `-300f horizontal`"

    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fadeslide-fromminushorizontal-light.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
=== "Dark `-300f horizontal`"
    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fadeslide-fromminushorizontal-dark.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>

### Custom *toAlpha* and *fromAlpha*

=== "Light `to = 0.7f`"

    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fadeslide-toalpha-light.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
=== "Dark `to = 0.7f`"
    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fadeslide-toalpha-dark.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>

=== "Light `from = 0.3f`"

    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fadeslide-fromalpha-light.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
=== "Dark `from = 0.3f`"
    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fadeslide-fromalpha-dark.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>

### Custom *animationSpec*

=== "Light `tween(1000, easing = LinearEasing)`"

    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fadeslide-spec-light.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
=== "Dark `tween(1000, easing = LinearEasing)`"
    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fadeslide-spec-dark.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
