AdaptivePA
==========

Code for an adaptive physical activity intervention

These are currently run when the user has pressed 'Save Response' on
the experiment input form in the app. They override the current
"Feedback" screen with custom output that can take advantage of the
data that has been collected in the experiment.

Simple example 1:
Giving custom feedback based on average response value for the last n responses
This example has an experimental form that collects a variable called
"alertness" that has a value scaled from 1 to 5. If the user is
reporting high alertness over the last 3 responses it gives them
kudos. If they are reporting an average low response it tries to be
uplifting. Otherwise, if they are in the middle of the scale, it gives
a general affirmative response. This is of course, just an example
:-). You can paste this into the custom feedback portion of an
experiment, (be sure to check the custom feedback checkbox to turn it
on).

I would start with the "main" function at the bottom to see the flow
of execution. The next most interesting function for you (I think) is
the "computeResponse" function, which is called from the main
function. It takes the average response and decides what message to
show the user. The other function perhaps of interest is

Example 2: Output that sums up and weights responses.
This example was used by the author of the Discover article on Paco.
It asks about incidence of sneezing attacks after eating. It then
shows a chart with the foods eaten when sneezing was reported with a
weighted score based on frequency and intensity of sneezing.

