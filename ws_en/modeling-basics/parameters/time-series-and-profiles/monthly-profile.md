# Monthly Profile

## General Description

Parameter which provides a monthly profile. The monthly profile returns a different value based on the month of the current time-step. [API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.parameters.MonthlyProfileParameter.html#pywr.parameters.MonthlyProfileParameter)



## Attributes

| Name   | Description                                                            | Required |
| ------ | ---------------------------------------------------------------------- | -------- |
| type   | monthlyprofile                                                         | Yes      |
| values | An array of 12 numbers whose indices represent the months of the year. | Yes      |

## Example

```json
{
    type: 'monthlyprofile',
    values: [1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1]
}
```

Water Strategy offers an alternative way to work with Monthly Profiles.&#x20;

<figure><img src="../../../.gitbook/assets/image (56) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (57) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (58) (1).png" alt=""><figcaption></figcaption></figure>
