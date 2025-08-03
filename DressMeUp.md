## Dress Me Up

### Overview


<img src="https://github.com/Shtrompel/BGal256ModulesDocs/blob/main/DressMeUp.png?raw=true" style="width:50%;">

Dress me up is a programmable 4 step sequencer with an interactive dressing game where each step is represented by piece of clothing (categorized into 4 types: hair, shirt, pants and shoes).
In the UI at **(1)** you can drag and drop clothes on onto or frame the model on the left. The current piece of clothing for the current step will be highlighted, and each time the step changes, the next clothing item will be highlighted and selected.
The output value is depended on the currently worn piece of clothing.


## Inputs


| No. | Option | Description  |
| --- | --------------------------------- | ------------------------------------------------------------------------------------------------- |
| 2   | Reset        | Reset the step position to 1.            | Trigger     |
| 3   | Prev       | Go to the previous step        | Trigger     |
| 4   | Step       | Advance to the next step   | Trigger     |
| 5   | Step/CV      | Control the current step using a CV input.    | Range depends on **(12)** |
| 6   | Value A/B/C/D        | Control the value of each of the 4 steps. |  Range depends on **(14)**  |
| 7   | Current Value           | Control the value of the current step.         |  Range depends on  **(14)**  |

## Outputs

| No. | Output             | Description                              | Signal Type |
| --- | ------------------ | ---------------------------------------- | ----------- |
| 8  | Out  | Output the value of the current step. When output filter is enabled through the context menu negative values will also be outputted. | ±10 V     |
| 9  | Step | If the current step was changed, and there is a cloth currently worn, this output jack will output a trigger.          | Trigger     |
| 10  | Sum | The raw sum of all 4 steps.          | 0-40 V     |

## Knobs & Switches

| No. | Control        | Description                                            | Range             |
| --- | -------------- | ------------------------------------------------------ | ----------------- |
| 11  | Steps Len            | Change the step count of the sequencer.                              | 1-4 steps         |
| 12  | Step/CV Range | The expected input range or the Step/CV  | Switch |
| 13  | Smooth Step  | Instead of snapping to the nearest step, enable a smooth transition between the steps.      | Switch     |
| 14  | Value/CV Range | The expected input range or the Value/CV  | Switch |
| 15  | Quantize Value  | Instead of outputting the value of the cloth for each step, output the stored value that was inputted from the Value/CV inputs. | Switch     |
| 16  | Output Range  | Multiply the output by the value of the knob. | 0 - 10 |

## Context Menu Options

<img src="https://github.com/Shtrompel/BGal256ModulesDocs/blob/main/DressMeUpContext.png?raw=true" style="width:25%;">

| No. | Option | Description  |
| --- | --------------------------------- | ------------------------------------------------------------------------------------------------- |
| 17  | Shader Parameters  | Customise the lcd screen shader. |
| 18  | Disable Shader | Disable the lcd screen shader. |
| 19  | Enable Output Filter | If the module is used as an effect or mixer, you can enable a high-pass filter in order to normalize the waveform. |

