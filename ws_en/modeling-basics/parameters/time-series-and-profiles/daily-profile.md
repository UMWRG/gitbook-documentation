# Daily Profile

## General Description

Parameter which provides a daily profile.

The daily profile returns a different value based on the month of the current time-step.[ API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.parameters.DailyProfileParameter.html#pywr.parameters.DailyProfileParameter)



## Attributes

| Name   | Description                                                           | Required |
| ------ | --------------------------------------------------------------------- | -------- |
| type   | dailyprofile                                                          | Yes      |
| values | An array of 366 numbers whose indices represent the days of the year. | Yes      |

## Example

```json
{
    type: 'dailyprofile',
    values: [1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1 ... ]
}
```
