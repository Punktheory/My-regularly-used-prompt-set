## 满分AI prompt调用

前言：日常生活裏面，我們經常會使用到一些AI工具辅助我们学习或者做project。为了最大化利用LLM AI tool, 一个良好，格式化，有明确目标的prompt是必不可失的。由于笔者经常使用AI工具帮忙，并且有心理学知识背景，于是我*总结出来一套我日常比较多使用，对于学生而言十分有用的prompt template*。下面的template主要针对在国际化大学学习的学生（lecture notes以英文为标准但是母语为中文）。如有需要，也可以进行客制化更改，调成更符合个人习惯或者地区习惯的prompt。  
  <br>

***
### 利用AI的學習prompt:

Easy lecture notes：

```bash
我是香港科技大学的学生，我正在上一门课。我需要你先阅读这份讲义。接着我会一张slide一张slide把讲义传给你，我需要你以初学者的角度向我逐句讲解slide里面的内容(你的回答的重点focus)，确保我能准确的理解和学习到slide内容。你还要向我(浅浅地解释下)：解释slide的上下文逻辑关系，evalaution of concept，和provide exmaple for concept for understanding，以及解释为什么这个concept/example会出现在这里(老师为什么把这个content/exmaple/concept/表格放在这个地方教我们？）。
```

Meddile-level difficulty lecture notes：

```bash
我是香港科技大学的学生，我正在上一门课。我需要你先阅读这份讲义。接着我会一张slide一张slide把讲义传给你，我需要你以初学者的角度向我逐句讲解slide里面的内容(你的回答的重点focus)，确保我能准确的理解和学习到slide内容。你还要向我(浅浅地解释下)：解释slide的上下文逻辑关系，evalaution of concept，和provide exmaple for concept for understanding，以及解释为什么这个concept/example会出现在这里(老师为什么把这个content/exmaple/concept/表格放在这个地方教我们？）。如果我特别specify，就不需要逐句解释，需要从高层次的角度帮我解释和理解concept。
```

complex, cs/math related lecture notes:

```bash
我是香港科技大学的学生，我正在上一门课。我需要你先阅读这份讲义。接着我会一张slide一张slide把讲义传给你，我需要你以初学者的角度向我逐句讲解slide里面的内容，确保我能准确的理解和学习到slide内容。你还要向我：解释slide的上下文逻辑关系，evalaution of concept，和provide exmaple for concept for understanding，以及解释为什么这个concept/example会出现在这里(老师为什么把这个content/exmaple/concept/表格放在这个地方教我们？）。如果我特别specify，就不需要逐句解释，需要从高层次的角度帮我解释和理解concept。对于如果你觉得对于初学者特别复杂/抽象的概念，请你为每个复杂/抽象的概念提供一个intutition，以及an appropriate example帮助我理解。
```
  
具体的用法：

>使用方法：prompt +整个ppt slide丢进去，然后一页一页slide截图/ 一张一张slide的文字[....copy 一张slide里面的所有文字...] (更推荐，更快) 丢进去给它解释

Note:一个窗口的AI对话最多支持~40 page的教学，超过这个page数量建议开新窗口  
Note:推荐使用claude系列模型

  <br>
  <br>  

***

### 利用AI做功课的prompt:

AI的使用，自然离不开 ~~帮忙做功课~~ 辅助完成作业。然而，想要让AI给出一份符合lecture notes规范的，符合学者知识水平的，以及不会过于死板的答案，也是一门学问。以下是一些可以参考的方法：

```bash
我现在正在做一份[Subject_name]的作业，我的终极任务是需要你协助我完成这份作业。现在你先详细地阅读我附上的几个lecture notes，掌握核心要点和教学内容，以明白我上课所学过的内容（明白我所该掌握的知识和我的知识水平），以及我的学校的教学风格。之后帮我做的作业要以这些slide为准。
```

>以上的prompt附上所有相关的lecture notes，和作业guidance,全部丢进去给AI

```bash
现在，我需要你帮我完成这份作业，请帮我以[您需要这份功课的output格式，例如可以是word，可以是代码] output这份作业的答案出来，一题一题来。做作业有以下规矩：1. Your answers should be typed, not handwritten。2. 同时，我要求你写出来的答案要相似人写出来的，不能有ai感，例如变量名字不能太公式化让人看得出来一眼AI，代码逻辑不能太完美不然有ai感，代码comment要有人写出来的感觉（比如说不是那么optimize，但是还是要保证正确），偶尔要有词语错别字(很少）模仿人常见的拼写错误，和标点符号例如句号要偶尔忘记加上去。3. 写出的答案例如写出来的文章或者数学计算要是严谨的，必须经得起反复验证的。现在，先做第一题，用英文回答。[^以上是针对计算机作业的一些要求，你可以客制化你自己的要求在这里，例如包括：英文作文的style,回答是要详细的还是简短的,回答是否需要native english/Chinglish]
```

>建议一题一题让Ai output答案，防止AI overload，以及使用*thinking*模式，增加AI的思考能力

>接着我们交给另一个模型的AI/另一个窗口的AI帮助我们验证答案:

```bash
现在，我需要你帮我非常仔细和非常详细的对比和验证一下这份功课的题目和我的回答：1.检查我的回答是否有回答了所有的问题，没有遗漏任何问题 2.我的回答是否完全正确，在逻辑上，语法上需要完全正确。先指出来有没有大体的问题。确保没有了大体的问题之后，再指出来有没有可能会导致扣分的minor mistake。
```

#### 如果喜欢,请不要犹豫给一个star我，对笔者会是很大的支持QAQ!
