#### set round corner of a view

```
yourView.layer.cornerRadius = 5.0;
yourView.layer.masksToBounds = YES;
```

#### set round corner on only certain corner

```
//bottom left&right for example:
UIBezierPath *maskPath = [UIBezierPath bezierPathWithRoundedRect:yourView.bounds byRoundingCorners:(UIRectCornerBottomLeft | UIRectCornerBottomRight) cornerRadii:CGSizeMake(20, 20)
];

CAShapeLayer *maskLayer = [CAShapeLayer layer];

maskLayer.frame = self.bounds;
maskLayer.path = maskPath.CGPath;

yourView.layer.mask = maskLayer;

```

#### set border color and width

```
yourView.layer.borderColor = [UIColor redColor].CGColor;
yourView.layer.borderWidth = 3.0f;
```
