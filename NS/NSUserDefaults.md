#### NSUserDefaults set

```objective-c
- (void)customSet {
    [[NSUserDefaults standardUserDefaults] setObject:textField.text forKey:@"mainTitle"];
    [[NSUserDefaults standardUserDefaults] synchronize];
}

#### NSUserDefaults get

```objective-c
- (void)customGet {
    NSString *title = [[NSUserDefaults standardUserDefaults] objectForKey:@"mainTitle"];
}
```
