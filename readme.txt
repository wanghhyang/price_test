���㹦��˵��

1-Design
�����������������˵�����ֲ�ṹ��������ù�ϵ


2-Common
������������и�����Թ��õĻ�����������������ࡣ
����
AOP     ��һ���������㣬���ڸ����ģ�����־��¼�Ĵ����װ�������㣺Common��Logger
Caching ��һ������㣬����redis���м����װ�����ػ������Ĵ��������㣺Common��Logger
Common  ��һ��Helper��Ĳ㡣������Ҫ�����һЩ���ô��������Էŵ����㡣�����㣺Logger
Logger  ��һ����־�����ܲ㣬������һЩ������־��¼�İ����ࡣ�����㣺Common
MQ      ��һ����Ϣ����װ��Ϣ����Լ���Ϣ����İ��������ࡣ�����㣺Common��Logger


3-DataAccess
���ݷ��ʲ㣬ʹ��JnsFramework���ݿ��м����ɶ����ݿ�ķ��ʡ�
����
BLL��  ��ҵ���߼�����㡣��Ҫ�Ƕ�DAL��ĵ��ã��Լ���Core��Ľ�һ������������Ҫ���Բ����ñ��㡣�����㣺DAL��Common��Logger
DAL��  �����ݿ���ʲ㡣��Ҫ����sql����ִ�С������㣺Common��Logger
JnsBLL
JnsDAL


4-Entity
ʵ���ࡢ���ݿ�Ͷ���ӳ����
DTO     ��һ�����ݿ�洢��Ҫʵ����
Entity  ��һ���û�����ʹ�õ�ʵ����
JnsDict
JnsModel


5-Core
������ҵ���߼������Ψһ��Ԫ�����е�ҵ����Ҫ�ŵ�����ȥ��
Core��          �Ǵ���ϵͳ�Ϸǲ�ѯ��ҵ���߼��������㣺BLL��AOP��Caching��Common��Logger��MQ��ServiceProxy
Query��         �Ǵ���ϵͳ�ϲ�ѯ��Ҫ��ҵ���߼��������㣺BLL��Caching��Common��Logger��ServiceProxy
ServiceProxy��  ���ⲿ�ӿڵ����ò�


6-Service
�Ĳ��Ƿ���ӿڵĽӿڶ����
ApiService��  �Ƿ���ӿڶ���㡣�����㣺Core��Query
JobService��  ��Schedule���ýӿڲ㡣�����㣺Core��Query


7-StartUp
ϵͳ����㣬�û�������
JobHost��         ��Job�����������
MQConsumerHost��  ����Ϣ���Ѷ˵�����������
ServiceHost��     �ǽӿڷ����������
Web��             �Ǽ۸�ϵͳ���û�������


8-UnitTests
��Ԫ���Բ�
CommonTest��      �ǻ�������ĵ�Ԫ���Բ㣬2-Common������Ҫ���Ե����б�д��Ҫ�ŵ�����
CoreTest��        ��ҵ���߼��ĵ�Ԫ���Բ㣬5-Core������Ҫ���Ե����б�д��Ҫ�ŵ�����
DataAccessTest��  �����ݷ��ʵĵ�Ԫ���Բ㣬3-DataAccess������Ҫ���Ե����б�д��Ҫ�ŵ�����
Service��         �Ƿ���ĵ�Ԫ���Բ㣬6-Service������Ҫ���Եı�д��Ҫ�ŵ�����