#### Set start view controller programmingly

Put your customised code such as below nside AppDidFinishLaunch

```swift
self.window = [[UIWindow alloc] initWithFrame:UIScreen.mainScreen.bounds];
UIStoryboard *storyboard = [UIStoryboard storyboardWithName:@"Main" bundle:nil];
StartViewController * startViewController = (StartViewController*)[storyboard instantiateViewControllerWithIdentifier: @"StartViewController"];
self.window.rootViewController = startViewController;
[self.window makeKeyAndVisible];
```


#### Enable back swipe gestures programmingly
Sometimes after you customised the back button in navigation cotnroller, the back swipe gesture was disabled.

```

- (void)enableBackSwipeGesture {
    if ([self.navigationController respondsToSelector:@selector(interactivePopGestureRecognizer)]) {
        self.navigationController.interactivePopGestureRecognizer.enabled = YES;
        self.navigationController.interactivePopGestureRecognizer.delegate = self;
    }
}
- (BOOL)gestureRecognizerShouldBegin:(UIGestureRecognizer *)gestureRecognizer {
    return YES;
}
```

#### Present UIActivityViewController programminly

```
NSString *text = @"hello world";
NSURL *url = [NSURL URLWithString:@"http://airbob.github.io/lifeNumber"];
UIImage *image = [UIImage imageNamed:@"yourImage"];

UIActivityViewController *controller = [[UIActivityViewController alloc] initWithActivityItems:@[text, url, image] applicationActivities:nil];

controller.excludedActivityTypes = @[UIActivityTypePrint,
                                     UIActivityTypeCopyToPasteboard,
                                     UIActivityTypeAssignToContact,
                                     UIActivityTypeSaveToCameraRoll,
                                     UIActivityTypeAddToReadingList,
                                     UIActivityTypeAirDrop];
[self presentViewController:controller animated:YES completion:nil];
```
