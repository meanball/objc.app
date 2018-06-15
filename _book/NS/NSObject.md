#### Singleton

```objecitve-c
+ (instanceType *)sharedInstance {
    static instanceType *sharedInstance = nil;
    static dispatch_once_t onceToken; // onceToken = 0
    dispatch_once(&onceToken, ^{
        sharedInstance = [[instanceType alloc] init];
    });

     return sharedInstance;
}
```
