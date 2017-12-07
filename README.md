Go to [this link](https://gitpitch.com/hoj201/retreat_2017_presentation)

# Contents
- Where are we?
- Where should we go?
- How do we get there?

# Where are we?
 - We can semi-reliably detect bad lifts in a warehouse environment if it's worn on the correct side.
 - We can detect walking pretty well.
 - We can detect squat, but only if the squat generates a lift-window.


# Where should we go?
- We should know our ground truth
- Step counter
- ROI calculator
- We should get rid of Our caveates (e.g. "semi-reliable", "but only if ..", "correct side")

# How we get there?

## Ground truth
We need:
- a quick way to annotate data
- data to annotate

Therefore:
  - For annotation we will probably use [scale-api](https://www.scaleapi.com/)
  - For back-angle annotation we might use some [computer vision](https://www.youtube.com/watch?v=tKfkGttx0qs)
  - Data will be gathered by myself and/or by an intern.

## Side detection
To try a quick-dirty side detector, we can rock-and-roll today.

To do it well we need:
- more data of walking
- Videos annotated with the location of the device.

## Step counter
We need:
- data of walking, with known step counts. (we have least 6-ish videos)
- to test the existing algorithm
- to write a new algorithm if the existing one doesn't cut it.

## ROI calculator
We need:
 - An accurate estimate of back-angle
 - A squat estimator that works independently of lift-windows.

## Other stuff
It's hard to plan ahead until we get a ground truth (which is how things will be prioritized):

- Anomaly detection
- location detection
- More accurate back-angle calculations (it never buzzes for matt)
- A more useful coruscant-report
- replace kinetic-live with plotly
- a walk detector with less lag
- transition to using embedded tensorflow
