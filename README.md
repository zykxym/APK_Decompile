# APK_Decompile
apk反编译说明
1.准备工具
(1)  apktool （资源文件获取） 	https://bitbucket.org/iBotPeaches/apktool/downloads/
(2)  dex2jar（源码文件获取）	https://sourceforge.net/projects/dex2jar/files/
(3)  jd-gui  （源码查看）	https://github.com/java-decompiler/jd-gui/releases/tag/v1.6.6

2.cmd反编译目录下运行
D:\fan_bian_yi> java -jar apktool_2.4.1.jar d -f D:\fan_bian_yi_text\momo.apk -o apk
(1) apktool_2.4.1.jar		下载的apktool jar文件
(2) D:\fan_bian_yi_text\ssk.apk	需要反编译的apk文件
(3) apk  			反编译后存放文件夹名称，存放在当前文件夹(fan_bian_yi)新建文件夹(apk)中
得到res文件夹与AndroidManifest.xml文件

3.将要反编译的APK后缀名改为.rar或者 .zip，并解压，得到其中的classes.dex文件（它就是java文件编译再通过dx工具打包而成的），将获取到的classes.dex放到之前解压出来的工具【dex2jar-2.0】文件夹内，cmd定位到dex2jar-2.0文件夹下，
执行“d2j-dex2jar classes.dex”得到“classes-dex2jar.jar”

4.将classes-dex2jar.jar拖入jd-gui查看源码