### 使用步骤
1、在C:\Program Files\Wireshark\下新建lua目录  
2、将两个lua文件拷贝到刚才建的lua目录下  
3、在C:\Program Files\Wireshark\init.lua最后增加一行：dofile(DATA_DIR.."lua\\omci.lua")  
4、在30上运行./gen_hexdump -i xxx.md -o omci.hex  
5、导入hex文件  
File -> Import from Hex Dump  
Browse -> omci.hex  
Encapsulation Type -> Ethernet  
Ethernet -> Ethertype (hex): 8888  
