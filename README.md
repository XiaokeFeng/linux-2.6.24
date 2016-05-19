# Concept for "Professional Linux Architecture"
> by fengxiaoke at 2016-05-19 14:20

## Content
* [进程管理](#process)
* [内存管理](#memory)
    * [内存组织](#memory_modle)
    * [内存节点](#pglist_data)
    * [内存域](#zone)
    * [内存域水印](#watermask)
    * [冷热页](#hot_cold_page)
    * [页帧](#page)
* [文件系统](#file)
* [网络](#network)

<h2 id="process">进程管理</h2>

> coming soon ...
> * PID
> * fork/clone
> * process schedule

<h2 id="memory">内存管理</h2>

<h3 id="memory_modle">内存组织</h3>
* UMA
* NUMA

<h3 id="pglist_data">内存节点</h3>
* `struct pglist_data`
* 在UMA和NUMA中有区别吗？
* 一个节点连接一个CPU？

<h3 id="zone">内存域</h3>
* `struct zone`
* ZONE的类型？

<h3 id="watermask">内存域水印</h3>
* 什么是watermask？
* 什么是min_free_kbytes？
* pages_{min, low, high}有什么区别？
* lowmem_reserve是什么？

<h3 id="hot_cold_page">冷热页</h3>
* `struct per_cpu_pageset`
* batch？

<h3 id="page">页帧</h3>
* `struct page`
* 为什么page越小越好？
* 内核的一些模块会用到page中的一部分，但是剩余部分仅对其他模块有用，如何解决这种资源的利用问题？
* 什么时候可以换出一个page？

<h2 id="file">文件系统</h2>

> @todo

<h2 id="network">网络</h2>

> @todo


