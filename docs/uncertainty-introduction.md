# Uncertainty Introduction


- [Overview](#overview)
- [Sources of Uncertainty](#sources-of-uncertainty)
    - [Resolution Uncertainty](#resolution-uncertainty)
    - [Random Uncertainty](#resolution-uncertainty)
    - [Systematic Uncertainty](#resolution-uncertainty)
- [Combining Uncertainties](Combining-Uncertainties)
- [Propagation of Uncertainties](propagation-of-uncertainties)


## Overview

One of our goals as experimental scientists is to try to minimize the uncertainty when we perform a measurement. We can of course increase our confidence in our measurement by collecting as much data as possible, although we must decide when we have reached a point of “diminishing returns.” We must be aware of how much variance there is in our data and how to quantify that variance. We want to be aware of what factors in our experiment are introducing the most significant uncertainty and determine if there is some way we can improve our experimental design within our laboratory constraints. During an experiment you will need to ask yourself what factors could influence the result of your measurement. Each of these factors can be thought of as working against our having perfect knowledge about a “measurand” (the quantity we want to measure) and adding to the overall uncertainty. A crucial aspect of experimentation is to identify the most important sources of uncertainty and to numerically estimate their effect on your measurement result.

Common sources of uncertainty include:

– your judgement in reading analogue instruments;
– the sensitivity of your instruments (e.g. the digital scale, smallest interval on a meter stick, etc.);
– the rating or stated calibration of the instrument;
– approximations and assumptions that you make while doing the experiment;
– variations in repeated readings made under apparently identical conditions; and
– the effects of environmental conditions on the measurement.

A measurement uncertainty is not meant to be an indication of “mistakes” that you might make in an experiment. If you are aware that you have made a mistake, then you should repeat your experiment or at least exclude the data taken improperly. Similarly, “human error” is not a useful way of identifying a source of uncertainty; that phrase provides future experimenters with no guidance at all about what aspects of the experimental apparatus or procedures to focus on improving.

## Sources of Uncertainty
There are many sources of uncertainty in your experiment, but not all originate in the same manner and therefore there are different methods of accounting for them.  When designing an experiment the aim is to make the uncertainty small enough to achieve the experiment’s goal — or often, to make the uncertainty as small as possible in order to observe as much detail as possible about the phenomenon.  However, always keep in mind that the uncertainty can never be reduced to zero, just made small and honestly estimated.



### Resolution Uncertainty
Imagine you are attempting to measure the length of an object using the meter stick shown at the right. The length of the object is more than 80 cm but it is less than 90 cm but we are clearly limited by the resolution of our measuring device:
![meter stick zoomed out](/images/meter-stick-1.png)

We now get a better measuring device that has graduations down to the cm. We can now say that the length of the object is between 83 and 84 cm, although it appears to be closer to the 83 cm mark. Again, the accuracy of our measurement is limited by the markings on the meter stick:
![meter stick zoomed in a litte](/images/meter-stick-2.png)

Finally, we obtain a measurement device that can measure much smaller intervals than our previous devices, surely we can now know the “exact” length of our object, right? As we see when we zoom in our measurement still could be improved by increasing the resolution of our measurement device!!
![image of a meter stick zoomed in a lot](/images/meter-stick-3.png)

Apparently even with our super device there is a limit to the knowledge that the we can gain about the length of the object. All we can say is that the length of the object is between 83.4 and 83.5 cm. Even if we use smaller and smaller divisions on our meter stick our knowledge about the length of the object will never be perfect. This type of uncertainty is called the resolution uncertainty. A general rule of thumb is that the resolution is half of the smallest digit a device can measure, but it may be much greater than this if other known factors are limiting your uncertainty (perhaps you can’t get your ruler close enough to make an accurate measurement or can’t really tell where the object you are trying to measure begins or ends). Estimating uncertainties requires more than rules of thumb, it also requires judgement and common sense.

### Random Uncertainty
In the last module you took measurements of the rotation rate of a motor. If you attempted to repeat your rotation rate measurement of a particular motor you most likely saw some spread in your values (you did not get an identical rotation rate each time you spun a motor under “identical” conditions). There will be slight and uncontrollable differences from one trial to another. These uncontrollable differences generally arise from a huge variety of detailed causes. Maybe the air conditioning happens to blow a slight puff of air on your setup the first time. Maybe a speck of lint falls on the sanded portion of the motor and reduces the current flowing through the motor. But, however these differences arise, they cause different results when a single procedure is repeated several times. The differences don’t trend in any particular direction, and their causes are subtle and hard to identify, let alone control, in the lab – so we call them random. These variations in data cause a spread in your data, as shown in the two histograms of repeated measurements from experiments A and B below:

![Historgam of measurements from two experiments](/images/PDF-random-uncertainty.png)
*Histogram of length measurements of a single object for two different experiments, A and B. What can you say about the difference in your confidence between the results of Experiment A and B?  (Area = 0.68 indicates in each case that the shaded area contains 68% of the total trials.)*


Clearly, Experiment B has a narrower spread in the data and therefore has a lower uncertainty, but how do we calculate this uncertainty? It seems reasonable that the result of your multiple measurement trials would be the mean value ± some uncertainty that is related to the spread in your data. The range in which 68% of your measurements reside is the mean ±σ where σ is the standard deviation of the data. However, taking more data will likely not decrease the value of the standard deviation of your data but it will surely increase your confidence in the mean and therefore should decrease the uncertainty. Therefore, the uncertainty we report will be $$\pm \sqrt{\sigma/N}$$, known as the standard error, where N is the number of trials (data points taken under “identical” experimental conditions).

Tip: Google Sheets can calculate the standard deviation of your data for you by using the function STDEV().  You can read more on this [here](https://support.google.com/docs/answer/3094054?hl=en).

Lesson check: If you take several trials of a particular measurement and record an identical value every time, does this mean you know the exact value with no uncertainty? What does this say about your experimental procedure?

### Systematic errors
A group from another table in your section uses the exact same equipment and setup as you (i.e. same motor, oscilloscope, etc) to measure the rotation rate of the motor. They design their own, independent procedure to measure this quantity. The two groups can have differing results not only because of random uncertainty but also because of systematic error.

Systematic error arises when your experimental procedure and/or apparatus somehow cause all your measurements to be shifted away from the true value of the quantity you set out to measure. A systematic error happens in the same direction and the same (or similar) size in all your data, so its effect only shows up when an alternate measurement procedure is compared to yours.

For example, if you measure the length of an object with a meter stick that is 1.1 m rather than 1 m long (i.e. the spacing between mm marks is 10% too large) then all of your length measurements will be larger than those measured with a calibrated meter stick. Systematic errors are biases in the experimental process that need to be considered separately from resolution error and random uncertainty.  One good way to identify systematic error is to try several methods of collecting the same data.  If they should produce equal results (within resolution and random errors) but are consistently shifted from each other, then at least one method has a systematic error.  Another hint that you have a systematic error is to analyze your data for an expected shape or pattern.  If the basic pattern is what theory predicts but there is an offset, either the theory applies poorly to reality or you have a systematic error.  The best scenario is that you identify the source of systematic error and eliminate it from your process.  If that doesn’t happen, at least the size of systematic error can be estimated from careful checks like these.

Lesson check: what sources of systematic error could have been present in your experiment from the first module? How could you have tested this?

### Combining Uncertainties
When you make a measurement you will have both random and resolution (sometimes multiple!) uncertainties. In order to obtain one actual uncertainty to quote in your value you can combine the sources by adding in quadrature. Adding in quadrature means to square each value for your uncertainty, add them all together, and take the square root of the sum:

$$ \delta x_\mathrm{total} = \sqrt{\delta x_1^2 + \delta x_2^2 \delta x_3^2 ...}$$

Where $$\delta x_\mathrm{total}$$ is the total uncertainty in the measured value $$x$$ and $$\delta x_1$$,$$\delta x_2$$,$$\delta x_3$$,… are the various sources of uncertainty in the measurement of $$x$$ (e.g. random uncertainty, resolution uncertainty, etc).

Remember: Systematic errors should be dealt with separately, by eliminating all you possibly can and estimating the size of remaining shifts, in addition to pinpointing the specific effect they would have on the final analysis.  (Would they make the speed of sound come out too high?  Would they make a linear graph look quadratic?  etc.)

## Propagation of Uncertainties
Suppose you have a function $$g$$ that is a function of the quantities $$x$$, $$y$$ and $$z$$, i.e. $$g(x, y, z)$$. The uncertainty in $$g$$ in terms of the uncertainties in $$x$$, $$y$$ and $$z$$ is found by:

$$\delta g = \sqrt{ (\delta x \frac{\partial g}{\partial x})^2 + (\delta y \frac{\partial g}{\partial y})^2 + (\delta z \frac{\partial g}{\partial z})^2} $$

Where $$\delta x$$ is the uncertainty in $$x$$ and $$\frac{\partial g}{\partial x}$$  is the partial derivative of $$g$$ with respect to $$x$$ (similar for $$y$$ and $$z$$).

To see the origins of this relationship I encourage you to read the following document, [An Introduction to Experimental Uncertainties and Error Analysis](https://www.physics.hmc.edu/~physics50/wp/wp-content/uploads/2018/08/intro_to_uncert_ph22.pdf), created for HMC physics labs of the past. This is a great document that explains calculating uncertainties (how and why), when you can throw out data, and how to propagate uncertainty measurements in one value into uncertainties in another value. The entire document is beneficial (with the exception of 17-19 as we are not using this during Ph 50), but I encourage you to read pages 15-16 and 21-22 with particular attention. 

Try it:
The radius of a circle is measured to be $$2.4 \pm 0.3 \textrm{cm}$$. What is the area of the circle?

<details>
<summary markdown='span'> (try it first, then click to expand/collapse) Solution: </summary>

The area of the circle is $$ A = \pi r^2=\pi (2.4 \textrm{cm})^2= 18.0864 \textrm{cm}^2$$. But what is the uncertainty?

$$ \delta A = {\delta r}\frac {\partial A}{\partial r} = {\delta r}(2\pi r)=(0.3 \textrm{cm})(2 \pi)(2.4 \textrm{cm}) = 4.5216 \textrm{cm}^2$$

Therefore $$ A=(18 \pm 5) \textrm{cm}^2$$

</details>

-----------

Let’s try another one:
If we now have a cone, with the same radius $$r=2.4 \pm0.3\textrm{cm}$$ and a height $$h=10.2\pm0.4\textrm{cm}$$, what is the volume of the cone? (Hint: $$V_\mathrm{cone}=\frac{1}{3}\pi r^2 h$$)

<details>
<summary markdown='span'> (try it first, then click to expand/collapse) Solution: </summary>

The volume of the cone is \( V_\mathrm{cone}=\frac{1}{3} \pi r^2 h= 61.49376 \textrm{cm}^3 \). But what is the uncertainty?

$$ \delta V_\mathrm{cone} = \sqrt{({\delta r}\frac {\partial V_{cone}}{\partial r})^2 +({\delta h}\frac {\partial V_{cone}}{\partial h})^2 }$$

$$ = \sqrt{({\delta r} * \frac{1}{3} 2\pi r h)^2+({\delta h} * \frac{1}{3} \pi r^2)^2}$$
$$ =\sqrt{(15.37344 cm^3)^2+ (2.41152 cm^3)^2}= 15.56 \textrm{cm}^3 $$

Therefore \( V_\mathrm{cone}=(61 \pm 16) \textrm{cm}^3 \).


Bonus: What measurement’s uncertainty was dominant in our uncertainty in the volume of the cone, \(r\) or \(h\)? 

<details>
<summary markdown='span'> (try it first, then click to expand/collapse) Solution: </summary>

Since the uncertainty in the volume of the cone due to the uncertainty in the radius is much larger than that from the height ( \(15.5 \textrm{cm}^3>>2.41 \textrm{cm}^3\) ) we should refine our experimental procedure to be much more careful and precise in our radius measurement since this is limiting our knowledge of the cone's volume.

</details>
 
 ----------

</details>

-----------

