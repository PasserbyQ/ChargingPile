ChargingPile
=================

![Pod Version](https://img.shields.io/cocoapods/v/SVProgressHUD.svg?style=flat)
![Pod Platform](https://img.shields.io/cocoapods/p/SVProgressHUD.svg?style=flat)
![Pod License](https://img.shields.io/cocoapods/l/SVProgressHUD.svg?style=flat)

### Overview-概括

### Demo-图片展示（UI层面：可选）

### Usage-用法（代码层面）

(see sample Xcode project in `/Demo`)

`SVProgressHUD` is created as a singleton (i.e. it doesn't need to be explicitly allocated and instantiated; you directly call `[SVProgressHUD method]`).

**Use `SVProgressHUD` wisely! Only use it if you absolutely need to perform a task before taking the user forward. Bad use case examples: pull to refresh, infinite scrolling, sending message.**

Using `SVProgressHUD` in your app will usually look as simple as this (using Grand Central Dispatch):

```objective-c
[SVProgressHUD show];
dispatch_async(dispatch_get_global_queue(DISPATCH_QUEUE_PRIORITY_DEFAULT, 0), ^{
    // time-consuming task
    dispatch_async(dispatch_get_main_queue(), ^{
        [SVProgressHUD dismiss];
    });
});
```

### Methods-核心方法

You can show the status of indeterminate tasks using one of the following:

```objective-c
+ (void)show;
+ (void)showWithStatus:(NSString*)string;
```

### Protocols-协议 (可选)

### Properties-属性 (可选)

### Install-安装

```ruby
pod 'SVProgressHUD'
```

### TODO-待完成

### Version-版本（该版本支持的工具版本、语言及语言版本）

版本  | 工具  | 语言
 ---- | ----- | ------  
 1.0.0  | Xcode 9+ | Swift 4+

### Author-作者

XXX

