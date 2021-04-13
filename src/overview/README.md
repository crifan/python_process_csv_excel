# 概述

* `csv`
* `Excel`

用Python处理`csv`和`Excel`的常见库有：

* `csv`库
  * Python内置库：`csv`
  * `pandas`
    * 读：`pandas.read_csv`
    * 写：`pandas.DataFrame.to_csv`
* `Excel`库
  * 读写文件的库
    * `openpyxl`
      * 功能强大，支持设置背景色等样式的细节设置
      * 支持新的（`Excel 2010`之后的）格式：`.xlsx`
    * `xlutils`：
      * 概述
        * 整合了`xlrd`和`xlwt`，额外加`copy`等辅助功能
        * 只支持Excel旧格式：`.xls`
      * 相关库
        * 读：`xlrd`
        * 写：`xlwt`
    * `pandas`
      * 读：`pandas.read_excel`
      * 写：`pandas.DataFrame.to_excel`
    * 其他
      * `xlsxwriter`
        * An alternative package for writing data, formatting information and, in particular, charts in the Excel 2010 format (ie: .xlsx)
      * `pyxlsb`
        * This package allows you to read Excel files in the xlsb format.
      * `pylightxl`
        * This package allows you to read xlsx and xlsm files and write xlsx files.
  * 自动化操作的库
    * 说明：对于Excel文件的自动化操作 =对标旧的Excel（其实是`Microsoft`的`Office`的）`VBA`脚本 = 英文称:`Excel add-ins`
      * 注意：需要系统中已安装`Excel`软件
    * 库
      * `PyXLL`
        * 概述
          * PyXLL is a commercial product that enables writing Excel add-ins in Python with no VBA. Python functions can be exposed as worksheet functions (UDFs), macros, menus and ribbon tool bars.
        * 主页
          * https://www.pyxll.com/
      * `xlwings`
        * 概述
          * xlwings is an open-source library to automate Excel with Python instead of VBA and works on Windows and macOS: you can call Python from Excel and vice versa and write UDFs in Python (Windows only). xlwings PRO is a commercial add-on with additional functionality.
        * 主页
          * https://www.pyxll.com/

## 如何选择

* 根据不同情况，选择合适的解析`csv`和`Excel`的Python库
  * 数据量不大的 + 简单的 csv文件：Python自带的`csv`库
  * 数据量不大的 + Excel旧文件`.xls` + 操作不复杂：`xlutils` (`xlrd`+`xlwt`)
  * 数据量不大的 + Excel新格式`.xlsx` + 操作复杂 + 能设置样式：`openpyxl`
  * 数据量较大的`csv`或`Excel`，主要用于数据处理和计算的：`pandas`
