#### generate the date by days difference

```objecitve-c
NSDate *sevenDaysAgo = [[NSCalendar currentCalendar] dateByAddingUnit:NSCalendarUnitDay value:-7 toDate:[NSDate date] options:0];
```
