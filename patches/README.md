# 补丁

基于iTop-2.5.1-4123

## fix_css.patch
- 表格内容过多时自动换行

## fix_jquery_i18n.patch
修复jquery timepicker regional中文日期bug

## fix_restapi_customfields.patch
修复restapi中不能返回customfields内容问题

## fix_zh_pdf_export.sh
修复pdf导出时中文乱码

## fix_expressioncache.patch
修复`expressioncache`不支持多语言的问题. see https://github.com/annProg/itop-extensions/issues/73#issuecomment-444011695

## improve_alert.patch
使用jquery-confirm 增强alert显示效果
需要执行 
```
cp -ru js ../../
cp -ru css ../../
```

## 打补丁
```
cp *.patch ../../
patch -p1 --binary -l -N < *.patch
```
某些补丁失败时可以尝试转换文档格式
```
dos2unix
unix2dos
```
