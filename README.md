# 将lua脚本导入wireshark中
将BinDecHex.lua和omci.lua拷贝到'C:\Program Files\Wireshark\plugins\'下

# 生成二进制文件
./gen_hexdump -i [你的log文件] -o omci.hex

*如果你的log不满足，可以修改cpp文件并编译：g++ -Wall -std=c++0x -o gen_hexdump gen_hexdump.cpp*

# 导入二进制文件
打开Wireshark，按如下操作操作：
File -> Import from Hex Dump  
Browse -> omci.hex  
Encapsulation Type -> Ethernet  
Ethernet -> Ethertype (hex): 8888  
