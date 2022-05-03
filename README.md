# -Promise
## 实现过程
1、new Promise2时执行constructor函数，将new Promise2中的函数作为参数传给fn，constructor函数中执行fn，并将其中resolve、reject传递到函数中。fn执行过程创建xhr对象然后发送请求
，做好这些fn执行结束返回promise对象，即getWeather函数得到一个promise对象后执行then函数。  
2、reject函数执行时在定时器中将状态赋值为rejected并执行this.succeed函数，reject函数执行时同理。  
3、rejct未执行时，then已经执行完了，此时的succeed及fail已经赋值完成了。
