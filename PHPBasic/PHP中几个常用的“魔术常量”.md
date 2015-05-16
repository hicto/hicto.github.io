## PHP中几个常用的“魔术常量”

[来源](http://php.net/manual/zh/language.constants.predefined.php)：http://php.net/manual/zh/language.constants.predefined.php

------

PHP为其运行的脚本提供了大量的预定义常量，但是这些常量是由不能的扩展库提供的，所有，只有在加载了对应的扩展库之后才可以使用。不过，有些常量也可以在动态加载后可见，或者在编译时就已经包括进来了。

下表中列出了8个常见的“魔术常量”，它们的值并非是一层不变的，而是随着它们在代码中的位置而发生改变。

**注意：** 这些特殊的常量是*不分区大小写*的。

|名称|说明|
|:---|:---|
|\_\_LINE__ |文件中的当前行号|
|\_\_FILE__ |文件的完整路径和文件名。如果用在被包含文件中，则返回被包含的文件名。自 PHP 4.0.2 起，\_\_FILE__总是包含一个绝对路径（如果是符号连接，则是解析后的绝对路径），而在此之前的版本有时会包含一个相对路径|
|\_\_DIR__ | 文件所在的目录。如果用在被包括文件中，则返回被包括的文件所在的目录。它等价于 dirname(\_\_FILE__ )。除非是根目录，否则目录中名不包括末尾的斜杠。（PHP 5.3.0中新增）= |
|\_\_FUNCTION__ |函数名称（PHP 4.3.0 新加）。自 PHP 5 起本常量返回该函数被定义时的名字（区分大小写）。在 PHP 4 中该值总是小写字母的|
|\_\_CLASS__ |类的名称（PHP 4.3.0 新加）。自 PHP 5 起本常量返回该类被定义时的名字（区分大小写）。在 PHP 4 中该值总是小写字母的。类名包括其被声明的作用区域（例如 Foo\Bar）。注意自 PHP 5.4 起 \_\_CLASS__ 对 trait 也起作用。当用在 trait 方法中时，\_\_CLASS__ 是调用 trait 方法的类的名字|
|\_\_TRAIT__ |Trait 的名字（PHP 5.4.0 新加）。自 PHP 5.4 起此常量返回 trait 被定义时的名字（区分大小写）。Trait 名包括其被声明的作用区域（例如 Foo\Bar）|
|\_\_METHOD__ |类的方法名（PHP 5.0.0 新加）。返回该方法被定义时的名字（区分大小写）|
|\_\_NAMESPACE__ |当前命名空间的名称（区分大小写）。此常量是在编译时定义的（PHP 5.3.0 新增）|

参见 [get_class()](http://php.net/manual/zh/function.get-class.php)，[get_object_vars()](http://php.net/manual/zh/function.get-object-vars.php)，[file_exists()](http://php.net/manual/zh/function.file-exists.php) 和 [function_exists()](http://php.net/manual/zh/function.function-exists.php)

