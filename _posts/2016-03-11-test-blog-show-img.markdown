---
layout: post
title: 博客一直显示不了图片-测试
date: 2013-10-11 00:59:56.000000000 +09:00
tags: 测试博客
---

```ruby
def hello
  puts 'Hello'
end
```


```objc
//ContainerVC.m

[self addChildViewController:toVC];
[fromVC willMoveToParentViewController:nil];
[self.view addSubview:toVC.view];

__weak id weakSelf = self;
[self transitionFromViewController:fromVC
                  toViewController:toVC duration:0.3
                           options:UIViewAnimationOptionTransitionCrossDissolve
                        animations:^{}
                        completion:^(BOOL finished) {
    [fromVC.view removeFromSuperView];
    [fromVC removeFromParentViewController];
    [toVC didMoveToParentViewController:weakSelf];
}];
```

下面测试显示图片:
----

![BouncePresentAnimation的实际效果](/assets/images/avatar.jpg)

-----
![](/assets/images/background-cover.jpg)

-----
![](/assets/images/favicon.png)
