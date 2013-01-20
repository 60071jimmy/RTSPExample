RTSPExample
=====================

�y�z
=
> ���{���D��**��j�j�� 2012�Ĥ@�Ǵ� [�p�������]�����@�~**�A
> ���{���ޥ�Emgu CV���v�� GPL v3 �C
> 

�{���ݨD
-
- Microsoft Windows7 x64
- Microsoft Visual Studio 2008
- Emgu CV x64

���d�ұM�ץ]�t�H�UC#�{���d��
-
- Emgu CV (�v���^��)
- Jpge ���Y
- Async TCP 
- Async UDP

�M�׻���
-
- Emgu.CV (Emgu CV��l�X)
- Emgu.Util (Emgu CV��l�X)
- HelloWorld (Emgu CV��l�X �i����Emgu CV�O�_���`�B�@)
- VideoTest (�i����Emgu CV�O�_�i���`�^���v��)
- VideoServer (RTSP���A��)
- VideoClient (RTSP�Ȥ��)


�{���[�c
-
[![�{���[�c][structure]][structure]

���󻡩�
-
**�@�Ϊ���**

- RTPModel 
 - RTPModel class <-> rtp packet byte array �ഫ 
- FrameHelper 
 - Bitmap class <-> jpge byte array �ഫ 
- SockHelper
 - Async TCP �P Async UDP ����


**���A����**

- VideoCache
 - �NVideoFile �ন RTP�ʥ] byte�s��
- RTPPlayer
 - �t�d�o�eRTP�ʥ]�P�x�s���񪬺A
- RTSPServer
 - �t�d�B�zClient TCP��RTSP Rquest �ñ���RTPPlayer

**�Ȥ��**

- ClientPlayer
 - �t�d�B�z�����쪺UDP�ʥ]���নImage�s��iQueue
- RTSPClient
 - �t�d�x�sRTSP���A�BRTSP Rquest�o�e�PRTSP Response�B�z

�}�o�y�{
-
**FrameHelper.cs���g**

1. �������v���v���^���ʧ@�A�ݤ����N�v�����v�洣���X�Ӧ�C#����ϥ�
2. �A�NC#�����নjpge�榡 byte array �榡�ϥ�
3. �A�Nbyte array�ݨϧ_����^Image����A����UI�ϥ�
4. ��ӵo�{UDP�ʥ]�̤j�u���65535�j�p�A�ҥH�S�[�J�F���Yjpge15%�~��{���X�i�h�C

**RTPModel.cs���g**

1. ���ձNjpge byte�নRTP�ʥ]���p
2. ���Nbyte array�নparse ��RTPModel���oplayload
3. �o�{���Ǧa��|�����쪺���p�o�ͻݽվ�timestemp�Pseq���פj�p

**SockHelper.cs���g**

1. �ϥ�asyc�覡���g�A���e���ϥ�multithread���gsocket�A�令�o�˼g�{���X��²�h�F

**VideoServer�PVideoClient ���g**

1. ������RTP��V�ǿ�A������`����server�o�eRTP�ʥ]��client����A��������VideoCache�BRTPPlayer
2. ����RSTP Request�PResponse�ʧ@�AServer���N�s��h��VideoCache�PRTPPlayer�A�ë��򼽩�w�s�b��RTPPlayer�ʥ]�AClient�ݫإ�UDP�����ݫ�ARequest SETUP���oSessions�A��i����v���ʧ@�AServer����Request��ݨ̷�SessionID��RTPPlayer������A�æ^��Response�A��������RTSPServer�BRTSPClient

�ѦҤ��m
=====================
- [RTSP��w] 
- [RTP��w]
- [Emgu CV]

[RTSP��w]: http://en.wikipedia.org/wiki/Real_Time_Streaming_Protocol
[RTP��w]: http://en.wikipedia.org/wiki/Real-time_Transport_Protocol
[Emgu CV]: http://sourceforge.net/projects/emgucv/
[structure]: https://raw.github.com/fajoy/RTSPExample/master/structure.png