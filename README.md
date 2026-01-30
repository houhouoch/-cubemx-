# -cubemx-
CubeMX v6.13、v6.14
解决中文乱码
打开cubemx文件所在地
在文件夹里，双击打开：STM32CubeMX.l4j.ini
在末尾文件，追加：-Dfile.encoding=GBK   （前后不带空格、末尾不带回车换行) 
Keil：Edit / Configuration / Encoding / GB2312

@https://blog.csdn.net/qq_49053936/article/details/145456532
//争对更高版本的cubemx
在mdk中的C++中 Misc Controls中写入
--no-multibyte-chars
目的是告诉编译器：“把源代码里的所有字符都当成单字节的 ASCII 码来处理，别试图去解析什么多字节编码（如 UTF-8 或 GBK）。”

经过以上设置：cubemx生成的文件中 若含有中文注释 再也不乱码了
