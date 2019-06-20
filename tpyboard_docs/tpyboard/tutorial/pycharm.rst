ǰ��
--------------

PyCharm����˵�ǵ��������е�һ��Python IDE�ˣ��󲿷ֹ���TPYBoard��С��鶼��ʹ��PyCharm��дMicroPython�ĳ����ź����ǣ�ֻ�ǰ�PyCharm������һ�ִ���༭����������Ȼ������Ҫ�����������������PuTTY����ʵ���Ҳ�в���С���ѯ��PyCharm����ô��װMicroPython��������⣬����������վҲȱ���ⲿ�ֵĽ̳̣�����ʵ��һ���ܽ��¾��鹲�����ң�Ҳ�ø�����MicroPython��С����ṩ������

׼������
------------

*Ӳ��Ҫ��*
 
 - **TPYBoard v102������ һ��**

*���Ի���Ҫ��*
 
 - **windowsϵͳ�����̳���win10Ϊ����**

 - **�Ѱ�װPython���������̳�Python 3.6.4��**

 - **�Ѱ�װPyCharm���**

 - **�ɽ�������**

PyCharm 2018רҵ�� ��װ�����ü���� `������� <http://old.tpyboard.com/download/tool/201.html>`_ ��


���ְ�װ
-------------------

**��װMicroPython���**

1. �򿪡�PyCharm��������Լ�����һ����Ŀ���˵��� *File => Settings => Plugins* ,���� *micropython* �������������ŵ�� *Search in repositories*���������MicroPython���ʱ��� *Install* ���а�װ����װ��Ϻ�����PyCharm�����

.. image:: img/install.gif


**����MicroPython���豸**

2. ��TPYBoard v102������ͨ��USB�����߽�������У�Ȼ��˵���  *File => Settings => Languager & Frameworks => MicroPython* ��ѡEnable MicroPython support��Device typeѡ��Pyboard��Device path���뿪�����Ӧ�Ķ˿ںţ�����COM19�����Apply����Ӧ�ã����OK�رնԻ���

.. image:: img/COM.gif


**REPL����**

2. ��װ�ǲ��Ǻܼ򵥣�����������һ�¡������ǰ��Ŀ�Ҽ�ѡ�񴴽�һ��Python File����������main����ʱ��PyCharm��ʾ����Ҫ����docopt���������װ����ʾ���󣬲鿴���������ͼ��

.. image:: img/m1.png

��û������������ģ������е�����3�������ƴ�����Ϣ�ٶȲ��ҽ���������ҵ���һ�����еķ������ǣ��ҵ�PyCharm�İ�װĿ¼�µ�packaging_tool.py�����޸ģ�packaging_tool.py��\JetBrains\PyCharm 2018.1\helpersĿ¼�¡���packaging_tool.py�ļ������޸ģ������ı��ĵ����׳������ҵ�do_install��do_uninstall������������������Ϣ���У�����Ϊ�������ݣ�

.. block-code:python

    def do_install(pkgs):
        try:
            try:
                from pip._internal import main
            except Exception:
                from pip import main
        except ImportError:
            error_no_pip()
        return main(['install'] + pkgs)


    def do_uninstall(pkgs):
        try:
            try:
                from pip._internal import main
            except Exception:
                from pip import main
        except ImportError:
            error_no_pip()
        return main(['uninstall', '-y'] + pkgs)

�޸ı�����ٵ㰲װ�ͺ��ˡ�

.. image:: img/m2.png


3. ��main.py�ļ����������µĴ��룬�ô���Ĺ��ܾ���ÿ��1�뷴ת��LED4��״̬ͬʱ���Hello�ַ���

.. block-code:python

    from pyb import LED

    LED4 = LED(4)

    while True:
        LED4.toggle()
        print('Hello')
        print('-------')
        pyb.delay(1000)


�������ʱ��ᷢ�֣�PyCharm����pybģ�鲢û�д���������ʾ�Ĺ��ܣ�������Ϊ��micropython�����û��ʵ�ֶ�pybģ���֧�֣������ò���Ѿ��������ļ����غ�REPL���ԵĹ��ܣ�Ҳ�Ǻ������Ĺ����ˡ��ò��Դ���Github��ַ��`https://github.com/vlasovskikh/intellij-micropython <https://github.com/vlasovskikh/intellij-micropython>`_ ��


4. ��д����󣬵��������Ͻ�ѡ�� *Flash main.py*������Աߵ���ɫ��ͷ�������У���д��main.py�ļ��ͻ����ص������������Ϻ���Զ����г�������·��ĵ���������ʾ�����Ϣ�����£�

.. image:: img/m3.png

.. image:: img/m4.png 

5. �˵��� *Tools => MicroPython => MicroPython REPL* ���Ե���REPL���Խ��棬ʹ�÷���ͬPuTTY��ÿ�ε���ʱ��������ֹͣ���г���

.. image:: img/m5.png

��ϸ�Ĳ����������£�

.. image:: img/repl.gif







