# 注意以下几点

## 1.升序 this.a>o.a 要return 1;其中this指向要添加的元素

return正数，o1存右边。
return负数，o1存左边。

所以:
return o1-o2（return正，o1>o2,存右边）（return负，o1<o2,存左边）-->(小的存左边，大的存右边，-->升序)


return o2-o1（return正    o1<o2,存右边）（return负，o1>o2,存左边）-->(小的存右边，大的存左边，-->降序)
## 2.降序 this.a>o.a 要return -1；
