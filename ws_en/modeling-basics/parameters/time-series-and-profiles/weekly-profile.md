# Weekly Profile

## General Description

The **weekly profile** contains 52 weeks per year. The last week of the year will have more than 7 days, as 365 / 7 is not whole.[ API Reference](https://pywr.github.io/pywr-docs/master/api/generated/pywr.parameters.WeeklyProfileParameter.html)



## Attributes

| Name   | Description                                                          | Required |
| ------ | -------------------------------------------------------------------- | -------- |
| type   | weeklyprofile                                                        | Yes      |
| values | An array of 52 numbers whose indices represent the days of the year. | Yes      |

## Example

```json
{
    type: 'weeklyprofile',
    values: [1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1 ... ]
}
```
