#### 扩展按钮点击范围

- 继承UIBUTTON, 重写方法- (CGRECT)BACKGROUNDRECTFORBOUNDS:(CGRECT)CONTENTRECT；决定背景图大小，实际按钮大小可以扩大。

#### OC示例代码　
```Objective-C
@interface LYExpendButton : UIButton
@end

@implementation LYExpendButton

- (CGRect)backgroundRectForBounds:(CGRect)contentRect {
     CGFloat x = ceilf(contentRect.size.width - 54)/2;
     CGFloat y = ceilf(contentRect.size.height - 22)/2;
     CGFloat width = 54;
     CGFloat height = 22;
     return CGRectMake(x, y, width, height);
}
@end
```