#### Set property in a category

```
NSString const *customKey = @"kCustom";

- (void)setCustom:(NSString *)custom {
    objc_setAssociatedObject(self, &customKey, custom, OBJC_ASSOCIATION_RETAIN_NONATOMIC);
}

- (NSString *)custom {
    return objc_getAssociatedObject(self, &customKey);
}
```