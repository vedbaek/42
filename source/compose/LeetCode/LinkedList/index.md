# 链表

链表（Linked List）是一种常见的数据结构，它由一系列节点组成，每个节点包含两个部分：数据和指向下一个节点的指针。链表中每个节点的数据可以是任意类型，而指针则是一个变量，用于存储下一个节点的地址。

链表通常有两种类型：单向链表和双向链表。在单向链表中，每个节点指向下一个节点，最后一个节点则指向 NULL。而在双向链表中，每个节点同时指向前一个节点和后一个节点，即每个节点有两个指针。

相比于数组等线性结构，链表的插入和删除操作更为高效，因为只需要调整节点的指针即可，而不需要移动大量数据。但查找某个节点的时间复杂度为$O(n)$，因为需要从头开始遍历链表。

链表的优点包括：

- 可以动态地增加和删除节点，不需要预先知道节点数量。
- 内存空间可以灵活利用，不需要一块连续的内存空间。
- 插入和删除节点的时间复杂度为$O(1)$，相对数组等线性结构更为高效。

链表的缺点包括：

- 查找某个节点的时间复杂度为$O(n)$。
- 由于每个节点都需要一个额外的指针来指向下一个节点，因此空间复杂度比数组等线性结构更高。

链表是一种十分常见且实用的数据结构，它在许多算法和程序中都有广泛的应用。


## 相关问题

```{toctree}
:maxdepth: 1

lc142
```