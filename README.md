# serverSpeeser_Install
redirect to https://github.com/0oVicero0/serverSpeeder_Install

blog https://moeclub.org/2017/03/08/14/
====================================================================================
wget --no-check-certificate -qO /tmp/appex.sh "https://raw.githubusercontent.com/0oVicero0/serverSpeeder_Install/master/appex.sh" && bash /tmp/appex.sh 'install'


安装一开始的时候，会提示：

Press Enter to Continue...
# 这个是提示你按回车键继续
如果安装过程中没问题的话，最后会提示：

Accelerate VPN (PPTP,L2TP,etc.)? [n]:
# 是否加速VPN
 
Auto load ServerSpeeder on linux start-up? [y]:
# 是否开机启动
 
Run ServerSpeeder now? [y]:
# 是否现在启动锐速
 
# 全部默认回车即可。
最后出现这样的提示就说明安装并启动成功：

[Running Status]
ServerSpeeder is running!
version              3.11.20.4
 
[License Information]
License              6001ADDF578B6C0E (valid on current device)
MaxSession           unlimited
MaxTcpAccSession     unlimited
MaxBandwidth(kbps)   1024000
ExpireDate           2035-12-31
....
# 以下省略....
卸载LotServer

wget --no-check-certificate -qO /tmp/appex.sh "https://raw.githubusercontent.com/0oVicero0/serverSpeeder_Install/master/appex.sh" && bash /tmp/appex.sh 'uninstall'
使用说明

/appex/bin/serverSpeeder.sh start
# 启动 LotServer
 
/appex/bin/serverSpeeder.sh stop
# 停止 LotServer
 
/appex/bin/serverSpeeder.sh restart
# 重启 LotServer
 
/appex/bin/serverSpeeder.sh status
# 状态查询
 
/appex/bin/serverSpeeder.sh renewLic
# 更新许可

=========================================
提示错误：Kernel not be matched!You should change kernel manually, and try again!

出现这个错误，说明你的系统或内核 不满足LotServer的要求，建议使用 Debian 7 x64 系统，此系统内核大多默认都满足要求。

更换内核教程可以参考：Debian/Ubuntu 内核降级教程 —— 降低(BBR)为支持锐速的内核版本

提示错误：I can not find the server pubilc Ethernet!
------------------------------------------------------------------------------------
提示错误：I can not find the server pubilc Ethernet!

出现这个错误，说明你的系统没有安装 ifconfig ，这导致了 脚本无法获取网卡绑定的IP，一般是CentOS 7系统出现这个问题，安装这个工具后重新执行脚本即可。

yum -y install net-tools
