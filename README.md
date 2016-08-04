# netty-protobuf-rpc#
Fork of netty-protobuf-rpc
#protoc +netty 的rpc实现,hadoop中hbaserpc实现#
1. 定义protoc  的service服务,request,response
2. service中有2个接口 一个interface 一个blockinginterface 分别是
异步和同步的接口, 异步接口中有回调方法,同步接口没有
3. 客户端实现channel 这个channel  有BlockingRpcChannel 和 rpcChannel 同接口一样 异步中有回调方法,chanal中实现callmethod  进行远程rpc调用
4. 在服务端进行服务的注册通过newReflectiveBlockingService 或者 newReflectiveService 进行服务的注册 监听服务并调用
