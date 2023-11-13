# Piano Floor Example Scene SDK7 (Unknower's Remix)

A piano floor where the player walks on the keys to play.

![demo](https://github.com/decentraland-scenes/piano-floor-example-scene/blob/master/screenshots/piano-floor.gif)

This scene shows you:
- How to play sounds from files
- How to change the material of a primitive shape
- How to use the trigger area from the Utils library to activate something when a player walks over it
- How to keey players synced by using the messagebus to communicate each player's actions to others
- How to use the pitch value of audioclips to create different musical notes

## Try it out

**Previewing the scene**

1. Download this repository.

2. Install the [Decentraland Editor](https://docs.decentraland.org/creator/development-guide/sdk7/editor/)

3. Open a Visual Studio Code window on this scene's root folder. Not on the root folder of the whole repo, but instead on this sub-folder that belongs to the scene.

4. Open the Decentraland Editor tab, and press **Run Scene**

Alternatively, you can use the command line. Inside this scene root directory run:

```
npm run start
```

## Scene Usage

Step on the keys to activate each note. 

If there are multiple players in the scene, they should all hear what each other plays. You can simulate this by opening two browser windows with the same preview. 

Learn more about how to build your own scenes in the Decentraland [documentation](https://docs.decentraland.org/) site.

If something doesn't work, please [create a pull request](https://github.com/decentraland/sdk7-goerli-plaza/pulls). 

## Code Overview

### 'pianoKey.ts'

- **BlackPianoKey Class**: Represents a black piano key, managing its properties like shape, colour and triggers.
- **WhitePianoKey Class**: Represents a white piano key, similar to the black key.

### 'index.ts'

Sets up the scene, creating black and white keys and handling audio.

### 'sceneBus.ts'

Sets up the scene's multiplayer message bus and event handling

## Customisation Guide

### Adding More Notes

Add additional key objects to the resources.ts file

Each key can have its own position and scale set in its cooresponding object.

You can define a specific file for each key and shift the pitch by a certain number of semitones. Set pitch to 0 to play the sound file without pitch shifting.

## Copyright Info

This scene is protected with a standard Apache 2 license.
