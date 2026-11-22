# CEPAK: Parkinson's Disease Control
CEPAK is a web app for keeping a detailed day-to-day record of a person with Parkinson's disease: 
what medication they take and 
when, how they feel at each moment, 
what symptoms appear and, 
if they have a neurostimulator, 
how deep brain stimulation is working.
With that data, the app draws a graph of the day, estimates how the medication is working, and prepares summaries and reports to take to the neurologist appointment.
## What can be logged?
How they are now: marked OFF, mild OFF, partial ON or full ON, with the current time or an earlier one.
Medication doses: Sinemet Plus and Sinemet Retard (half a tablet or one), Xadago (safinamide) and the Neupro patch (rotigotine).
The time of each dose can be changed and upcoming doses can be planned.
Dyskinesia: mild, moderate or high, and the moment it ends.
Symptoms: numb arm, feeling hot, restlessness, dizziness, tiredness or low mood.
Stimulation effects: tingling, muscle pulling, slurred speech, double vision, freezing when walking, instability, fall, discomfort at the implant site or mood change.
Sleep: when they go to bed and when they get up.Meals: start and end time. 
The app calculates how digestion affects each dose.
### The day graph
This is the main screen. 
It shows on the same time axis:the estimated effect of the medication throughout the day,
the tablets taken (and the planned ones, in a lighter shade),
the actual state logged (ON, OFF, dyskinesia),
meals and their estimated digestion,
the expected ON/OFF state, 
with an uncertainty band.
You can view the whole day, the last 18 hours, twelve hours back and forward, or tomorrow.
#### Deep brain stimulation (DBS)
From what is logged, the app calculates:
time in ON and in OFF and its weekly evolution,
dyskinesia over recent days,
regularity of doses over the last two weeks,
the effect of meals and of protein close to a dose,
the duration of the effect according to the amount taken,
comparisons before and after each change of regimen,
recurring patterns and suggestions based on the latest records.
It also includes a simulator to see when it is best to take a tablet in relation to a meal.
##### A model that learns
The app starts from an initial model to estimate the medication effect and adjusts it with what is logged. 
It shows its real accuracy by comparing what was predicted with what was observed, day by day.

###### What CEPAK is not
CEPAK is not a medical device and does not replace the judgement of the medical team. 
The curves and analyses are estimates calculated from what each person logs, not measurements. 
Any decision about treatment belongs to the neurologist.

####### If you want to adapt it
The interface is in Spanish and the medication list is designed for Sinemet Plus and Retard, Xadago and the Neupro patch. 
To use it with another treatment, those sections in [index.html] would need to be modified. 
Instructions for connecting your own Firebase are in the README.
