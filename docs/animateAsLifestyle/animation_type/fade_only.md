# FadeOnly

FadeOnly AnimationType:
```kotlin
AnimationType.FadeOnly(
    from: Float = 0f,
    to: Float = 1f,
    animationSpec: AnimationSpec<Float> = spring()
)
```
=== "Light"

    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fade-light.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
=== "Dark"
    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fade-dark.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>


## Specs
|Parameter       |Description             |Type    |Default value      |Allowed values      |
|----------------|------------------------|--------|-------------------|-----------|
|*from*          |Alpha when element is *not* visible|Float|0f|[0f; 1f]|
|*to*            |Alpha when element is visible|Float|1f|[0f; 1f]|
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
        visible, animationType = AnimationType.FadeOnly(
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
        <source src="fade-animateVisibility-light.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
=== "Dark"
    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fade-animateVisibility-dark.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>

### Custom *from* and *to*


=== "Light `from = 0.3f`"

    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fade-from-light.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
=== "Dark `from = 0.3f`"
    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fade-from-dark.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>


=== "Light `to = 0.7f`"

    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fade-to-light.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
=== "Dark `to = 0.7f`"
    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fade-to-dark.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>

### Custom *animationSpec*


=== "Light `tween(1000)`"

    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fade-spec-light.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
=== "Dark `tween(1000)`"
    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fade-spec-dark.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
