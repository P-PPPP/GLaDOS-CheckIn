# Glados-Checkin
The Easiest Way To Check Glados In 👍. | 最简单的Glados_Checkin方式  | 请勿用于Github Actions(大概率ban)  
- 多用户
- 可外部调用
- 可推送Server酱
### 你需要准备
- 你的Glados Cookie
- 你的Server酱Key (如果你要推送的话)
### 使用方式
1. Clone/Download本项目  
2. `pip install -r requirements.txt`安装依赖库  
3. 把自己的信息扔到`Config.json`里面  
4. 如果想改变每天签到时间的话,将`main.py`中的`schedule.every().day.at("01:20").do(Check)`里面改成你想要的任意时间  
5. 运行`python main.py`,搞定  

或注册云函数(请在符合云服务主机和云服务商的规定下使用)，上传本项目代码即可，入口为`index.py`
###### 外部调用
把`Checkin.py`扔到你的项目中然后`import Checkin as Glados_Checkin`即可。  
之后通过`Glados_Checkin.Checkin(Cookie)`调用即可,会返回官方返回的Json信息,自行解析即可  
如果想格式化信息并推送到server酱,调用`Glados_Checkin.SendServerChain(ServerChainKey,OfficialCallback)`即可  