# Behavioral web experiment with jsPsych hosted on Pavlovia

This repository may be helpful if you are working with [jsPsych](https://www.jspsych.org/) to build behavioral experiments and want to deploy them via [Pavlovia](https://pavlovia.org/) or an alternative web server.

## About the experimental task
The experimental script I showcase here implements a behavioral response time experiment I designed for a study investigating people's propensity to imitate the actions they observe in others. If you are curious about the theoretical background and findings of the study, 
have a look at the [published research paper](https://journalofcognition.org/articles/10.5334/joc.483). In the experiment, participants play a simple card game together with a virtual partner (i.e., the computer). Participants' task is to select one of two playing cards 
with different numerical values in response to observing their partner selecting one of two playing cards themselves. In the experiment, we manipulated whether participants' card selection required them to imitate or to counter-imitate the selection of their partner, 
and measured effects of our experimental manipulations on participants' response performance (whether they select the correct card and how fast they do so). 
You can [work through the task yourself by clicking on this link](https://run.pavlovia.org/MaxMarschner/cardgameimitationmatchsidebyside). 

## Files in this repository
- `index.html` --> main experimental script controlling experimental procedure, stimuli presentation, response recording, and communication with the Pavlovia web server
- `imitation_trials_blocked_info.js` --> Contains an array defining experimental variables of all trials in the experiment. Important for randomization and counterbalancing of experimental variables.
- `Stimuli` --> folder containing images of the playing cards and background
- `jspsych-7-pavlovia-2021.12` --> jsPsych plugin that handles communication with the Pavlovia web-server. Not written by me, but by people from the Pavlovia cosmos. See [documentation for the plugin here.](https://gitlab.pavlovia.org/shir/jsPsych_SimpleReactionTime/-/tree/5482642e23223b5b24417992a460f36f73824a09) 
- `consentForm.html` --> html file that displays general study information and asks for informed consent.

## What to do with this repository
If you want to deploy the experiment as it is, download all files to your computer and push them to your Pavlovia GitLab repository. See [this documentation for details](https://pavlovia.org/docs/experiments/create-jsPsych).
You are also welcome to use code snippets from `index.html` for your own projects. E.g., the script is useful if you want to display multiple image and text stimuli simultaneously in a grid. It also provides working examples
for creating custom sampling functions for randomized stimulus presentation and for handling conditional timelines in jsPsych. 

## Additional resources for jsPsych x Pavlovia integration if you are recruiting online participants 
If you are running into trouble redirecting participants back to Prolific or alternative recruiting platforms after they completed the study, check the following online discussions for guidance:
- description and discussion of common problems: https://github.com/jspsych/jsPsych/discussions/2686
- suggested solution by Jonathan Kominsky: https://discourse.psychopy.org/t/how-to-redirect-to-prolific-after-completing-a-jspsych-experiment-on-pavlovia/43063

 

