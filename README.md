<img width="1386" alt="截屏2025-02-28 20 47 09" src="https://github.com/user-attachments/assets/85ffdd79-b480-4227-8281-911d8b66bee0" />

StoreModel(Models)商店模式：编排从视图到Web服务的数据流，要创建一个函数（需要使用Web服务或者某种HTTP客户端call因此我们要创建另一个Services组），访问服务，获取产品全部信息并分配我们想要的产品属性。此处可以创建WebServices依赖项

Product(Models)产品模型：结构体，只是携带数据。并且要Decodable(可解码），因为这将从我们收到的JSON数据解码到这个特定的模型中。

WebService(Services)Web服务：负责获取产品，先获取URL（否则报错）之后URL会话点共享点数据给出数据和反应，从而检查响应。一旦有了数据和响应，我们就可以解码数据（JSONDecoder）,返回数据拿给产品。最后返回产品。

ContentView(Models)内容视图：使用StoreMode进行调用即获取内容并显示它，调用前先注入
