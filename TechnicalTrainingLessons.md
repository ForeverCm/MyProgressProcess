##异步消息队列  
	

	1. 组成： Asynchronous Message Queue Server，Producer，Consumer，Delay Server 
	2. 特点： Producer  don't need to care about Consumer,
		     Consumer don't need to care about Producer
	3. 安全： need feedback Mechanisms  

##负载均衡器
	
	1. very important
	2. wide application  

##Redis

	1. very important  
	2. wide application


##一个系统的底层优化

	1. cpu： 缓存，剪枝，空间换时间，算法调整，并发，任务调度粒度
	2. Memory：对象池，去除冗余信息，选择更适合的数据模型，优化string类型  
		存储这块：数据量大，时效性高 - 分布式存储（Redis）
				 数据量大，时效性低 - 文件+MMF+LocalCache
				 数据量小 - 直接放入内存
	3. I/O: network card, disk

##一个硬币

	1. 一个硬币有两面
	2. 少了任何一面都不可称之为硬币了


##显示branche结构图  
	1. git log --graph --decorate --oneline --simplify-by-decoration --all  
	2. gitk --simplify-by-decoration --all


	
	
