---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Dealing with Model Errors

Water Strategy reports errors when there is either a technical fault, or the model has some incorrect configuration. Learning how to read a model error report and address the issue is important when creating networks.

This chapter will give you an example on how to read the report and find which part of your model leads to the error.

## How to get the error report

When a run fails, you will see the run turn red in runs section.

<figure><img src="../../.gitbook/assets/image (296).png" alt=""><figcaption><p>Click the red run bar to get the error report</p></figcaption></figure>

Click the red run bar and you will get an overview of the run, including the error report.

<figure><img src="../../.gitbook/assets/image (297).png" alt=""><figcaption><p>The error report</p></figcaption></figure>

**Scroll to the end of the report.** This is where the run will reports its error.

<figure><img src="../../.gitbook/assets/image (298).png" alt=""><figcaption><p>Find the error type at the end of the report</p></figcaption></figure>

For this run, it can be found that a monthly profile has not been entered correctly.

In some cases, more detail will be given about an error within the run report. It is important to look back through the run logs to see if there are any clues as to the issue.&#x20;

Upon scrolling up we see 'CRITICAL'. This is an indication that an error has been recognized. In the same line, it indicates where the error is.

<figure><img src="../../.gitbook/assets/image (299).png" alt=""><figcaption><p>Find which monthly profile is incorrect</p></figcaption></figure>

The input 'evaporation' of the 'Example reservoir' node is incorrect.

We can edit the 'evaporation' parameter to solve this problem.

<figure><img src="../../.gitbook/assets/image (300).png" alt=""><figcaption><p>Click to edit the 'evaporation' parameter</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (301).png" alt=""><figcaption><p>The 'evaporation' parameter</p></figcaption></figure>

There are 13 values in the monthly profile, we need to remove the value that does not belong. In this case '3.14' was not meant to be in the monthly profile.

<figure><img src="../../.gitbook/assets/image (302).png" alt=""><figcaption><p>The 'evaporation' parameter after correction</p></figcaption></figure>

Save the parameter and run this model again.

Now the model has run successfully.

<figure><img src="../../.gitbook/assets/image (303).png" alt=""><figcaption><p>Run successful</p></figcaption></figure>
