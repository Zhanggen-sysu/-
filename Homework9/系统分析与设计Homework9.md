使用 **UMLet** 建模

- 1、使用类图，分别对 Asg_RH 文档中 Make Reservation 用例以及 Payment 用例开展领域建模。然后，根据上述模型，给出建议的数据表以及主要字段，特别是主键和外键
  - 注意事项：
    - 对象必须是名词、特别是技术名词、报表、描述类的处理；
    - 关联必须有多重性、部分有名称与导航方向
    - 属性要注意计算字段

  - 数据建模，为了简化描述仅需要给出表清单，例如：

    - Hotel（ID/Key，Name，LoctionID/Fkey，Address…..）

    Make Reservation:

    ![hw9_1](https://github.com/Zhanggen-sysu/Software-Analysis-Design-Homework/raw/master/Homework9/hw9_1.png)

    Rome-Catalog(ID/Key, type)

    Room-Description(ID/Key, type, totals, list-price, description)

    Room(ID/Key, type, date, /isAvailable, reserved, totals, /price)

    Hotel(ID/Key, name, stars, address, loc-code, brief-intro, /favorite, /lowest price, /rating, /max-discount)

    Reservation(ID/Key, date, time, check in date, number of nights )

    Reservation Item(ID/Key, type, date, time, check in date, number of nights, adult, number, children number, children age)

    

    Payment

    ![hw9_2](https://github.com/Zhanggen-sysu/Software-Analysis-Design-Homework/raw/master/Homework9/hw9_2.png)

    Reservation(ID/Key, date, time, check in date, number of nights )

    Reservation Item(ID/Key, type, date, time, check in date, number of nights, adult, number, children number, children age)

    payment(ID/Key, total cost)

    credit card(ID/Key, type, /isAcceptable, card number, card security code, expiry date)

    card holder(ID/Key, title, first name, last name, address, city, country/state, country, postcode, daytime telephone, evening telephone, email)
- 2、使用 UML State Model，对每个订单对象生命周期建模
  - 建模对象： 参考 Asg_RH 文档， 对 Reservation/Order 对象建模。
  - 建模要求： 参考练习不能提供足够信息帮助你对订单对象建模，请参考现在 定旅馆 的旅游网站，尽可能分析围绕订单发生的各种情况，直到订单通过销售事件（柜台销售）结束订单。

![hw9_3](https://github.com/Zhanggen-sysu/Software-Analysis-Design-Homework/raw/master/Homework9/hw9_3.png)

