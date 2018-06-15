#### how to copy bundle plist(which is read only) to document plist file(which is writable)?

```objective-c
- (void)copyPlistWithName:(NSString *)name {
    NSFileManager *fileManager = [NSFileManager defaultManager];
    NSError *error;
    NSArray *documentPaths = NSSearchPathForDirectoriesInDomains(NSDocumentDirectory, NSUserDomainMask, YES);
    NSString *documentsDirectory = [documentPaths objectAtIndex:0];
    NSString *documentPlistPath = [documentsDirectory stringByAppendingPathComponent:@"messages.plist"];
    NSString *bundlePath = [[NSBundle mainBundle] bundlePath];
    NSString *bundlePlistPath = [bundlePath stringByAppendingPathComponent:@"messages.plist"];

    BOOL success = [fileManager copyItemAtPath:bundlePlistPath toPath:documentPlistPath error:&error];
    if (success) {
    NSArray *array = [NSArray arrayWithContentsOfFile:documentPlistPath];
    NSLog(@"success: after copied the plist file is %@", array);
    } else {
    NSArray *array = [NSArray arrayWithContentsOfFile:documentPlistPath];
    NSLog(@"fail: after copied the plist file is %@", array);
    }
}
```

####  how to remove a file in document path

```objective-c
- (void)removeFile:(NSString *)fileName {
    NSFileManager *fileManager = [NSFileManager defaultManager];
    NSString *documentsPath = [NSSearchPathForDirectoriesInDomains(NSDocumentDirectory, NSUserDomainMask, YES) objectAtIndex:0];
    NSString *filePath = [documentsPath stringByAppendingPathComponent:fileName];
    NSError *error;
    BOOL success = [fileManager removeItemAtPath:filePath error:&error];
    if (success) {
        NSLog(@"removed");
    } else {
       NSLog(@"Could not delete file -:%@ ",[error localizedDescription]);
    }
}
```

