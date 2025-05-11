## Dress Me Up

### Overview


<img src="https://github.com/Shtrompel/BGal256ModulesDocs/blob/main/DressMeUp.png?raw=true" style="width:50%;">

Dress me up is a programmable 4 step sequencer with an interactable dressing game where each cloth is categorized into 4 types of clothes, each representing a step. And each cloth of the in the same cloth type represents the value of the step.

In the UI at **(1)** you can drag and drop clothes on or from the model, the current step will highlight the current worn cloth of the equivalent clothing type.


## Inputs

| No. | Input             | Description                                 | Signal Type |
| --- | ----------------- | ------------------------------------------- | ----------- |
| 2   | Reset        | Reset the step position to 1.            | Trigger     |
| 3   | Prev       | Go the the previous step        | Trigger     |
| 4   | Step       | Advance to the next step   | Trigger     |
| 5   | Step/CV      | Controll the current step using a cv input.    | Range depends on **(12)** |
| 6   | Value A/B/C/D        | Controll the value of every of the 4 steps. |  Range depends on **(14)**  |
| 7   | Current Value           | Controll the value of the current step.         |  Range depends on  **(14)**  |

## Outputs

| No. | Output             | Description                              | Signal Type |
| --- | ------------------ | ---------------------------------------- | ----------- |
| 8  | Out  | Output the value of the current step. When output filter is enabled through the context menu negative values will also be outputted. | ±10 V     |
| 9  | Step | If the current step was changed, and there is a cloth currenly worn this output jack will output a trigger.          | Trigger     |
| 10  | Sum | The raw sum of all 4 steps.          | 0-40 V     |

## Knobs & Switches

| No. | Control        | Description                                            | Range             |
| --- | -------------- | ------------------------------------------------------ | ----------------- |
| 11  | Steps Len            | Change the step count of the sequencer.                              | 1-4 Steps         |
| 12  | Step/CV Range | The expected input range or the Step/CV  | Switch |
| 13  | Smooth Step  | Instead of snapping to the nearest step, enable smooth transition between the steps.      | Switch     |
| 14  | Value/CV Range | The expected input range or the Value/CV  | Switch |
| 15  | Quantize Value  | Instead of outputing the value of the cloth for each step, output the stored value that was inputted from the Value/CV inputs. | Switch     |
| 16  | Output Range  | Multiply the output by the value of the knob. | 0 - 10 |

## Context Menu Options

<img src="https://github.com/Shtrompel/BGal256ModulesDocs/blob/main/DressMeUpContext.png?raw=true" style="width:25%;">

| No. | Option | Description  |
| --- | --------------------------------- | ------------------------------------------------------------------------------------------------- |
| 17  | Shader Parameters  | Customise the lcd screen shader. |
| 18  | Disable Shader | Disable the lcd screen shader. |
| 19  | Enable Output Filter | If the module is used as a effect or mixer, you can enable a high pass filter in order to normalize the waveform.|
