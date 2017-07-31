###Redis入门  

	1. Redis的模型：是基于内存的单进程单线程的KV数据库
		![](http://i.imgur.com/T4iTQ2F.png)
	2. Redis快的原因:   
		* 完全基于内存
		* 数据结构简单，对数据操作也简单
		* 使用多路I/O复用（多路指多个网络连接，复用指单个现成处理多个请求）  
	3. 追求轻巧：
		实现了对select，select、epoll、evport、kqueue这些通用的接口的实现。在不同的系统调用选用适合的接口，linux下默认是epoll。因为Libevent比较重更通用代码量也就很庞大，拥有很多Redis用不上的功能，Redis为了追求“轻巧”并且去除依赖，就选择自己去封装了一套。  
	4. 单进程单线程好处
		* 代码更清晰，处理逻辑更简单
		* 不用去考虑各种锁的问题，不存在加锁释放锁操作，没有因为可能出现死锁而导致的性能消耗
		* 不存在多进程或者多线程导致的切换而消耗CPU
	5. 单进程单线程弊端
		* 无法发挥多核CPU性能，不过可以通过在单机开多个Redis实例来完善；
	6. 其他一些优秀的开源软件采用的模型
		* 多进程单线程模型：Nginx
		* 单进程多线程模型：Memcached 
	7. Linux下的五种网络I/O
		* 阻塞 I/O（blocking IO）
		* 非阻塞 I/O（nonblocking IO）
        * I/O 多路复用（ IO multiplexing）
        * 信号驱动 I/O（ signal driven IO）
        * 异步 I/O（asynchronous IO）
	
	     
