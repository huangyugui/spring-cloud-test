# 需要开启的服务
- service-config-center
- serice
- consumer
- api-gateway

# 关于服务网关
- 由于服务是无状态的，但是为了保障对外服务的安全，同时为了不至于权限控制污染整个服务，因此需要额外的对接口访问的控制处理
- 这一层在Open Service 和  Service 之间


									外部调用方
										|
								   	   负载均衡
							/		  	|		    \						   Git
					Open service		open service			open service				|
						|	   \		/	|		\		/	|					|
	 eureka Service--		|	 	\/		|		  \	  /		|			---Config Service
						|	  /	  \		|		/	\		|
					service			  service			service
				
				
				
				
				
				
								   