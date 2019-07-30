
如何初始化
1.部署OwnedUpgradeabilityProxy实例
2.部署逻辑合约的初始版本(V1)(OKUSDImplementation)
3.调用OwnedUpgradeabilityProxy实例来更新到初始版本的逻辑合约
4.调用初始化方法如果逻辑合约依赖自己的构造函数(constructor)来设置某个初始状态，那么在它和代理合约产生联系之后，之前的这些状态就要重新修改，因为代理合约的存储并不知道(逻辑合约里的)这些值。OwnedUpgradeabilityProxy有一个upgradeToAndCall方法专门来调用一些逻辑合约中的方法，一旦代理合约升级到最新版本时，就把连接到的那个逻辑合约里的初始设置重新设置一遍。

如何升级
1.部署一个新版本的逻辑合约(V2)，确保它继承了上一个版本里的状态变量结构。
2.调用ownedUpgradeabilityProxy实例来升级到新版本合约的地址。


先部署代理   再部署实现类    将实现类加入代理 初始化实现类   调用实现类Mint方法