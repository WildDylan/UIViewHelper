# UIViewHelper

[![CI Status](http://img.shields.io/travis/Dylan/UIViewHelper.svg?style=flat)](https://travis-ci.org/Dylan/UIViewHelper)
[![Version](https://img.shields.io/cocoapods/v/UIViewHelper.svg?style=flat)](http://cocoapods.org/pods/UIViewHelper)
[![License](https://img.shields.io/cocoapods/l/UIViewHelper.svg?style=flat)](http://cocoapods.org/pods/UIViewHelper)
[![Platform](https://img.shields.io/cocoapods/p/UIViewHelper.svg?style=flat)](http://cocoapods.org/pods/UIViewHelper)

## Usage

To run the example project, clone the repo, and run `pod install` from the Example directory first.

## Methods

- properties

```objc

@property (nonatomic, assign) CGPoint origin;
@property (nonatomic, assign) CGSize size;
@property (nonatomic, assign) CGFloat top;
@property (nonatomic, assign) CGFloat left;
@property (nonatomic, assign) CGFloat bottom;
@property (nonatomic, assign) CGFloat right;
@property (nonatomic, assign) CGFloat width;
@property (nonatomic, assign) CGFloat height;
@property (nonatomic, assign) CGFloat x;
@property (nonatomic, assign) CGFloat y;
@property (nonatomic, assign) CGSize boundsSize;
@property (nonatomic, assign) CGFloat boundsWidth;
@property (nonatomic, assign) CGFloat boundsHeight;
@property (nonatomic, readonly) CGRect contentBounds;
@property (nonatomic, readonly) CGPoint contentCenter;

@property (nonatomic, strong) UILabel *badge;
@property (nonatomic, strong) UIColor *badgeBgColor;
@property (nonatomic, strong) UIColor *badgeTextColor;
@property (nonatomic, assign) CGRect badgeFrame;
@property (nonatomic, assign) DLBadgeAnimType aniType;

```

- methods

```objc

// shake View
- (void)shakeView;

// show bage
- (void)showDLBadge;
- (void)showDLBadgeWithStyle:(DLBadgeStyle)style value:(NSInteger)value animationType:(DLBadgeAnimType)aniType;
- (void)clearBadge;

// Moves
- (void)moveTo:(CGPoint)destination duration:(float)secs option:(UIViewAnimationOptions)option;
- (void)moveTo:(CGPoint)destination duration:(float)secs option:(UIViewAnimationOptions)option delegate:(id)delegate callback:(SEL)method;
- (void)raceTo:(CGPoint)destination withSnapBack:(BOOL)withSnapBack;
- (void)raceTo:(CGPoint)destination withSnapBack:(BOOL)withSnapBack delegate:(id)delegate callback:(SEL)method;

// Transforms
- (void)rotate:(int)degrees secs:(float)secs delegate:(id)delegate callback:(SEL)method;
- (void)scale:(float)secs x:(float)scaleX y:(float)scaleY delegate:(id)delegate callback:(SEL)method;
- (void)spinClockwise:(float)secs;
- (void)spinCounterClockwise:(float)secs;

// Transitions
- (void)curlDown:(float)secs;
- (void)curlUpAndAway:(float)secs;
- (void)drainAway:(float)secs;

// Effects
- (void)changeAlpha:(float)newAlpha secs:(float)secs;
- (void)pulse:(float)secs continuously:(BOOL)continuously;

// add subview with animation
- (void)addSubviewWithFadeAnimation:(UIView *)subview;

// gesture with block
- (void)addTapActionWithBlock:(GestureActionBlock)block;
- (void)addLongPressActionWithBlock:(GestureActionBlock)block;

// firstResponderViewController
- (UIViewController *)firstResponderViewController;


```

## Requirements

## Installation

UIViewHelper is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod "UIViewHelper"
```

## Author

Dylan, 3664132@163.com

## License

UIViewHelper is available under the MIT license. See the LICENSE file for more info.
