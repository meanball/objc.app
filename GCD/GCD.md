####  Execute a task in background

```
dispatch_async(dispatch_get_global_queue(DISPATCH_QUEUE_PRIORITY_DEFAULT, 0), ^{

});
```

####  Execute a task on the main thread

```
dispatch_async(dispatch_get_main_queue(), ^{

});

```
