�ȴ������ݿ�:
```
simple
simple_crm
simple_erp
simple_sso
```
��ÿ�����ݿ���ִ��sqlĿ¼�¶�Ӧ��SQL�ű�  
ע��ʾ���е����ݿ�˿�����36902  
ע�ⰲװ���ݿ�ʱ,���ñ��������ִ�Сд
���Բο�  
http://qa.anyline.org/art/v?id=lv0182c99f6acebf1d2d680783bf1168e8f99eced8e0136a4ec1

    <!--
        Ϊ�˲������ݿ⣬��Ҫһ��AnylineService���󲿷ֲ���ͨ�����service�����

        ������Controller��ע��service
        @Qualifier("anyline.service") 
        private AnylineService service;

        ��ͨ���Ǽ̳����TemplateController
        org.anyboot.mvc.controller.impl.TemplateController

        �������󲿷ֲ���ͨ�����service����ɣ���
        DataSet set = service.querys("HR_USER");
        ���ص�DataSet���Դ��˳��õ���ѧ���㺯�� ��������ͣ���ȡ�������ֵ������ȥ�أ������Сֵ�������ϼ�������飬����ת������SQLɸѡ
    -->
    <module>anyline-simple-start</module>
    
    <!--������Դ�����-->
    <module>anyline-simple-ds</module>
    
    <!--�Խ�����Ĳ���-->
    <module>anyline-simple-result</module>
    
    <!--pdf����-->
    <module>anyline-simple-pdf</module>
    
    <!--������ʽ ��Ҫ������ȡ��ǩ ����ַ��� �����һ��html�г�ȡ���г�����-->
    <module>anyline-simple-regular</module>
    
    <!--���ֳ����Ĳ�ѯ-->
    <module>anyline-simple-query</module>
    
    <!--�������-->
    <module>anyline-simple-net</module>
    
    <!--word excel���� �ص�ʵ��word excel�еı������Լ�html/cssתword��ǩ-->
    <module>anyline-simple-office-excel</module>
    <module>anyline-simple-office-word</module>

ÿ��Ŀ¼����read˵����ʵ�ֵ�ʾ�������Է�ʽ��ע������