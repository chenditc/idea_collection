## 可引用的文档系统

## 痛点
文档在记录内容的时候，往往承载了一些通用知识和一些场景特定的知识。例如如何部署 xxx，其中可能会设计 “如何安装 docker”。而根据阅读者的能力不同，有些信息是需要深入阅读的，有些信息是不需要那么详细的。

此时文档的管理和阅读就会遇到几个困境：
1. 如果事无巨细地记录在一个文档里：那就会导致文档过于冗长，且文档之间重复内容过多。例如每个部署文档可能都会复述 “如何安装 docker”。且如果 “如何安装 docker” 的信息需要更新，需要更新多个文档。
2. 如果把子步骤拆出来，作为单独的文档，在其他文档中贴上链接：那就会导致一个文档的跳转次数过多，为了了解如何部署xxx，需要阅读 “如何安装 docker” ，“如何配置权限” 等等，而没有阅读过的人也不确定这些引用文档中有没有重要信息，所以往往会都看一遍，或者都不看。

## 问题以及解决方案
这个问题和代码中的 “高内聚” “低耦合” “可复用” 是很像的。可以考虑用类似代码的方式来解决。即一个文档解决好一个问题，把一个问题说清楚，在其他文档中引用该文档，通过传参的方式只显示最重要的部分。

例如 “如何安装 docker” 会写好在不同平台上如何安装，而引用它的文档可以一键插入，并通过参数调节显示或者不显示哪一部分的内容。
