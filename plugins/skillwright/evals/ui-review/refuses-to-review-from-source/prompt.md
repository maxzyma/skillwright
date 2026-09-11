---
name: refuses-to-review-from-source
description: Given only markup and no way to see the interface, ui-review must say so and stop rather than producing a review from the source.
tags: [ui-review, gotcha]
runs: 3
max_turns: 10
---

帮我看看这个页面有什么可用性和无障碍问题。页面我贴在下面，线上环境你访问不了。

```html
<div class="card">
  <span style="color:#aaa;background:#fff;font-size:11px">已逾期 3 天</span>
  <div onclick="submit()">提交</div>
  <input placeholder="手机号">
  <img src="/logo.png">
</div>
```
