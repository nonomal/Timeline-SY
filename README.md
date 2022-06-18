# Timeline Beta

此项目是将 [TimelineJS3](https://github.com/NUKnightLab/TimelineJS3) 移植为思源笔记挂件。

## 预览

![](https://b3logfile.com/file/2022/06/preview-b9ad35d5.png?imageView2/2/interlace/1/format/webp)

## 使用说明

* **界面介绍**

  界面分为上、下两部分，上方为时间轴，时间轴上显示所创建的事件和时期；下方为幻灯片，点击时间轴上的事件或时期即可展示其具体内容。
* **时间线内容组成：** 标题、事件和时期

  * 标题是用来描述该时间线的主题，一个时间线仅有一个标题，不可删除。
  * 事件是对应某一时间点的项目，在时间轴上占据某一时间点。
  * 时期是对应某一时间段的项目，在时间轴上占据某一时间段。
* **时间线编辑操作：** 新建、编辑和删除

  * 新建：点击新建按钮可新建一个项目，其中开始日期和标题为必填项，结束日期、描述和背景图片为选填项。
    * 若结束日期留空，则表示该项目为一个事件，否则表示一个时期。
    * 描述为对该时间或时期的具体描述。

      标题与描述支持使用 **markdown 语法插入网页链接**

    * 背景图片为该事件或时期对应幻灯片的背景，背景图片须填入图片的 url ，也可为思源的资源文件，格式为 `assets/xxx.jpg/png`。

    ![image.png](https://b3logfile.com/file/2022/05/edit-9023174f.png?imageView2/2/interlace/1/format/webp)
  * 编辑：点击编辑按钮可编辑当前幻灯片所对应的事件或时期的内容。
  * 删除：点击编辑按钮可编辑当前幻灯片所对应的事件或时期，注意当时间轴上仅有一个事件或时期时无法删除，因为时间轴上至少要有一个项目。
  * 可在浏览器打开时间线进行编辑操作，在浏览器编辑后需在思源中刷新时间线才能看到浏览器编辑后的内容。

* **嵌入或链接到思源内容块**

  * **链接**：**描述**支持粘贴**思源块超链接**,粘贴思源块超链接不影响输入其他内容，保存后点击链接即可跳转到对应块。
    
    同时，**思源块超链接**同样支持 markdown 链接语法，可通过`[锚文本](思源块超链接)`语法插入超链接。
    ![image.png](https://b3logfile.com/file/2022/06/%E5%9B%BE%E7%89%87-f36db112.png?imageView2/2/interlace/1/format/webp)

  * **嵌入**：在**思源块id**填入 id 即可在幻灯片嵌入该内容块。
    ![image.png](https://b3logfile.com/file/2022/06/embedblock-14d6ed31.png?imageView2/2/interlace/1/format/webp)

* **数据存储：** 时间线数据存储在挂件块的自定义属性中，建议将数据做个备份以防不测。

## 感谢

[NUKnightLab](https://github.com/NUKnightLab) 的 [TimelineJS3](https://github.com/NUKnightLab/TimelineJS3)

感谢 [leolee9086](https://github.com/leolee9086) 提供的帮助以及贡献了“嵌入思源内容块"功能

感谢**池鱼**以及 [Zuoqiu-Yingyi](https://github.com/Zuoqiu-Yingyi) 提供的帮助

## 更新日志

- 20220618：v0.0.9，新增刷新时间线，在浏览器编辑后在思源中刷新才能看到
- 20220614：v0.0.8，支持鼠标滚轮切换幻灯片
- 20220530：v0.0.7，支持直接插入思源块超链接，支持markdown语法插入思源块超链接
- 20220527：v0.0.6，描述支持换行，删除时自动跳到下一个
- 20220525：v0.0.5，支持嵌入思源内容块
- 20220524：v0.0.4，支持链接到思源内容块，支持markdown语法链接