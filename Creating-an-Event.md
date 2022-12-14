# On a Downloaded Build
The easiest way to do this is by editing my [Example Event script](https://cdn.discordapp.com/attachments/840678333602857040/888568125413552168/CustomEvent.zip), extract the files inside `mods/custom_events/`
_______________________
# On the Source Code
## Adding it to Chart Editor
**1.** Open ChartingState.hx and around Line 50 you will see the `eventStuff` array.

![](https://user-images.githubusercontent.com/44785097/127798468-47d51a1c-ce0c-4d89-9ad9-405cf5f7254f.png)

**2.** Add your new Event's name and description to it.
_________________________

## Coding your event
**1.** Open PlayState.hx

**2.** Search for the function named `triggerEventNote`, add a new case using your event's name and code your event's action there.

![](https://user-images.githubusercontent.com/44785097/127798675-d56631da-6fb6-4926-b267-9f5f81ba4d91.png)
_________________________

## Early Trigger
Some events like "Kill Henchmen" are triggered earlier than their chart position (280ms earlier).
If you want to do something similar, search for the function `eventNoteEarlyTrigger` and set a new case with your event's name and how many milliseconds earlier should it be triggered.