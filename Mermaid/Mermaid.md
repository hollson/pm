[TOC]


##  流程图 


```mermaid
flowchart TD
A[Hard] -->|Text| B(Round)
B --> C{Decision}
C -->|One| D[Result 1]
C -->|Two| E[Result 2]
```
```mermaid
graph TD
A[图形] -->|开始| B(圆角)
B --> C{判断}
C -->|dddd| D[结果1]
C --> E[结果2]
F[竖向流程图]
```


```mermaid
graph LR
A[方形] --> B(圆角)
B --> C{条件a}
C --> |a=1| D[结果1]
C --> |a=2| D[结果2]
F[横向流程图]
```
```mermaid
flowchart LR
A[Hard] -->|Text| B(Round)
B --> C{Decision}
C -->|One| D[Result 1]
C -->|Two| E[Result 2]
```





## 时序图

```
sequenceDiagram
Alice->>John: Hello John, how are you?
loop Healthcheck
    John->>John: Fight against hypochondria
end
Note right of John: Rational thoughts!
John-->>Alice: Great!
John->>Bob: How about you?
Bob-->>John: Jolly good!
```
```mermaid
sequenceDiagram
Alice->>John: Hello John, how are you?
loop Healthcheck
    John->>John: Fight against hypochondria
end
Note right of John: Rational thoughts!
John-->>Alice: Great!
John->>Bob: How about you?
Bob-->>John: Jolly good!
```



```mermaid
gantt
    section Section
    Completed :done,    des1, 2014-01-06,2014-01-08
    Active        :active,  des2, 2014-01-07, 3d
    Parallel 1   :         des3, after des1, 1d
    Parallel 2   :         des4, after des1, 1d
    Parallel 3   :         des5, after des3, 1d
    Parallel 4   :         des6, after des4, 1d
```


## 甘特图

```mermaid
gantt
title 甘特图
dateFormat YYYY-MM-DD
section 行1
任务1 :a1, 2014-01-01, 30d
任务2 :after a1 , 20d
section 行2
任务3 :2014-01-12 , 12d
任务4 : 24d
```
```mermaid
%% 语法示例
gantt
dateFormat YYYY-MM-DD
title 软件开发甘特图
section 设计
需求:done,des1,2020-01-01,2020-01-05
原型:active,des2,2020-01-06,3d
UI设计:des3,after des2,5d
未来任务:des4,after des3,5d
section 开发
学习准备理解需求:crit,done,2020-01-01,24h
设计框架:crit,done,after des2,2d
开发:crit,active,3d
未来任务:crit,5d
耍:2d
section 测试
功能测试:active,a1,after des3,3d
压力测试:after a1,20h
测试报告:48h
```


## 类图
``` mermaid
classDiagram
Class01 <|-- AveryLongClass : Cool
Class03 *-- Class04
Class05 o-- Class06
Class07 .. Class08
Class09 --> C2 : Where am i?
Class09 --* C3
Class09 --|> Class07
Class07 : equals()
Class07 : Object[] elementData
Class01 : size()
Class01 : int chimp
Class01 : int gorilla
Class08 <--> C2: Cool label
```
```mermaid
classDiagram
Class01 <|-- AveryLongClass : Cool
<<Interface>> Class01
Class09 --> C2 : Where am i?
Class09 --* C3
Class09 --|> Class07
Class07 : equals()
Class07 : Object[] elementData
Class01 : size()
Class01 : int chimp
Class01 : int gorilla
class Class10 {
  <<service>>
  int id
  size()
}
```

```mermaid
 classDiagram
      Animal <|-- Duck
      Animal <|-- Fish
      Animal <|-- Zebra
      Animal : +int age
      Animal : +String gender
      Animal: +isMammal()
      Animal: +mate()
      class Duck{
          +String beakColor
          +swim()
          +quack()
      }
      class Fish{
          -int sizeInFeet
          -canEat()
      }
      class Zebra{
          +bool is_wild
          +run()
      }

```

## 状态图 

```
stateDiagram-v2
[*] --> Still
Still --> [*]
Still --> Moving
Moving --> Still
Moving --> Crash
Crash --> [*]
```
```mermaid
stateDiagram-v2
[*] --> Still
Still --> [*]
Still --> Moving
Moving --> Still
Moving --> Crash
Crash --> [*]
```

## 饼图

```mermaid
pie
"Dogs" : 386
"Cats" : 85
"Rats" : 15
```

## Git图

```mermaid
gitGraph:
options
{
    "nodeSpacing": 150,
    "nodeRadius": 10
}
end
commit
branch newbranch
checkout newbranch
commit
commit
checkout master
commit
commit
merge newbranch
```



## 用户体验旅程图 

```
  journey
    title My working day
    section Go to work
      Make tea: 5: Me
      Go upstairs: 3: Me
      Do work: 1: Me, Cat
    section Go home
      Go downstairs: 5: Me
      Sit down: 3: Me
```
```mermaid
  journey
    title My working day
    section Go to work
      Make tea: 5: Me
      Go upstairs: 3: Me
      Do work: 1: Me, Cat
    section Go home
      Go downstairs: 5: Me
      Sit down: 3: Me
```




---

>   *Mermaid 是由 Knut Sveidqvist 创建，它为了更简单的文档编写而生。*

https://www.cnblogs.com/xdy-/p/13402709.html