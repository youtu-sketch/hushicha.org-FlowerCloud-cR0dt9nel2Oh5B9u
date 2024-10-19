[合集 \- 经验分享(29\)](https://github.com)[1\.记一次由于操作失误致使数据库瘫痪的故障分析与解决方案2023\-09\-08](https://github.com/guoxiaoyu/p/17678340.html)[2\.网络之谜：记一次失败排查的故事2023\-11\-15](https://github.com/guoxiaoyu/p/17811098.html)[3\.你是否想知道如何应对高并发？Go语言为你提供了答案！2023\-12\-29](https://github.com/guoxiaoyu/p/17933653.html)[4\.2023年终总结：拉帮结伙，拼搏探索新机遇2023\-12\-30](https://github.com/guoxiaoyu/p/17933731.html)[5\.谁说后端不能画出美丽的动图？让我来给大家拜个年！01\-29](https://github.com/guoxiaoyu/p/17991503)[6\.【10秒开服】幻兽帕鲁全自动部署教程，难道你还想手动搭建游戏服务器吗？快来学习这个简单又快速的方法！01\-30](https://github.com/guoxiaoyu/p/17998193)[7\.踩坑指南：入门OpenTenBase之部署篇04\-10](https://github.com/guoxiaoyu/p/18116318)[8\.踩坑指南：入门OpenTenBase之监控篇04\-11](https://github.com/guoxiaoyu/p/18117472)[9\.加速博客体验：静态资源优化技巧大揭秘！04\-28](https://github.com/guoxiaoyu/p/18149525)[10\.5分钟带你了解RabbitMQ的（普通/镜像）集群06\-14](https://github.com/guoxiaoyu/p/18240661)[11\.金仓数据库全攻略：简化部署，优化管理的全流程指南06\-21](https://github.com/guoxiaoyu/p/18257320)[12\.KES数据库实践指南：探索KES数据库的事务隔离级别07\-02](https://github.com/guoxiaoyu/p/18276998)[13\.云端IDE如何重定义开发体验07\-24](https://github.com/guoxiaoyu/p/18294897)[14\.国产数据库：数字时代的科技巨擘07\-16](https://github.com/guoxiaoyu/p/18295131):[蓝猫机场](https://fenfang.org)[15\.浅析前端数据埋点监控：用户行为与性能分析的桥梁08\-02](https://github.com/guoxiaoyu/p/18329944)[16\.数据库与我：一段关于学习与成长的深情回顾08\-05](https://github.com/guoxiaoyu/p/18338820)[17\.观存储历史，论数据未来08\-12](https://github.com/guoxiaoyu/p/18352499)[18\.从自建到云原生：数据管理的未来与变革08\-13](https://github.com/guoxiaoyu/p/18354003)[19\.深入分析与解决方案：缓存与数据库双写不一致问题08\-20](https://github.com/guoxiaoyu/p/18363049)[20\.小白系列：数据库基础知识解析08\-19](https://github.com/guoxiaoyu/p/18363713)[21\.智能客服的演变：从传统到向量数据库的新时代08\-21](https://github.com/guoxiaoyu/p/18370513)[22\.Cloud Studio：颠覆传统的云端开发与学习解决方案08\-28](https://github.com/guoxiaoyu/p/18382973)[23\.单元测试的入门实践与应用09\-05](https://github.com/guoxiaoyu/p/18395944)[24\.Git冲突解决技巧09\-15](https://github.com/guoxiaoyu/p/18409072)[25\.提升软件测试效率与灵活性：探索Mock测试的重要性09\-22](https://github.com/guoxiaoyu/p/18419378)[26\.从设计到代码：探索高效的前端开发工具与实践09\-28](https://github.com/guoxiaoyu/p/18425801)[27\.掌握Docker：简化KES单机安装与管理的最佳实践10\-01](https://github.com/guoxiaoyu/p/18436754)[28\.AI实战篇：Spring AI \+ 混元 手把手带你实现企业级稳定可部署的AI业务智能体10\-18](https://github.com/guoxiaoyu/p/18453559)29\.实用小工具——快速获取数据库时间写法10\-19收起
最近我遇到了一个比较棘手的问题：在工作中，各个项目所使用的数据库类型各不相同。这导致我习惯性地使用Oracle的SQL语句进行编写，但每次完成后都会遇到报错，最终才意识到项目的数据库并非Oracle。为了避免这种情况，我需要额外花时间去查找不同数据库版本的SQL语法，这严重耽误了我的工作效率。


为了提高我的工作效率，我决定自己编写一个脚本，以便能够快速获取所需的数据库语法，从而节省时间，专注于其他更重要的任务。


今天我使用了utools平台，专注于自动化脚本的编写。这个平台的搭建工作已经完成，所有的环境和依赖都已配置妥当。现在，剩下的任务就是我亲自撰写脚本，将自己的需求和功能实现出来。


# 准备工作


首先，你需要下载utools工具。这款工具以其便捷性和高效性著称，能够让你在需要的时候迅速调出所需功能，真正实现“呼之即来、即用即走”。


![image](https://img2024.cnblogs.com/blog/1423484/202410/1423484-20241012102252325-989392120.png)


这款工具应该是许多程序员在日常工作中必不可少的利器。它不仅提供了丰富的功能，还有广泛的社区支持。接下来，你需要前往商店，免费下载两个非常实用的插件——自动化脚本和JSON编辑器。


![image](https://img2024.cnblogs.com/blog/1423484/202410/1423484-20241012102256132-1748196365.png)


在这个工具中，你可以找到许多现成的自动化脚本，随时下载并使用。然而，这些脚本并不完全适合我的需求，因此我决定自己实现一个。


由于不同版本的数据库在语法上存在差异，我选择将我的实现以JSON格式进行展示，方便大家查看和理解。在这个过程中，由于涉及到数据的可视化展示，我还下载了JSON编辑器。这样一来，大家就可以更直观地操作和分析数据，而不仅仅是看一个简单的字符串，这样大大提升了操作的便利性和有效性。


# 编写脚本


接下来，我们可以自行创建这个脚本，具体步骤如下。


![image](https://img2024.cnblogs.com/blog/1423484/202410/1423484-20241012102301322-1939245747.png)


我会将基本代码写出来，以便大家参考和学习。



```
var conver = parseToJson(ENTER.payload)
var res = JSON.stringify(conver, null, 4);
utools.showNotification('"'+conver+'"'+'已生成完毕')
utools.redirect('Json', res);

function parseToJson(data) {
    const json = {"type":"text","word":"word"};
    return json;
}

```

这段代码的主要目的是将JSON数据传递给JSON编辑器插件，以便进行可视化展示和更便捷的操作。如图所示：


![image](https://img2024.cnblogs.com/blog/1423484/202410/1423484-20241012102310102-1303965624.png)


由于这段代码是基于utools平台开发的，因此其中的一些写法使用了utools集成的API。为了便于大家更好地理解这些写法及其背后的实现逻辑，建议大家参考utools的开发文档，那里提供了详细的说明和示例。在这里，我就不再逐一介绍每个API的细节。


## 各版本写法


剩下的部分就留给大家自行探索和尝试各种写法了。根据各自的需求，大家可以灵活添加或修改代码，以实现特定的功能或优化。


为了帮助大家更快入手，我在这里分享一些我常用的写法，供大家参考。



```
// 获取当前时间
const now = new Date();
const formattedDate = now.toISOString().slice(0, 19).replace('T', ' '); // 格式化为 'YYYY-MM-DD HH:mm:ss'

const json = {
    "指定时间": {
        "Oracle": `to_date('${formattedDate}', 'yyyy-mm-dd hh24:mi:ss')`,
        "MySQL": `STR_TO_DATE('${formattedDate}', '%Y-%m-%d %H:%i:%s')`,
        "PostgreSQL": `TO_TIMESTAMP('${formattedDate}', 'YYYY-MM-DD HH24:MI:SS')`,
        "SQL Server": `CONVERT(DATETIME, '${formattedDate}', 120)`,
        "SQLite": `DATETIME('${formattedDate}')`
    },
    "当前时间": {
        "Oracle": "SYSDATE",
        "MySQL": "NOW()",
        "PostgreSQL": "CURRENT_TIMESTAMP",
        "SQL Server": "GETDATE()",
        "SQLite": "CURRENT_TIMESTAMP"
    },
    "时间转字符串": {
        "Oracle": "TO_CHAR(SYSDATE, 'YYYY-MM-DD HH24:MI:SS')",
        "MySQL": "DATE_FORMAT(NOW(), '%Y-%m-%d %H:%i:%s')",
        "PostgreSQL": "TO_CHAR(CURRENT_TIMESTAMP, 'YYYY-MM-DD HH24:MI:SS')",
        "SQL Server": "CONVERT(VARCHAR, GETDATE(), 120)",
        "SQLite": "STRFTIME('%Y-%m-%d %H:%M:%S', 'now')"
    }
};

```

## 实现效果


接下来的步骤是自动发起JSON调用，之后只需将生成的结果复制下来进行使用即可。尽管这个工具体积较小，但它能够帮助我节省大量的时间和精力。


将自己的脚本上架之后，只需在utools中输入相应的配置关键字即可轻松调用。


![image](https://img2024.cnblogs.com/blog/1423484/202410/1423484-20241012102316502-934670264.png)


运行成功，系统已顺利完成操作，具体结果如图所示。


![image](https://img2024.cnblogs.com/blog/1423484/202410/1423484-20241012102322920-1585848774.png)


希望这个工具能够为大家提供帮助，提升工作效率。


# 总结


如果你们有任何想要实现的小工具，utools绝对是一个值得考虑的平台。它不仅功能强大，而且特别适合程序员的工作方式，能够满足我们对灵活性和可定制性的需求。


