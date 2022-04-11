# RBAC(基于角色的访问控制)


**RBAC (`Role-Based Access Control`)** 即基于角色的访问控制模型。

RBAC也就是需求发掘所用到的**Who**(角色)、**What**(拥有什么资源)、**How**(有哪些操作)。它们构成了访问权限三元组，即：Who对What进行How的操作。

-   **Who：** 是权限的拥有者或主体（如：User，Role）
-   **What：** 是操作或对象（operation，object）
-   **How：** 具体的权限（Privilege,正向授权与负向授权）


RBAC主要包含四个子模型：RBAC0、RBAC1、RBAC2和RBAC3，合起来叫做**RBAC96**。

-   **RBAC0：** 是RBAC的核心思想。
-   **RBAC1：** 是把RBAC的角色**分层模型**。
-   **RBAC2：** 增加了RBAC的**约束模型**。
-   **RBAC3：** 其实是RBAC1 + RBAC2。

<br/>

##  RBAC0模型
**RBAC0**是RBAC的核心，主要由四个部分组成：**用户**(User)、**角色**(Role)、**权限**(Permission)和**会话**(Session)，

这是一种多对多的分配关系：用户对应多个角色、角色对应多个权限。用户与会话一对一，会话与角色一对多。

![](https://raw.githubusercontent.com/hollson/pm/62692ff5cadca5743d1c87eaf680656a993ccd4e/RBAC/rbac0.svg)

<br/>

##  RBAC1模型
**RBAC1** 是在RBAC0模型基础之上增加了**角色分层**概念和角色之间的**继承关系**。  
- **一般继承：** 一般继承是一个“加法继承"(如：VIP会员=普通权限+VIP权限)，允许角色间的多继承。
- **受限继承：**: 受限继承是一个减法继承，它要求角色继承关系是一个树结构，实现角色间的单继承。


![](https://raw.githubusercontent.com/hollson/pm/62692ff5cadca5743d1c87eaf680656a993ccd4e/RBAC/rbac1.svg)


<br/>

# RBAC2模型
**RBAC2** 是在RBAC0模型基础之上引入了**静态职责分离**(SSD)与**动态职责分离**(DSD)概念和角色之间的**继承关系**。


静态职责分离：

-   **互斥角色：** 同一个用户不能授予互斥关系的多个角色，如：不能同时授予**会计**与**审计**角色。

- **基数约束：**
    一个角色对应的访问权限数量应该是受限的；
    一个角色中用户的数量应该是受限的；
    一个用户拥有的角色数量应该是受限的；
    
- **先决条件角色：** 用户想拥有A角色就必须先拥有B角色，从而保证用户拥有X权限的前提是拥有 Y 权限。
    例如：**金牌会员**角色只能授予拥有**银牌会员**角色的用户。
    
    
动态责任分离：

-   用户登录系统后动态决定用户的角色。如：XX直聘(同一账户)登录后才能分配**应聘者**或是**招聘者**角色；
再如OA审批中动态分配**申请者**和**审批人**角色。


![img](https://raw.githubusercontent.com/hollson/pm/62692ff5cadca5743d1c87eaf680656a993ccd4e/RBAC/rbac2.svg)


<br/>

## RBAC3模型
**RBAC3** 是集聚了RBAC1和RBAC2的全部特点，即 **RBAC3=RBAC1+RBAC2** 。

![img](https://raw.githubusercontent.com/hollson/pm/62692ff5cadca5743d1c87eaf680656a993ccd4e/RBAC/rbac3.svg)


<br/>

## RBAC示例

![img](https://raw.githubusercontent.com/hollson/pm/62692ff5cadca5743d1c87eaf680656a993ccd4e/RBAC/rbac_eg1.svg)

<br/>

![img](https://raw.githubusercontent.com/hollson/pm/62692ff5cadca5743d1c87eaf680656a993ccd4e/RBAC/rbac_eg2.svg)



## 参考链接

https://www.sojson.com/blog/141.html

