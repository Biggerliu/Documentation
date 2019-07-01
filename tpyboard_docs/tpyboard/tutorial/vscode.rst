ʹ��Visual Studio Code����MicroPython���
===============================================

Visual Studio Code(���¼��VSCode)��һ��������ǿ��Ŀ�ƽ̨��Դ����༭����IDE����֧��Windows��OS 
X��Linux������JavaScript��TypeScript��Node.js֧�֣�����ӵ�зḻ�Ĳ����̬ϵͳ����ͨ����װ�����֧�� 
C++��C#��Python��PHP���������ԡ�

׼������
------------------
 - **TPYBoard v102 һ��**
 - **�ɷ��������Windowsϵͳ�ĵ��ԣ�������win10Ϊ����**
 - **�Ѱ�װVSCode�༭��**

*VSCode����ص�ַ*

������ַ `https://code.visualstudio.com/ <https://code.visualstudio.com/>`_

GitHub��ַ `https://github.com/Microsoft/vscode <https://github.com/Microsoft/vscode>`_

VSCode IDE���� `https://code.visualstudio.com/?wt.mc_id=vscom_downloads <https://code.visualstudio.com/?wt.mc_id=vscom_downloads>`_


��װPycom���
---------------------------

Pycom�����Ҫnode.js�����������Ҫ��װnode.js��`���ص�ַ <https://nodejs.org/en/>`_
��װ��ɺ�ͨ��CMD����鿴node�汾����ȷ���Ƿ�װ�ɹ���

.. code-block::c

    node -v
    
.. image:: img/1cmd.png

��VSCode��������˵��� *Extensions* ��չͼ�꣬�������������档

.. image:: img/vs1.png

���� *Pymakr* ������ز����������� *Install* ���а�װ��

.. image:: img/vs1.gif

��װ��Ϻ󣬹ر�VSCode����TPYBoard v102������ԣ��豸��������ȷ���Ƿ��ѳɹ����ض˿ڡ�

.. image:: img/vs2.png

Ĭ�ϻ��Զ��� *pymakr.json* �����ļ���������Ҫ�����޸ġ��������Ŀ���̨Ҳ�������Ӱ��ӵ�REPL�˿ڡ�

.. image:: img/vs3.png

�������������ļ���Щ��������Ҫ�Ĳ��֡�*pymakr.json* �����ļ��������£�

.. code-block::c

    {
    "address": "COM19",
    "username": "micro",
    "password": "python",
    "sync_folder": "/flash",
    "open_on_start": false,
    "sync_file_types": "py,txt,log,json,xml,html,js,css,mpy",
    "ctrl_c_on_connect": false,
    }

Pycom�����https://marketplace.visualstudio.com/items?itemName=dphans.micropython-ide-vscode

���ʹ��
---------------

ÿ������VSCodeʱPycom Console�����Զ��򿪲�ȥ���������õĶ˿ڡ�

.. image:: img/vs4.png

��ʱ�����Ͽ��������Զ����ӡ�REPL������PuTTY�÷�һ����CTRL+C��ֹͣ���г��� CTRL+D���������г�����λ����

.. image:: img/vs5.png

��������˵�����ļ����ع��ܵ�ʹ�÷��������ȣ���VSCode������Դ�������½�һ��Ŀ¼����һ�����̣��½�һ��main.py�ļ���

.. image:: img/vs6.gif

дһ�μ򵥵Ŀ��ư���LED�ĳ������ڲ��ԡ���д����ʱ��VSCode����ʾ����������Ϊ�����Ǳ���û��pyb�⣬���Դ�����Ժ��ԣ���Ӱ�칦�ܡ�

.. code-block::python

    from pyb import LED
    
    for i in range(5):
        LED(4).toggle()
        print('-----',i,'-----')
        pyb.delay(350)

VSCode���ߵײ���ɫ�����й���Pycom����ļ�����ݹ��ܡ�

.. image:: img/vs7.png

- Pycom Console:�򿪻�ر�����ӵ�����

- Run�����е�ǰ�ļ�

- Upload���ϴ������ļ���������

- Download�����ذ�����Ĺ����ļ�

��� *Run* ���е�ǰ��main.py��ע����ֻ������һ����ѣ��������main.py��Ĵ���洢���������FLASH�С�

.. image:: img/vs8.gif

��� *Upload* ��main.py�ϴ���������ϴ���Ϻ���ӻ��Զ������������µĳ�����ʱ��������˿ڶϿ������������Զ����ӵġ�

.. image:: img/vs9.gif

��������һ�� *Download* �Ĺ��ܣ���������������㷢���������ļ����Ƿ�ֻ���ص�ǰ���ļ�����ȫ�����ء����������ʾ����Ϊ�����ﻹ��һ��boot.py�ļ���ѡ���Ǹ������ԣ���������ѡ��ȫ�����ء�

.. image:: img/vs10.gif

�������ִ����Ϻ����ӶϿ��˲�û���Զ������ϣ���������������ʾ **> Failed to connect (Error: Port is not open). Click here to try again.** ����ʱ����� *Pycom Console* �Ϳ����ˡ�

.. image:: img/vs11.gif

ʹ������
------------------------

������˵������ͦ����ģ����������ϴ��ļ����������ء�����ÿ�β����󣬶������һ��Ӳ����λ���˿ڶϿ����������о���̫�Ѻá���Ȼ������ʹ��micropython�е�ģ��ʱû�д�����ʾ��ȫ�ȹ��ܣ����ǿ���ȥ��װPython���������ʹ��Python�﷨ʱ��ȽϷ��㡣
 



