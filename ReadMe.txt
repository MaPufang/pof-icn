���Խű�λ��pox/forwarding/����Ҫ������
1��test_for_2PC      
   USTC�������յ����ݰ���ƥ��DMAC�������
2��test_for_ipv6_3
   USTC�������յ����ݰ�ƥ��DMAC��ɾ��MACͷ������IPv6ͷ�����
3��test_for_ustc_loop
   USTC������ͨ���Ի����Է�װ�����װ���ͷ�������ܣ����ݰ��������£�10043 input(pc) ---VxLanEncap--> 10045 output(switch) ->10049 input(switch) ---VxLanDecap---> 10047 output(pc)         
4��test_for_cooperation_ustc
   ����������������ʱUSTC������������
5��test_for_cooperation
   ����dpid�ŷֱ�����������������ʱUSTC��NC��IOA������������
6��test_for_cooperation_loop
   ������·��USTC-->IOA--->NC--->USTC������dpid�ŷֱ�����������������������㣬ʹUSTC���ĵ�����IOA��IOA�İ�������NC��NC�İ�����USTC��
   

ע�⣺
�ð汾��֮ǰ�汾�Ƚϣ������²�ͬ�㣺
1)���յ�PORT_STATUS��RESOURCE_REPORT����Ϣ˳��ͬ���ð汾���յ�PORT_STATUSȻ���յ�RESOURCE_REPORT��֮ǰ�汾��֮��
2)֮ǰ�汾�ɽ���������ECHO_REQUEST����������ӦECHO_REPLY���ð汾���ö�ʱ��ÿ1s����ECHO_REQUEST������������������ӦECHO_REPLY��
3)֮ǰ�汾��Ĭ�Ͽ�ͨ���ж˿ڵ�pof_enable,�ð汾ֻ�ڽű��￪�����ֶ˿ڵ�pof_enable��
