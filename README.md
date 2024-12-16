# Twinkly

Twinkly LEDs are magical smart Christmas light bulbs which transform your Christmas tree into something addictive.

I wrote this repo as the Twinkly app has become so unstable it requires often a un/reinstallation which has the awkward effect
that all custom made effects are lost. As most Twinkly effects are easily describable via some sort of YAML structure, this makes
it very easy to define the that way, so recreation of your effects become somehow easier.

Very sad that export/import of Twinkly effects is not (yet) possible via the app.  One only can hope...

You'll find 2 files in this repo at this moment:

* twinkly_custom_effects.yaml: the main file with the description of each of my custom effects
* devices.yaml: all my Twinkly devices with their corresponding playlist

## Effects preview
<img src=./images/twinkly_effects.png>

## Effects file layout
The effects file describe per effect:
* the defined layers with their respective parameters
* the mix defined on the previous 2 layers

So let's say you have an effect defined consisting of 2 layers.  Then to recreate this on your Twinkly app, you just defined the layers chronologically as in the file, together with their defined colors and parameters.

## Colors
I defined the used colors somehow liberally.  Unfortunately, there's no means in the app to easily get the hex code of a used color. As such, I've simply chosen to call the name of the color as I see it.  It remains as a todo to convert these color names to a fixed color nomenclature defined somewhere.

## Parameters
In the effects definition, you'll find a section per defined layer:

| Parameter               | Description                                                                                                                                                                                        |
| ----------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Type                    | The type of effect, like sparkle, gradient, stripes, ...                                                                                                                                           |
| Zoom, angle, speed, ... | Some parameter per effect.  They represent the percentage set of a full slider line, so 100 means the slider has been set completely to the right. 50 means the slider has been set in the middle. |
| Mix                     | The mix effect applied to the previous two layers                                                                                                                                                  |

