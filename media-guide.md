---
title: 媒体文件使用示例
parent: Sugar Level
nav_order: 100
layout: default
---

# 如何添加图片和视频

## 添加图片

### 本地图片（推荐）
```markdown
![图片描述]({{ site.baseurl }}/assets/images/example.jpg)
```

### 使用相对路径
```markdown
![图片描述](/assets/images/example.jpg)
```

### 带链接的图片
```markdown
[![图片描述]({{ site.baseurl }}/assets/images/example.jpg)](链接地址)
```

### 控制图片大小
```html
<img src="{{ site.baseurl }}/assets/images/example.jpg" alt="图片描述" width="300" height="200">
```

## 添加视频

### HTML5视频（推荐）
```html
<video width="640" height="480" controls>
  <source src="{{ site.baseurl }}/assets/videos/example.mp4" type="video/mp4">
  您的浏览器不支持视频标签。
</video>
```

### YouTube嵌入
```html
<iframe width="560" height="315" 
  src="https://www.youtube.com/embed/视频ID" 
  frameborder="0" allowfullscreen>
</iframe>
```

### Bilibili嵌入
```html
<iframe src="//player.bilibili.com/player.html?bvid=BV号" 
  scrolling="no" border="0" frameborder="no" framespacing="0" 
  allowfullscreen="true" width="640" height="430">
</iframe>
```

## 文件上传步骤

1. **将文件复制到对应文件夹**：
   - 图片文件 → `assets/images/`
   - 视频文件 → `assets/videos/`

2. **提交到Git**：
   ```bash
   git add assets/
   git commit -m "添加媒体文件"
   git push
   ```

3. **在markdown中引用**：
   使用上面的语法引用文件

## 注意事项

- 图片推荐格式：JPG, PNG, GIF, SVG
- 视频推荐格式：MP4, WebM
- 文件大小建议控制在合理范围内
- 文件名使用英文和数字，避免特殊字符