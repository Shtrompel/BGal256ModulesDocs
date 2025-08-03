## Buffer Sludger Transposer

### Overview


<img src="https://github.com/Shtrompel/BGal256ModulesDocs/blob/main/BufferSludgerTransposer.png?raw=true" style="width:12.5%;">

Buffer Sludger Transposer is an expander module for [Buffer Sludger](https://github.com/Shtrompel/BGal256ModulesDocs/blob/main/BufferSludger.md) that acts as an additional automation input that is added on top of the existing automation input. Meaning the actual automation is the sum of the automation input jack with the automation value that from this module.
Assuming no additional automation is connected to the Buffer Sludger, this module will change the playback speed of the audio in correlation to the pitch (additional automation may also affect the pitch change).

## Inputs

| No. | Input             | Description                                 | Signal Type |
| --- | ----------------- | ------------------------------------------- | ----------- |
| 1   | Reverse Control       | When connected it will override the value of **(3)** reverse switch. When the input is higher than 5V, the playback of the audio is played in reverse.            | 0-10 CV     |
| 2   | V/OCT       | Changes the playback speed relative to the value of the input pitch. That means that if the audio in the buffer is in a C4 pitch, the resulting playback pitch will be equal to the input value. For example a value of -1 will play the audio at half speed.         | -10 - 10 CV     |

## Knobs & Switches

| No. | Control        | Description                                            | Range             |
| --- | -------------- | ------------------------------------------------------ | ----------------- |
| 3  | Reverse Switch            | The value is overridden when **(1)** is connected. When enabled, the playback of the audio buffer is reversed.                              | Disabled/Enabled         |
| 4  | Reset Switch | Controls the behaviour when a change in pitch is detected. The default **Add** mode will continue playing the buffer from the same place the last pitch ended in. **Reset** will reset the playback position to the start on every pitch change. | Add/Reset |

## Lights

| No. | Option                            | Description                                                                                       |
| --- | --------------------------------- | ------------------------------------------------------------------------------------------------- |
| 5  | Connected                    | Lights up if a [Buffer Sludger](https://github.com/Shtrompel/BGal256ModulesDocs/blob/main/BufferSludger.md) module is detected.                                                  |
| 6  | Reverse Mode                | Lights up if reverse mode is enabled. |
