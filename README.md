# 🛠 STM32 开发环境中文乱码修复指南
针对 **STM32CubeMX** 生成代码在 **Keil MDK** 中出现中文注释乱码或编译报错（如 `Error #8`）的终极解决方案。
## 📦 STM32CubeMX 配置 
**软件版本**：STM32CubeMX v6.13 / v6.14*  
为了让 CubeMX 生成符合中文 Windows 系统习惯的文件，需要修改其启动配置：  
1.找到 STM32CubeMX 的安装目录。  
2.找到并使用记事本打开 STM32CubeMX.l4j.ini 文件。  
3.在文件末尾追加以下代码：  
-Dfile.encoding=GBK  
注意：前后不要有空格，末尾不要有换行符，保存后重启 CubeMX。  

@https://blog.csdn.net/qq_49053936/article/details/145456532  

# 针对更高版本的STM32CubeMX 如 v6.15以上  
1.防止编译器在处理 GBK 字符（中文注释）时误判语法错误：  
2.在 Keil 工程右键选择 Options for Target...。  
3.切换至 C/C++ (或 C/C++ (AC6)) 选项卡。  
4.在底部的 Misc Controls 框中填入：  
--no-multibyte-chars  

---


