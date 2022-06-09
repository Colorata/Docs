# ScaleOnly

ScaleOnly AnimationType:
```kotlin
AnimationType.ScaleOnly(
    from: Float = 0f,
    to: Float = 1f,
    animationSpec: AnimationSpec<Float> = spring()
)
```
=== "Light"

    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="scale-light.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
=== "Dark"
    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="scale-dark.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>


## Specs
|Parameter       |Description             |Type    |Default value      |Allowed values      |
|----------------|------------------------|--------|-------------------|-----------|
|*from*          |Scale when element is *not* visible|Float|0f|[0f; ∞)|
|*to*            |Scale when element is visible|Float|1f|[0f; ∞)|
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
        visible, animationType = AnimationType.ScaleOnly(
            /*
            from = 0f,
            to = 1f,
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
        <source src="scale-animateVisibility-light.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
=== "Dark"
    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="scale-animateVisibility-dark.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>

### Custom *from* and *to*

=== "Light `from = 0.3f`"

    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="scale-from-light.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
=== "Dark `from = 0.3f`"
    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="scale-from-dark.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>


=== "Light `to = 0.5f`"

    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="scale-to-light.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
=== "Dark `to = 0.5f`"
    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="scale-to-dark.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>

### Custom *animationSpec*

=== "Light `spring(0.2f)`"

    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="scale-spec-light.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
=== "Dark `spring(0.2f)`"
    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="scale-spec-dark.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
