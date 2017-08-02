###C#学习
	
	* C#参数参数类型约束
		> where T : struct     | T必须是一个结构类型
		> where T : class      | T必须是一个Class类型
		> where T : new()      | T必须要有一个无参构造函数
		> where T : NameOfBaseClass | T必须继承名为NameOfBaseClass的类
		> where T : NameOfInterface | T必须实现名为NameOfInterface的接口
	
		