# FadeAndScale

FadeAndScale AnimationType:
```kotlin
AnimationType.FadeAndScale(
    fromAlpha: Float = 0f,
    toAlpha: Float = 1f,
    fromScale: Float = 0f,
    toScale: Float = 1f,
    animationSpec: AnimationSpec<Float> = spring()
)
```
=== "Light"

    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fadescale-light.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
=== "Dark"
    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fadescale-dark.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>


## Specs
|Parameter       |Description             |Type    |Default value      |Allowed values      |
|----------------|------------------------|--------|-------------------|-----------|
|*fromAlpha*          |Alpha when element is *not* visible|Float|0f|[0f; 1f]|
|*toAlpha*            |Alpha when element is visible|Float|1f|[0f; 1f]|
|*fromScale*          |Scale when element is *not* visible|Float|0f|[0f; ∞)|
|*toScale*            |Scale when element is visible|Float|1f|[0f; ∞)|
|*animationSpec* |General animationSpec for animation|AnimationSpec<Float\>|spring()|-|


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
        visible, animationType = AnimationType.FadeAndScale(
            /*
            fromAlpha = 0f,
            toAlpha = 1f,
            fromScale = 0f,
            toScale = 1f,
            animationSpec = spring()
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
        <source src="fadescale-animateVisibility-light.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
=== "Dark"
    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fadescale-animateVisibility-dark.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>

### Custom *alpha* and *scale*


=== "Light `fromAlpha = 0.3f, fromScale = 0.3f`"

    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fadescale-from-light.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
=== "Dark `fromAlpha = 0.3f, fromScale = 0.3f`"
    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fadescale-from-dark.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>


=== "Light `toAlpha = 0.5f, toScale = 0.5f`"

    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fadescale-to-light.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
=== "Dark `toAlpha = 0.5f, toScale = 0.5f`"
    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fadescale-to-dark.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>

### Custom *animationSpec*


=== "Light `spring(0.2f)`"

    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fadescale-spec-light.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
=== "Dark `spring(0.2f)`"
    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fadescale-spec-dark.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
