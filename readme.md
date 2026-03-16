**利用AI的学习prompt:**

简单的lecture notes：

```bash
我是香港科技大学的学生，我正在上一门课。我需要你先阅读这份讲义。接着我会一张slide一张slide把讲义传给你，我需要你以初学者的角度向我逐句讲解slide里面的内容(你的回答的重点focus)，确保我能准确的理解和学习到slide内容。你还要向我(浅浅地解释下)：解释slide的上下文逻辑关系，evalaution of concept，和provide exmaple for concept for understanding，以及解释为什么这个concept/example会出现在这里(老师为什么把这个content/exmaple/concept/表格放在这个地方教我们？）。```

难道中等的lecture notes：

```bash
我是香港科技大学的学生，我正在上一门课。我需要你先阅读这份讲义。接着我会一张slide一张slide把讲义传给你，我需要你以初学者的角度向我逐句讲解slide里面的内容(你的回答的重点focus)，确保我能准确的理解和学习到slide内容。你还要向我(浅浅地解释下)：解释slide的上下文逻辑关系，evalaution of concept，和provide exmaple for concept for understanding，以及解释为什么这个concept/example会出现在这里(老师为什么把这个content/exmaple/concept/表格放在这个地方教我们？）。如果我特别specify，就不需要逐句解释，需要从高层次的角度帮我解释和理解concept。```

较复杂，数学/计算机有关的lecture notes:

```bash
我是香港科技大学的学生，我正在上一门课。我需要你先阅读这份讲义。接着我会一张slide一张slide把讲义传给你，我需要你以初学者的角度向我逐句讲解slide里面的内容，确保我能准确的理解和学习到slide内容。你还要向我：解释slide的上下文逻辑关系，evalaution of concept，和provide exmaple for concept for understanding，以及解释为什么这个concept/example会出现在这里(老师为什么把这个content/exmaple/concept/表格放在这个地方教我们？）。如果我特别specify，就不需要逐句解释，需要从高层次的角度帮我解释和理解concept。对于如果你觉得对于初学者特别复杂/抽象的概念，请你为每个复杂/抽象的概念提供一个intutition，以及an appropriate example帮助我理解。```


具体的用法：

用法：prompt +整个ppt slide丢进去，然后一页一页slide截图/ 一张一张slide的文字[....copy 一张slide里面的所有文字...] (更推荐，更快) 丢进去给它解释

Note:一个窗口的AI对话最多支持~40 page的教学，超过这个page数量建议开新窗口
Note:推荐使用claude系列模型
