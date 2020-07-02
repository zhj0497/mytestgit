知识点整理:

spring相关的知识点:
    aop：https://www.cnblogs.com/zhangzongle/p/5944906.html
    
牛人的博客:
田小波
http://www.tianxiaobo.com/
活在梦里
https://www.cnblogs.com/micrari

redis的并发处理
while(jedis.setnx(lock, now+超时时间)==0）{
    if(now>jedis.get(lock) && now>jedis.getset(lock, now+超时时间)){
        break;
    }else{
        Thread.sleep(300);
    }
}
执行业务代码;
jedis.del(lock);

--打印java默认参数
-XX:+PrintFlagsFinal
--java 启动进程信息
jps -l
--运行时的参数
jinfo -flags pid
