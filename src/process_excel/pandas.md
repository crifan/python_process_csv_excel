# pandas

Python的科学计算方面的库，主要用于数据处理的`pandas`，也可以操作`excel`和`csv`

* `pandas`
  * 官网API文档
    * Excel
      * 读：`pandas.read_excel`
        * pandas.read_excel — pandas 1.2.4 documentation
          * https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_excel.html
            * 语法
              * `pandas.read_excel(io, sheet_name=0, header=0, names=None, index_col=None, usecols=None, squeeze=False, dtype=None, engine=None, converters=None, true_values=None, false_values=None, skiprows=None, nrows=None, na_values=None, keep_default_na=True, na_filter=True, verbose=False, parse_dates=False, date_parser=None, thousands=None, comment=None, skipfooter=0, convert_float=True, mangle_dupe_cols=True, storage_options=None)`
      * 写：`pandas.DataFrame.to_excel`
        * pandas.DataFrame.to_excel — pandas 1.2.4 documentation
          * https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.to_excel.html
            * 语法
              * `DataFrame.to_excel(excel_writer, sheet_name='Sheet1', na_rep='', float_format=None, columns=None, header=True, index=True, index_label=None, startrow=0, startcol=0, engine=None, merge_cells=True, encoding=None, inf_rep='inf', verbose=True, freeze_panes=None, storage_options=None)[source]`
    * csv
      * 读：`pandas.read_csv`
        * pandas.read_csv — pandas 1.2.4 documentation
          * https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_csv.html
            * 语法
              * `pandas.read_csv(filepath_or_buffer, sep=<object object>, delimiter=None, header='infer', names=None, index_col=None, usecols=None, squeeze=False, prefix=None, mangle_dupe_cols=True, dtype=None, engine=None, converters=None, true_values=None, false_values=None, skipinitialspace=False, skiprows=None, skipfooter=0, nrows=None, na_values=None, keep_default_na=True, na_filter=True, verbose=False, skip_blank_lines=True, parse_dates=False, infer_datetime_format=False, keep_date_col=False, date_parser=None, dayfirst=False, cache_dates=True, iterator=False, chunksize=None, compression='infer', thousands=None, decimal='.', lineterminator=None, quotechar='"', quoting=0, doublequote=True, escapechar=None, comment=None, encoding=None, dialect=None, error_bad_lines=True, warn_bad_lines=True, delim_whitespace=False, low_memory=True, memory_map=False, float_precision=None, storage_options=None)[source]`
      * 写：`pandas.DataFrame.to_csv`
        * pandas.DataFrame.to_csv — pandas 1.2.4 documentation
          * https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.to_csv.html
            * 语法
              * `DataFrame.to_csv(path_or_buf=None, sep=',', na_rep='', float_format=None, columns=None, header=True, index=True, index_label=None, mode='w', encoding=None, compression='infer', quoting=None, quotechar='"', line_terminator=None, chunksize=None, date_format=None, doublequote=True, escapechar=None, decimal='.', errors='strict', storage_options=None)`
