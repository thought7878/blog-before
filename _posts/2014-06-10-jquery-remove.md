---
layout:     post
title:      jquery remove()方法详解
date:       2015-03-02 12:31:19
summary:    jquery remove()方法详解
categories: jquery
---

暂时做个记录，有空详细解析下jquery remove()方法。

---

问题代码如下：
{% highlight ruby %}
  $(".adviser-manage-container").delegate('.icon-remove', 'click', function(event) {
    $(this).parent().remove();//这里先删除
    var adviserItemWrapper$ = $(this).parents(".adviser-item-wrapper");//问题在这里：adviserItemWrapper$.length值为0
    if (adviserItemWrapper$.length > 0) {//更新下的//问题在这里：adviserItemWrapper$.length值为0
      var csList$ = adviserItemWrapper$.find(".country-save-list");
      var csInput$ = adviserItemWrapper$.find(".country-save-input");
      updateSavedCountry(csList$,csInput$);
    }else{//新增下的
      updateSavedCountry(countrySaveList$,countrySaveInput$);
    }
  });
{% endhighlight %}


