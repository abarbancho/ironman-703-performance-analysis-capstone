# Ironman 70.3 Performance Analysis
## Non-Technical Report

---

### What is this project about?

Ironman 70.3 is one of the most popular long-distance triathlons in the 
world, combining a 1.9km swim, 90km bike ride and 21.1km run. Every year, 
hundreds of thousands of amateur athletes cross finish lines at events 
across the globe — each one wondering how they can race faster and train 
smarter.

This project uses data from over 821,000 race results recorded between 
2004 and 2020 to answer a simple but powerful question: what actually 
determines how fast an amateur triathlete finishes an Ironman 70.3?

---

### What did we find?

**The bike makes or breaks your race**

Of the three disciplines, the bike segment is by far the strongest 
predictor of overall finish time. An athlete's cycling performance alone 
explains 88% of the variation in their final result. Put simply — if you 
want to finish faster, focus on your bike training first.

**Knowing your swim and bike splits can predict your finish time**

By the time an athlete exits the bike course, we can predict their finish 
time with an average error of just 15 minutes — out of a total race 
duration of around 6 hours. That is a remarkably accurate prediction 
based on only two data points.

**Men finish about 28 minutes faster than women on average — mostly 
because of the bike**

The gender gap in finish times is real but concentrated in one segment. 
Men and women show very similar variability in their performances — the 
difference is almost entirely explained by cycling speed, where 
physiological differences have the greatest impact.

**Performance declines with age, and the run suffers most**

Athletes between 25 and 39 years old perform at their peak. After 45, 
finish times start increasing progressively. The most surprising finding 
is that the run — not the bike — is the segment that deteriorates fastest 
with age. Older athletes slow down significantly more on the run than on 
the bike or swim.

**Amateur performance has not improved in 16 years**

Despite the massive growth of the sport, better equipment, and more 
accessible training resources, the average amateur finish time has 
remained essentially unchanged between 2004 and 2020. The typical 
amateur triathlete finishes in around 5 hours 54 minutes — the same 
as 16 years ago. The only exception is 2020, where times were faster, 
likely because COVID-19 cancellations meant only the most experienced 
athletes competed that year.

---

### How was this done?

We used machine learning — a branch of artificial intelligence that 
learns patterns from data — to build models that predict finish times. 
We started with a simple baseline that always predicted the average 
finish time, and progressively improved it by adding more information.

The final model, called Gradient Boosting, can predict an athlete's 
finish time after they complete the swim and bike segments with an 
average error of 15 minutes. This is a significant improvement over 
simply guessing the average, which would be off by nearly 40 minutes.

---

### What could this be used for?

**For athletes:** A tool that predicts your finish time in real time 
during a race, based on your swim and bike splits. This could help with 
pacing strategy and mental preparation for the run.

**For coaches:** Data-driven evidence that the bike segment deserves 
the most training attention for athletes looking to improve their overall 
finish time.

**For race organizers:** Better understanding of how different athlete 
profiles perform across events and locations.

---

### What comes next?

This project opens several interesting avenues for future exploration:

- Building a simple web tool where any triathlete can enter their swim 
  and bike splits and receive an instant finish time prediction.
- Expanding the model to include weather conditions, course elevation, 
  and athlete nationality as additional features.
- Exploring whether performance predictions can be personalized further 
  by age group and gender.
- Analyzing which specific race locations produce the fastest and slowest 
  times, and why.