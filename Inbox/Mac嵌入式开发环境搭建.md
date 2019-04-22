# Mac嵌入式开发环境搭建
## STM32 交叉编译器
### 下载地址
```
https://launchpad.net/gcc-arm-embedded/+download
```
### 环境变量
```
export PATH=/Users/apple/gcc-arm-none-eabi/bin:$PATH
export PATH=/Users/apple/stlink.git:$PATH
```

## 安装ST-Link2 调试工具
### 依赖包
- XCode 5 Command Line Tools。
- ibusb-1.0
- pkg-config
- autotools
- git。

```
brew install {pacakge}
```

### 编译ST-Link2 
下载源码
```
git clone https://github.com/texane/stlink.git
./autogen.sh
./configure
make
```  
也可从STM32官网直接[下载](https://www.stmcu.com.cn/Designresource/design_resource_detail?file_name=STSW_LINK007_ST-LINK_ST-LINK-V2_ST-LINK-V2-1%E5%9B%BA%E4%BB%B6%E5%8D%87%E7%BA%A7%E7%A8%8B%E5%BA%8F&lang=EN&ver=2.31.21)可执行软件

擦除命令测试
```
./st-flash erase

```

## 相关可用开发工具
|       类型       |                                             名称                                              |
| --------------- | -------------------------------------------------------------------------------------------- |
| 串口工具         | https://itunes.apple.com/cn/app/serialport-chuan-kou-gong-ju/id1181734730?mt=12            |
| eclipse+openOCD | http://salvatoremenendez.blogspot.com/2011/08/mac-os-eclipse-openocd-stm32-arm-cortex.html |
| STM32 library   | https://www.st.com/en/embedded-software/stm32-standard-peripheral-libraries.html           |