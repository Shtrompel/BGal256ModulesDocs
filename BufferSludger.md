## Buffer Sludger

### Overview


<img src="https://github.com/Shtrompel/BGal256ModulesDocs/blob/main/BufferSludger.png?raw=true" style="width:50%;">

Buffer Sludger is a real-time audio buffer recorder and playback module supporting mono or stereo signals. It offers two **Playback Modes**:

* **Direct**: Automation CV sets the exact playback position in the buffer.
* **Wrap**: The loop plays continuously at the set tempo, and the automation CV adds a phase offset on top of the running loop.

The module has an internal clock that is used for controlling the playback speed of the sample. The sample duration (in seconds) is displayed at the top of the waveform display screen (**1**).

## Inputs

| No. | Input             | Description                                 | Signal Type |
| --- | ----------------- | ------------------------------------------- | ----------- |
| 2   | Clock Step        | Receives external clock triggers            | Trigger     |
| 3   | Clock Reset       | Manually reset the internal clock timing         | Trigger     |
| 4   | Clock Phase       | Continuous phase CV (alternative to step)   | 0–10 CV     |
| 5   | Clear Buffer      | Clears all recorded samples in the buffer   | Trigger     |
| 6   | Automation        | Controls playback position or offset (Wrap) | 0–10 CV     |
| 7   | Dry/Wet           | Modulates the dry/wet mix parameter         | 0–10 CV     |
| 8   | Audio Left Input  | Mono or left-channel audio recording input  | ±5 CV       |
| 9   | Audio Right Input | Right-channel audio recording input         | ±5 CV       |

## Outputs

| No. | Output             | Description                              | Signal Type |
| --- | ------------------ | ---------------------------------------- | ----------- |
| 10  | Audio Left Output  | Buffered playback (mono or left channel) | ±5 V CV     |
| 11  | Audio Right Output | Buffered playback (right channel)          | ±5 V CV     |

## Knobs & Switches

| No. | Control        | Description                                            | Range             |
| --- | -------------- | ------------------------------------------------------ | ----------------- |
| 12  | BPM            | Sets internal clock tempo                              | 1–400 BPM         |
| 13  | External Clock | Toggles between internal BPM and external clock inputs | Switch |
| 14  | Playback Mode  | Select **Direct** or **Wrap** mode (see Overview)      | Switch     |
| 15  | Dry/Wet Mix    | Blends original buffer (dry) with playback (wet)       | 0.0–1.0           |

## Context Menu Options

<img src="https://github.com/Shtrompel/BGal256ModulesDocs/blob/main/BufferSludgerContext.png?raw=true" style="width:25%;">

| No. | Option                            | Description                                                                                       |
| --- | --------------------------------- | ------------------------------------------------------------------------------------------------- |
| 16  | Load WAV File                     | Open file dialog to import a WAV into the buffer                                                  |
| 17  | Interpolation Mode                | Choose sample interpolation: None, Linear, Cubic, Optimal 2×/8×/32× (taken from https://yehar.com/blog/wp-content/uploads/2009/08/deip.pdf) |
| 18  | Disable Output Filter             | Turn off the low‑pass anti‑alias filter on playback                                               |
| 19  | Disable Anti-Click Filter         | Bypass crossfade smoothing on click detection                                                    |
| 20  | Enable Speed Change on BPM Change | Resample buffer on tempo change instead of adding silence of cutting of the sample                                  |
| 21  | Visual Mode                       | Select audio buffer display: rotating **Disk** mode, **Waveform** of the sample or **Disable** the view.                                     |
| 22  | UI Downsampling                   | Adjust the waveform draw resolution: lower values will increase the quality                                 |
