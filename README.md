根据LoxodonFramework 为Rougamo提供了Unity支持。

关于更多特性见仓库：`https://github.com/inversionhourglass/Rougamo`

## 安装方法：

1.在Unity包管理器中使用“从git URL添加包......”添加以下包。选择：

1. `https://github.com/vovgou/loxodon-framework.git?path=/Loxodon.Framework.Fody/Packages/com.vovgou.loxodon-framework-fody`
2. `https://github.com/meowalive/RougamoForUnity.git?path=Loxodon.Rougamo.Fody`


2：配置FodyWeavers.xml
```
<?xml version="1.0" encoding="utf-8"?>
<Weavers xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
	<AssemblyNames>
		<Item>YOUR-ASSEMBLY</Item>
	</AssemblyNames>
	<Rougamo />
</Weavers>
```
## 疑似不支持的特性
1. 方法参数不能是Ref Struct，否则无法编织。（需要Ignore）
3. 单例模式的属性疑似无法正常工作，对象池属性/结构体/接口正常工作。

## 新增的特性

except-namespaces="Name" 来忽略特定的命名空间
