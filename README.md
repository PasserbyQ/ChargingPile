项目名 ([Readme语法](https://blog.csdn.net/qq_31796651/article/details/80803599))
=================

![Pod Version](https://img.shields.io/cocoapods/v/SVProgressHUD.svg?style=flat)
![Pod Platform](https://img.shields.io/cocoapods/p/SVProgressHUD.svg?style=flat)
![Pod License](https://img.shields.io/cocoapods/l/SVProgressHUD.svg?style=flat)

### Overview-概括

这是干嘛的，用了有啥好处等等

### Demo-图片展示（UI层面：可选）

![Screenshots_Row1](https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1567422035678&di=7b11acd72a3c8ad77c335c3855647c2e&imgtype=0&src=http%3A%2F%2Fi0.hexunimg.cn%2F2013-04-10%2F153010415.jpg)

### Usage-用法（代码层面）

(see sample Xcode project in `/Demo`)

`XXX` is created as a singleton.

**注意点.**

Using `XXX` in your app will usually look as simple as this (using Grand Central Dispatch):

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

```objective-c
- (void)hideAnimated:(BOOL)animated;
```

### Properties-属性 (可选)

```objective-c
@property (nonatomic, assign) BOOL runningStatus;
```

### Install-安装

```ruby
pod 'SVProgressHUD'
```

### TODO-待完成

 * 还有啥没干没点数么


### Version-版本

版本  | 工具  | 语言
 ---- | ----- | ------  
 1.0.1  | Xcode 9+ | Swift 4+
 1.0.0  | Xcode 9+ | Swift 4+

### Author-作者

 xxx

