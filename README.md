# Shadertoy 壁纸教程

将[Shadertoy](https://www.shadertoy.com/)上的特效设定为桌面壁纸

## 需要的软件

[Wallpaper Engine](https://store.steampowered.com/app/431960/Wallpaper_Engine/)

(下文简称WE)

WE可能也有别的替代品，但暂时没找到

## 食用方法

### 准备特效

1. 在[Shadertoy](https://www.shadertoy.com/)上寻找你喜欢的Shader特效，如果你懒得去找特效也没事，本仓库已经提供了几个非常经典又炫酷的特效供使用，当然对自己Shader能力很有自信的也可以自己撸一个

2. clone本仓库，并拷贝本仓库的Template目录，重命名为你选中的Shader特效名，下面以[这个Spout特效](https://www.shadertoy.com/view/lsXGzH)为例

3. 将该特效右侧的`Image`标签下的着色器代码全部拷贝至`<script type="frag"></script>`内部

```html
<script type="frag">(将着色器代码拷贝于此)</script>
```

PS：如果Shader代码不是自己写的，一定要加一个`Credit: 原网址`，这是对创作者最起码的尊重！

4. 如果有用到材质的话（该特效就用到了），将材质图片（下方的iChannel0）右键保存至特效目录下，重命名为`iChannel0.png`，在着色器的代码上方加上材质的`img`标签，`name`设定为`iChannel0`，再加个`hidden`的属性即可

如果`iChannel0.png`是个cubemap，要加上`type="cube"`，uniform的名称会相对应地变为`iChannel0Cube`

```html
<img src="./iChannel0.png" name="iChannel0" hidden />
```

### 载入特效

1. 打开WE，点击左下角的“壁纸编辑器”

2. 这时会跳出一个“欢迎”的弹窗，点击“创建壁纸”，选择你之前准备好的特效的`html`文件，再点击“确认”

3. 点击左上角的“文件”，再点击“应用壁纸”，完成！
