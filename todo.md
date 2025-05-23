小学阅读准确性
测验内容：要求儿童依次朗读每组内的所有汉字，不会可以跳过。
主试记录：读对打勾，读错打叉并记录儿童读错的拼音，不会读打圈。
计分方式：朗读正确计1分，错误或不会计0分，以每组小分乘以每组系数求和得到总分。

小学阅读流畅性
测验内容：在1min的倒计时内，让儿童尽快按行朗读字表上的汉字。共朗读两遍，第一遍结束后重新计时朗读第二遍。
主试记录：儿童朗读的同时，在汉字下方的格子内对被试朗读结果进行记录，正确朗读不记录，错误朗读打叉，漏读画圈，用脚标备注错读或漏读发生在第几遍。如×1代表这个字第一遍读错。
计分方式：只记录正确朗读的个数作为分数，错读漏读不计分也不扣分。两遍平均分作为最终得分。

注意力符号划削
测验内容：在3min的倒计时内，让儿童按照一行一行的顺序圈出ψ。
主试记录：测验开始前带领儿童理解规则，完成练习；倒计时一结束用//标注出儿童最后一个看到的符号（可以不是目标符号ψ）；标注后对照答案进行判分。
计分方式：记录//以前儿童正确（是ψ且圈）、错误（不是ψ但圈）、遗漏（是ψ但没圈）的个数。最终得分为：正确-错误-0.5×遗漏。如，某一儿童正确个数21，错误个数1，遗漏个数2，则总分为19。

小学计算题
测验内容：在10min倒计时内，让儿童按照题号顺序笔算完成对应年级得40道计算题目。
主试记录：倒计时结束后对计算结果进行判分。
计分方式：正确作答计1分，漏答（未答）、答错计0分，分数计算题未约分但答案正确计0.5分，测验要求写循环节但仍然保留两位计0.5分。总分即位最终得分。

中学阅读流畅性
测验内容：在3min倒计时内，让学生按照题号顺序默读并回答阅读问题。
主试记录：倒计时结束后对做了部分的结果进行判分。
计分方式：正确作答计1分，漏答（未答）、答错计0分。总分即位最终得分。

中学计算流畅性
测验内容：在3min倒计时内，让学生按照题号顺序进行计算，可以笔算在旁边空白处列草稿，但不能使用计算器。
主试记录：倒计时结束后对做了部分的结果进行判分。
计分方式：正确作答计1分，漏答（未答）、答错计0分。总分即位最终得分。



docker update --restart=always mysql-8-app
docker update --restart=no ragflow-server
docker update --restart=no ragflow-redis

接下来让我们来设计第三个系统：计算流畅性测试。计算流畅性分为7个级别，分别是一到六年级6个级别和第7个级别大朋友。由于高年级会引入新的内容，我们先实现一到三年级的测试，测试的级别由进入测试的用户信息中的年级决定①一到三年级的题目完全由前端按相应的规则生成，测试一共40道题，默认3分钟（不同年级的时间不一样，可修改不同年级的时间），回传到服务器时应该包含题目的题干、用户答案、是否正确等信息。②一年级的题目为0到10，两个数的加减法，加法减法各20题，只有当其中有一个10的时候，计算结果才能超过10；如果两个数中没有10，计算结果不能超过10或者为负数。因此1+3合法，2+8合法，10+3合法，4+7不合法，2-4不合法。③二年级的题目为两位数（可以包含一位数）的加减法；其中第一部分的0道题为两个数字的加减法，第二部分10道题为三个数字的加减法（此时2个运算符号可以相同可以不同，注意当第一个符号为减号时，不要让第一个数小于第二个数）。计算结果不能超过100或者为负数④三年级的题目与二年级类似，其中第一部分10道为三位数和两位数的加减法，第二部分20道为三位数与三位数的加减法，第三部分10道为三位数3个数字的加减法。计算结果不能超过1000或者为负数⑤二三年级的题目中复杂规则的题目应该集中放后面⑥每道题前面都有题目的编号

非常棒！接下来优化一下。①ElementPlusError: [props] [API] type.text is about to be deprecated in version 3.0.0, please use link instead.
For more detail, please visit: https://element-plus.org/en-US/component/button.html#button-attributes②优化UI，现在selection页面3个测试的布局不统一，而且计算流畅性测试的回答区域太小了③评分记录到数据库会话中，正确作答计1分，漏答（未答）、答错计0分，可能需要改模型

igneous:gg1ag51o5rlur91hp
ipb_member_id:4286824
ipb_pass_hash:7423a7387437ad1b071134c697ad7a59