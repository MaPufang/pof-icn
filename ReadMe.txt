测试脚本位于pox/forwarding/，主要包括：
1、test_for_2PC      
   USTC交换机收到数据包后匹配DMAC后输出；
2、test_for_ipv6_3
   USTC交换机收到数据包匹配DMAC后删除MAC头并增加IPv6头输出；
3、test_for_ustc_loop
   USTC交换机通过自环测试封装、解封装隧道头工作功能；数据包流程如下：10043 input(pc) ---VxLanEncap--> 10045 output(switch) ->10049 input(switch) ---VxLanDecap---> 10047 output(pc)         
4、test_for_cooperation_ustc
   配置用于三点联调时USTC交换机的流表，
5、test_for_cooperation
   根据dpid号分别配置用于三点联调时USTC、NC、IOA交换机的流表
6、test_for_cooperation_loop
   构建环路：USTC-->IOA--->NC--->USTC，根据dpid号分别配置用于三交换机的流表点，使USTC发的到都到IOA，IOA的包都经过NC，NC的包都到USTC。
   

注意：
该版本与之前版本比较，有以下不同点：
1)接收到PORT_STATUS、RESOURCE_REPORT的消息顺序不同，该版本先收到PORT_STATUS然后收到RESOURCE_REPORT，之前版本反之。
2)之前版本由交换机发送ECHO_REQUEST，控制器响应ECHO_REPLY。该版本利用定时器每1s发送ECHO_REQUEST给交换机，交换机响应ECHO_REPLY。
3)之前版本会默认开通所有端口的pof_enable,该版本只在脚本里开启部分端口的pof_enable。
