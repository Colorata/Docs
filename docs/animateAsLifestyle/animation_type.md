# AnimationType

This is general class for defining animation types. 

## [FadeOnly](fade_only)
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
        <source src="fade_only/fade-light.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
=== "Dark"
    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fade_only/fade-dark.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>

## [ScaleOnly](scale_only)
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
        <source src="scale_only/scale-light.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
=== "Dark"
    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="scale_only/scale-dark.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>

## [FadeAndScale](fade_scale)
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
        <source src="fade_scale/fadescale-light.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
=== "Dark"
    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fade_scale/fadescale-dark.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>

## [FadeAndSlide](fade_slide)
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
        <source src="fade_slide/fadeslide-light.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
=== "Dark"
    <figure>
        <video width="400" controls="false" aria-hidden="true" loop class="video" autoplay>
        <source src="fade_slide/fadeslide-dark.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </figure>
