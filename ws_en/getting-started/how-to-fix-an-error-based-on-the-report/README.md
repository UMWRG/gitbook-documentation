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

# How to fix an error based on the report?

An error will occur when something in a model is incorrect. Learning how to read the error report and fix the error is vital to creating networks.

This chapter will give you an example on how to read the report and find which part of your model leads to the error.

## How to get the error report

When a run fails, you will see a red run under the run tab.

<figure><img src="../../.gitbook/assets/image (296).png" alt=""><figcaption><p>Click the red run bar to get the error report</p></figcaption></figure>

Click the red run bar and you will get an error report.

<figure><img src="../../.gitbook/assets/image (297).png" alt=""><figcaption><p>The error report</p></figcaption></figure>

Scroll to the end of the report. This is where the run will have failed and exited.

<figure><img src="../../.gitbook/assets/image (298).png" alt=""><figcaption><p>Find the error type at the end of the report</p></figcaption></figure>

For this run, it can be found that a monthly profile has not been entered correctly.

In some cases, more detail will be given about an error within the run report.&#x20;

Upon scrolling up and skimming we see 'CRITICAL'. This is an indication that an error has been recognized. In the same line, it indicates where the error is.

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
