# b4x20220302
B4X實驗:  打造 CCTV Server . MJPG-Streamer Server 串流服務器(B4J/B4A)
B4X實驗:  打造 CCTV Server . MJPG-Streamer Server 串流服務器(B4J/B4A)

參考資料:
http://albert-oma.blogspot.com/2012/07/jpegrtp.html Albert 的筆記本 很讚 
https://newgoodlooking.pixnet.net/blog/post/111175662


WireShark
https://www.wireshark.org/download.html




這里的 Boundary 可以是任意字符串，只要你覺得唯一并能區分即可，比如我可以設置為“--dennisgao”。
發送圖片數據

首先要保證，對一個HTTP連接只能發一次流頭，
后面 接連不斷的圖片數據。
A.表頭資料
HTTP/1.0 200 OK
Cache-Control: no-cache
Pragma: no-cache
Content-Type: multipart/x-mixed-replace; boundary=--myboundary
 
B.訊息資料
--myboundary
Content-Type:image/jpeg
Content-Length:27386


java.lang.RuntimeException: Object should first be initialized (B4XBitmap).
java.lang.ClassCastException: class anywheresoftware.b4a.objects.B4XCanvas cannot be cast to class anywheresoftware.b4a.ObjectWrapper (anywheresoftware.b4a.objects.B4XCanvas and anywheresoftware.b4a.ObjectWrapper are in unnamed module of loader 'app')
 

https://github.com/eric19740521/b4x20220302

