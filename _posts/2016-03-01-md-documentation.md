---
layout:     post
title:      markdown 编辑文本总结
date:       2006-03-01 12:32:19
summary:    markdown 编辑文本总结
categories: github jekyll
---

超链接：
[超链接](http://thought7878.github.io)

代码块：
{% highlight ruby %}
  // 擅长专业
  	$("#major-add-btn").click(function() {
  		var majorSelectVal = $("#juei-select-major2").find("option:selected").text();
  		var majorSaveList$ = $("#major-save-list");
  		var savedMajorArr = majorSaveList$.data("majors") || [];
  		if (majorSelectVal != "请选择" && !savedMajorArr.contains(majorSelectVal)) { //不是“请选择”，并且没添加过。添加到hidden input、显示区域、list data
  			// 显示区域
  			majorSaveList$.append($("#major-li-tmpl").tmpl({
  				major: majorSelectVal
  			}));
  			// list data// hidden input
  			updateSavedMajor();
  		}
  
  	});
{% endhighlight %}


