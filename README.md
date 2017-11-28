
![img](https://github.com/duoergun0729/1book/raw/master/photo/%E6%B5%B7%E6%8A%A5.jpg)
# 京东链接
[https://item.jd.com/12277728.html](https://item.jd.com/12277728.html)
# 主要内容
　　在现今的互联网公司中，产品线绵延复杂，安全防御体系无时无刻不在应对新的挑战。哪怕是拥有丰富工作经验的安全从业者，在面对层出不穷的攻击手段和海量日志数据时也会望洋兴叹。机器学习、深度学习是这些问题天然契合的解决方案，在数据量以指数级不断增长的未来，甚至有可能是唯*的出路。当AI遇到安全时，如何快速进化，本书给出了实战方案。
　　本书是作者推出AI+安全畅销书《Web安全之机器学习》之后又一力作。本书首先介绍如何打造自己的深度学习工具箱，包括TensorFlow、TFLearn等深度学习库的安装以及使用方法。接着介绍卷积神经网络和循环神经网络这两大深度学习算法的基础知识。特别着重介绍在生产环境搭建深度学习平台需要使用的开源组件，包括Logstash、Kafka、Storm、Spark等。随后讲解了11个使用机器学习技术解决实际安全问题的案例，包括验证码识别、垃圾邮件识别、负面评论识别、骚扰短信识别、Linux后门检测、恶意操作行为检测、Webshell检测、智能扫描、DGA域名检测、恶意程序分类识别、反信用卡欺诈。本书针对每一个算法都给出了具体案例，理论结合实际，讲解清晰，文笔幽默，适合有信息安全基础知识的网络开发与运维技术人员参考。
　　主要内容包括：
　　1.如何基于TensorFlow和TFLearn打造自己的深度学习工具箱。
　　2.如何基于Logstash、Kafka、Storm、Spark等打造深度学习的生产环境。
　　3.如何在MNIST数据集上实现验证码识别。
　　4.如何在安然数据集上实现垃圾邮件检测。
　　5.如何在IMDB数据集上实现负面评论识别。
　　6.如何在SMSSpamCollection数据集上实现骚扰短信识别。
　　7.如何在ADFA-LD数据集上实现Linux后门检测。
　　8.如何在SEA数据集上实现恶意操作行为检测。
　　9.如何在MIST数据集上实现恶意程序分类识别。
　　10.如何在Kaggle公开的数据集上实现信用卡欺诈检测。
　　11.如何在GitHub公开的数据集上实现Webshell检测，智能扫描和DGA域名检测。

# 前言

​	网络安全一直和AI相伴相生，从网络安全诞生的那一天起，人们就一直试图使用自动化的方式去解决安全问题。网络安全专家一直试图把自己对网络威胁的理解转换成机器可以理解的方式，比如黑白名单、正则表达式，然后利用机器强大的计算能力，夜以继日地从流量、日志、文件中寻找似曾相识的各类威胁。似乎这一切就是那么天经地义并无懈可击。但事情似乎又没有那么简单，机器其实并没有完全学到人的经验，网络安全专家一眼就可以识破的变形，对于机器却难以理解；更可怕的是，恶意程序数量呈指数级增长，各类新型攻击方式层出不穷，0day的出现早已超过一线明星出现在新闻头条的频率，依靠极其有限的网络专家总结的经验和几个安全厂商所谓的样本交换，已经难以应付现在的网络安全威胁。如果安全专家一眼就可以识破的威胁，机器也能够自动化发现甚至做出相应的响应，这已经是很大的进步；如果让机器可以像阿尔法狗理解围棋一样理解网络威胁，那将是巨大进步。事情又回到最初的那个问题，如何能让机器可以真正学会识别安全威胁？机器学习可能是一个不错的答案。
本书面向信息安全从业人员、大专院校计算机相关专业学生以及信息安全爱好者、机器学习爱好者，对于想了解人工智能的CTO、运维总监、架构师同样也是一本不错的科普书籍。如果读者看完本书，在工作学习中遇到问题时可以想起一到两种算法，那么我觉得就达到效果了；如果读者读完本书，可以像使用printf一样使用SVM、朴素贝叶斯等算法，那么这本书就相当成功了。
我写本书的初衷是帮助信息安全从业者了解机器学习，可以动手使用简单的机器学习算法解决实际问题。在写作中尽量避免生硬的说教，能用文字描述的尽量不用冷冰冰的公式，能用图和代码说明的尽量不用多余的文字。正如霍金所言“多写1个公式，少一半读者”，希望反之亦然。
机器学习应用于安全领域遇到的最大问题就是缺乏大量的黑样本，即所谓的攻击样本，尤其相对于大量的正常业务访问，攻击行为尤其是成功的攻击行为是非常少的，这就给机器学习带来了很大挑战。本书很少对不同算法进行横向比较，也是因为在不同场景下不同算法的确表现差别很大，很难说深度学习就一定比朴素贝叶斯好，也很难说支持向量机就比不过卷积神经网络，拿某个具体场景进行横评意义不大，毕竟选择算法不像购买SUV，可以拿几十个参数评头论足，最后还是需要大家结合实际问题去选择。
本书的第1章主要介绍了如何打造自己的深度学习工具箱，介绍了本书使用的TensorFlow、TFLearn等深度学习库的安装以及使用方法。第2章和第3章介绍了卷积神经网络和循环神经网络这两大深度学习算法的基础知识。第4章介绍在生产环境搭建机器学习平台需要使用的开源组件，包括Logstash、Kafka、Storm、Spark等，并且介绍了GPU和TPU的基础知识。第5章到第15章，介绍了11个使用机器学习技术解决实际安全问题的案例，包括验证码识别、垃圾邮件识别、负面评论识别、骚扰短信识别、Linux后门检测、用户行为分析与恶意行为检测、WebShell检测、智能扫描器、DGA域名检测、恶意程序分类识别、反信用卡欺诈，每个案例都使用互联网公开的数据集并配有基于Python的代码，代码和数据集可以在本书配套的GitHub下载。
本书是我所著机器学习三部曲的第二部，第一部主要以机器学习常见算法为主线，利用生活中的例子和具体安全场景来介绍机器学习常见算法，是机器学习入门书籍，便于读者可以快速上手。全部代码都能在普通PC上运行。本书将重点介绍深度学习，并以具体的11个案例介绍机器学习的应用，定位是面向具有一定机器学习基础或者致力于使用机器学习解决工作中问题的读者，本书将重点放在问题的解决而不是算法的介绍。由于深度学习通常计算量已经超过了PC的能力，部分代码需要在服务器甚至GPU上运行，不过这不影响大家的阅读与学习。第三部将重点介绍强化学习和对抗网络，并利用若干虚构安全产品或者项目来介绍如何让机器真正具备阿尔法狗级别的智能。遗憾的是，深度学习的优势发挥需要大量精准标注的训练样本，但是由于各种各样的原因，我只能在书中使用互联网上已经公开的数据集，这些数据量级往往很难发挥深度学习的优势，对于真正想在生产环境中验证想法的读者需要搜集更多样本。
致谢
这里我要感谢我的家人对我的支持，本来工作就很忙，没有太多时间处理家务，写书更是花费了我大量的休息时间，我的妻子无条件承担起了全部家务，尤其是照料孩子等繁杂事务。我很感谢我的女儿，写书这段时间几乎没有时间陪她玩，她很懂事地自己玩，我想用这本书作为她的生日礼物送给她。我还要感谢吴怡编辑对我的支持和鼓励，让我可以坚持把这本书写完。最后还要感谢各位业内好友尤其是我boss对我的支持，排名不分先后：马杰@百度安全、冯景辉@百度安全、Tony@京东安全、程岩@京东安全、简单@京东安全、林晓东@百度基础架构、黄颖@百度IT、李振宇@百度AI、Lenx@百度安全、黄正@百度安全、郝轶@百度云、云鹏@百度无人车、阿文@丁牛、赵林林@微步在线、张宇平@数盟、谢忱@Freebuf、李新@Freebuf、李琦@清华、徐恪@清华、王宇@蚂蚁金服、王珉然@蚂蚁金服、王龙@蚂蚁金服、周涛@启明星辰、姚志武@借贷宝、刘静@安天、刘袁君@医渡云、廖威@易宝支付、尹毅@sobug、宋文宽@联想、团长@宜人贷、齐鲁@搜狐安全、吴圣@58安全、康宇@新浪安全、幻泉@i春秋、雅驰@i春秋、王庆双@i春秋、张亚同@i春秋、王禾@微软、李臻@paloalto、西瓜@四叶草、郑伟@四叶草、朱利军@四叶草、土夫子@XSRC、英雄马@乐视云、sbilly@360、侯曼@360、高磊@滴滴、高磊@爱加密、高渐离@华为、刘洪善@华为云、宋柏林@一亩田、张昊@一亩田、张开@安恒、李硕@智联、阿杜@优信拍、李斌@房多多、李程@搜狗、姚聪@face+、李鸣雷@金山云、吴鲁加@小密圈，最后我还要感谢我的亲密战友陈燕、康亮亮、蔡奇、哲超、新宇、子奇、月升、王磊、碳基体、刘璇、钱华钩、刘超、王胄、吴梅、冯侦探、冯永校。
我平时在Freebuf专栏以及i春秋分享企业安全建设以及人工智能相关经验与最新话题，同时也运营我的微信公众号“兜哥带你学安全”、知识星球（原名小密圈）“Web安全之机器学习”，欢迎大家关注并在线交流。之前没有使用过知识星球的读者可以在各类应用市场上搜索。
本书使用的代码和数据均在GitHub上发布，地址为：https://github.com/duoergun0729/2book，代码层面任何疑问可以在GitHub上直接反馈。


​	我的公众号二维码为：

![img](https://github.com/duoergun0729/4book/raw/master/photo/logo/qrcode_for_gh_810edc392056_258.jpg)

​       我的i春秋专栏二维码为：

![img](https://github.com/duoergun0729/4book/raw/master/photo/logo/i%E6%98%A5%E7%A7%8B.png)





 
