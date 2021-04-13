# 常见问题

### `AttributeError: 'module' object has no attribute 'copy'`

**背景**

代码：

```python
import xlutils

newWb = xlutils.copy(gConst['xls']['fileName'])
```

报错：

```bash
AttributeError: 'module' object has no attribute 'copy'
```

**原因**：未知。可能是库本身的bug。

**解决办法**

改为：

```python
from xlutils.copy import copy

newWb = copy(gConst['xls']['fileName'])
```

即可（规避此问题）

### `AttributeError: 'str' object has no attribute 'datemode'`

**背景**

代码：

```python
from xlutils.copy import copy;

newWb = copy(gConst['xls']['fileName'])
```

出错：

```bash
   newWb = copy(gConst['xls']['fileName']);
  File "D:\tmp\dev_install_root\Python27_x64\lib\site-packages\xlutils-1.5.2-py2.7.egg\xlutils\copy.py", line 13, in copy
    w
  File "D:\tmp\dev_install_root\Python27_x64\lib\site-packages\xlutils-1.5.2-py2.7.egg\xlutils\filter.py", line 827, in process
    reader(chain[0])
  File "D:\tmp\dev_install_root\Python27_x64\lib\site-packages\xlutils-1.5.2-py2.7.egg\xlutils\filter.py", line 60, in __call__
    filter.workbook(workbook,filename)
  File "D:\tmp\dev_install_root\Python27_x64\lib\site-packages\xlutils-1.5.2-py2.7.egg\xlutils\filter.py", line 267, in workbook
    self.wtbook.dates_1904 = rdbook.datemode
AttributeError: 'str' object has no attribute 'datemode'
```

**原因**：参考官网的资料 [xlutils copy](https://secure.simplistix.co.uk/svn/xlutils/trunk/xlutils/docs/copy.txt)，才知道`copy`的参数，是对应的`workbook`，而不是`xls`的`filename`

**解决办法**：先从excel文件中（通过`xlrd`）读取得到`workbook`，再去用`copy`

**代码**

```python
import xlwt
import xlrd
#import xlutils
from xlutils.copy import copy

oldWb = xlrd.open_workbook(gConst['xls']['fileName'])
print oldWb; #<xlrd.book.Book object at 0x000000000315C940>
newWb = copy(oldWb)
print newWb; #<xlwt.Workbook.Workbook object at 0x000000000315F470>
```

才真正可以正常打开旧的xls，拷贝出一份新的xls

