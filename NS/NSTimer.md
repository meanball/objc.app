#### call a method for every 60 seconds

```objecitve-c
- (void)setupYourTimer {
    [NSTimer scheduledTimerWithTimeInterval:60.0 target:self selector:@selector(callMethod) userInfo:nil repeats:YES];
}

- (void)callMethod {
    //Your called method
}
```
