---
layout: page
title: KangEr (康尔)
description: Accessible healthcare Q&A with Large Language Models.
img: assets/img/projects/kanger_preview.jpeg
importance: 1
category: Artificial Intelligence
related_publications: false
---
*You can access the web app at [kanger-ai.web.app](https://kanger-ai.web.app).*

It's ironic that despite the promises of AI pioneers like Sam Altman that AI could narrow wealth disparities by boosting the productivity of the underprivileged, many communities lack both awareness of and access to AI technologies. This paradox highlights the missed potential for AI to act as a catalyst for inclusive societal and economic advancement, akin to past industrial revolutions. Therefore, I decided to champion AI accessibility in underprivileged communities, starting with rural Chinese villages.

My family roots have led me to explore numerous remote villages in China, some requiring a two-hour journey through mountains from the nearest city. These communities, due to geographical and economic constraints, often lack access to healthcare and medical knowledge, relying on just one rural doctor for basic services.

This realization struck me while researching **Large Language Models (LLMs)** and pondering why these text giants couldn't serve as virtual doctors. LLMs, with their extensive training data, seemed like ideal candidates. Their natural language interface also promised to bridge the gap for those with limited education, making complex medical knowledge more accessible than dense textbooks or obscure blogs. Moreover, LLMs offered personalized interactions, allowing users to ask specific questions.

Hence, I conducted numerous experiments with medical Q&A using ChatGPT (GPT-3.5-turbo) in Chinese to evaluate its authenticity and quality. However, I encountered a significant issue: **hallucination**, where the AI generated inaccurate responses, as illustrated below.

<div class="row">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/chatgpt_hallucination.png" title="ChatGPT Hallucination" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/kanger_rag.png" title="KangEr with RAG" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    When I asked GPT-3.5-turbo about Reiter's syndrome in Chinese, it provided a completely inaccurate description. However, RAG solves this, as shown by the response of KangEr to the right.
</div>

This is unacceptable for a healthcare-related application. Fortunately, a solution emerged thanks to **Retrieval-Augmented Generation (RAG)**, which addressed the hallucination problem by prompting LLMs with correct information searched from the internet, as demonstrated by KangEr's accurate response to Reiter's syndrome above.

`GPT-3.5-turbo` also showed its deficiency in understanding and generating Chinese, yet the cost of `GPT-4` APIs was prohibitive. I opted instead for iFlytek's API, integrating RAG capabilities and prompt engineering into their model `iFlytekSpark-3.1`, resulting in the **KangEr (康尔) web app**.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/kanger_demo_1.png" title="KangEr Chat Interface" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/kanger_demo_2.png" title="KangEr History Page" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/kanger_demo_3.png" title="KangEr Help Section" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
   A glimpse into KangEr's web app, showcasing its clean chat interface, a detailed history page with dates, and an intuitive help section.
</div>

This app allows users to **voice their questions and receive spoken answers**, overcoming literacy barriers in rural areas. Its **web-based** nature ensures accessibility across devices without requiring downloads, leveraging China's high mobile penetration rate of 99.8%.

I'm currently collaborating with rural health organizations to promote KangEr and plan to visit various villages to gather user feedback. This iterative process will tailor the app to real-life situations faced in rural areas. I believe KangEr has the potential to enhance both healthcare and AI accessibility in the often-overlooked parts of China's vast landscape, spanning 3,705,000 mi².

---
### Field Trip to Rural Areas, Memoir
In cooperation with the Chinese Center for Disease Control and Prevention, I visited over 20 rural villages across two provinces (Fujian and Henan) to promote the KangEr app in person to the rural doctors. I am proud to announce that the app is now actively used by 75 rural health workers in their daily practice. 

<div class="row">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/kanger_rural_1.jpg" title="KangEr Field Trip" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/kanger_rural_3.jpg" title="KangEr Field Trip" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Photos that have been taken during the field trip to rural areas.
</div>

In addition, I also hosted two workshops in the local commune in Jiangjunshan community, Fujian Province. The workshops aim to make the knowledge of AI accessible to these residents between the hills, and introduce the KangEr app to help with their daily healthcare needs. Beside professional health workers, the app is now used by hundreds of non-professional residents in their daily life.

<div class="row">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/kanger_rural_2.jpg" title="KangEr Field Trip" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/kanger_rural_4.jpg" title="KangEr Field Trip" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Photos of me hosting workshops in the local commune in Jiangjunshan community, Fujian Province.
</div>

I've also written a memoir to record my experiences during the field trip. Besides, it also includes my reflections thereafter: the lessons I learned, the situations facing China's rural healthcare, and the status of technology accessibility in underpriveleged areas. The memoir is written in Chinese, and it is provided below.

---
## 康尔 纪实

夏日早晨七点。

黑色的红旗轿车穿过大路。双向十车道的大路空空荡荡，平原县城的宽敞在南方甚是少见。

干燥的气候也是如此。头顶高照的太阳并没有带来酷暑，也没有沿海城市特有高湿度环境下与阳光不匹配的体感温度，和似有似无的汗感。我默默套上了夹克。

“风正使天气变得凉爽。”天气软件提示道，“体感温度28摄氏度。”

手上一包十片的旺仔牛奶糖是我的早餐，大红的包装略微提神。起床气正将头发吹得好似雀巢，刘海之下是两个黑圈包裹着的一双眼睛，些许血丝点缀让它们看上去不那么像熊猫。一阵干涩袭来，我快速地眨了两下眼。

迎接者是中牟当地疾控中心站长，他和妻子带着刚上小学的女儿。孩子身着新中式连衣裙，嚷嚷着要和妈妈一起坐。温馨的场景舒缓了进村前的紧张感 — 这是一直生活在深圳社交圈的我第一次与素不相识的人们来到未知的乡村。

“有些村医的诊所外边儿还晒着菜，里面都是破木头，”车上初次谋面的北京同行说道，“咱们走一步看一步吧，不知道他们的接受程度如何。”我不禁关上了蓝色夹克的拉链。

半小时的路程将我们从县城带入了狼城岗镇。“这儿一共有四万来号人，算是附近经济水平中等的镇了，”站长普及道。说罢，一个转弯将车子带入了片光秃秃的水泥地。浅灰之上搭建着白砖垒成的单层平房，掠过珠链便能直入其中。一位身着蓝色条纹保罗衫的男人正坐在电脑前，手边是一沓处方笺，第一页有着少许草体字符。

些许茫然，这是我初次进入中原地区。沿海省份乡村都少有访问的我对中原的基建、风土更是一无所知。进村之前，我甚至担心当地的网络信号是否足以打开我的软件。事实证明，这有些杞人忧天了 — 村里有堪比深圳的连接速度。这也是我初次和乡村卫生人员交流，对他们的文化背景、实际工作更是一张白纸。

正当我犹豫如何开口时，站长的妻子闯了进来，大声做着介绍：”这俩北京人大附中的学生来做社会实践，全国第一的高中啊。他们过来采访调研一下乡村的医疗现状，对这方面感兴趣。“显然，她和站长对我们此行的目的知之甚少，连我的身份都未有耳闻。正是在误打误撞中我们进入了陌生的乡村腹地。

热情的笑容在保罗衫男人的国字脸庞绽开，方方正正、刻板印象里中原人的长相让这笑容变得尤为和蔼。我和北京同行迎着笑容开始了软件介绍。

“咱们儿这次过来是做了个医疗相关的软件，想和您推荐使用一下。也征求下您用完后宝贵的反馈，这样咱好提升。”我笑着说道，他热情的态度打消了我对未知的犹豫，“您用浏览器打开下这个网址？”我在备忘录打下了“kangerai.site”，放大了屏幕显示，转过手机给他看。

“K — A — N......”他一个个字符地念着，熟练地用两手粗壮的大拇指敲打着九宫格键盘。

我在一旁介绍道：”咱这是个医疗问答软件，它可以回答任意医疗健康方面的问题，像‘连花清瘟怎么服用’这样。它回答的消息一定是准确的，因为它会先在网络上搜索一遍真的资料，再总结用咱平常说话的语言和您说。“

”您也可以给它描述患者的症状，它会告诉您病人可能得的病都有哪些。“真正来自人大附中的同行补充道，”不过只能作为一个辅助，最终把关的还得是您。“

”是的，您可以把它当作一个医疗辅助专家，还可以接着用自然语言追问它，像这样。“我接过话茬，演示给村医看，“不过最终还是要您来做决定。”

他始终浅浅露出几颗牙齿，嘴角微扬，边点头边看着我们的示范。手上也没闲着，在软件的对话框里输入起了问题。这个问题竟然是与中药相关的，十分令人惊讶。

更令我诧异的是他对软件的娴熟。我对村医的印象还停留在“赤脚大夫”这个在八十年代就消亡的概念中，这似乎是现代社会人们对他们认为不专业、不在大医院坐诊的卫生工作者的统称 — 后来，甚至在我向高文化人群（如中学老师）询问乡镇里”村医“的情况及分布时，他们都混淆地称呼村医们为“这些赤脚医生都是五六十岁的老人家”。这称谓或多或少带有歧视性，好似村医是一些文化水平低下、只用偏方的”野郎中“。我也深受这种思维惯性的毒害，认为村医们（所谓“赤脚大夫”们）对电子产品或许十分生疏，甚至完全不会使用。这种“数码歧视”来源于大城市的沾沾自得，总觉得自己在技术发展上高人一等，却忘却了乡镇脱贫复兴带来的新农村建设、和互联网的魅力。

我更愧疚的是对于“赤脚大夫”专业性的轻视。诚然，文革时期真正“赤脚大夫”是接受少许医疗教育的农民。他们的主要职能是负责基础疾病防治（如注射疫苗）、接生、处理基础急诊、并将重病患者转诊至上级医院这类初级任务。同时，他们也负责少许政治宣传 — 赤脚大夫们本身就是“群众运动”的表现。殊不知，”赤脚大夫“也是他们所在时代的英雄。惩创于已然，不如防患于未然。赤脚大夫们主动背着行囊前往村民家里问诊或进行公共卫生宣传、疾病预防。七十年代末到八十年代初，农村合作医疗的覆盖率达到90%以上，全国期望寿命提高至67.9岁（*中国卫生政策研究，2009*）。赤脚大夫是文革前后公共卫生的守护者。

然而，半农民半大夫、半政治宣传半医学专家的观念在这白瓦包裹、白光亮堂的诊室里显得尤为突兀。“乡村医生”并不是“赤脚大夫”。早在1985年全国卫生厅局长会议中，“赤脚大夫”被分流成达到医士水平的“乡村医生”和未达标的“卫生员”，这个称呼也就此成为历史。在2013年颁布的《全国乡村医生教育规划（2011 - 2020年）》中，卫计委要求在十年内乡村医师应具有中职（中专）以上学历，并需持有执业（助理）医师资格证（*卫生软科学，2023*）。学历及专业要求使村医往往是村民中文化水平较高的人群，他们的角色也从“半桶水”的农民村医变成了专业的医师。未来前对于他们作为“低文化农村人”的滤镜在此刻支离破碎，瓣瓣镜片反射出了一个先入为主的我。没有调查，没有发言权。

我甩了甩脑袋，将思绪从年代的回忆中抛离出来。保罗衫村医的接受程度唤醒了我开发“康尔”的初衷 — 普及人工智能。“康尔”不止是医疗助手，更是普及人工智能等前沿科技的载体。近期（2022年后）互联网对于人工智能的讨论如火如荼，各大科技巨头也在快马加鞭地研发出最新的人工智能模型，并宣称这项技术可以提高弱势群体的生产力，从而降低贫富差距并带动经济发展。不幸的是，弱势群体或许根本没有机会去了解人工智能，何谈使用这项技术。然而，我个人终极奋斗的目标之一是“技术平权”，因为我坚信人人都有平等使用技术的权利，而技术（尤其是人工智能）也只有在普及到万千群众时才能发挥其最大价值，帮助每个人都“变懒”，提高他们的生产力，就此宏观地带动社会进步乃至于变革。“康尔”便是借助医疗普及为媒介，让居住在经济较为落后地区的弱势村民们享受到人工智能的福利，并真切地在日常生活中去使用它。

“村民对新鲜电子事物接受这么快，那我技术普及的目标是否可以更加轻松快速的实现？”内心欣喜道，“或许他们早已知道人工智能呢？”

我不禁询问了起来：“请问您之前有听说过人工智能吗？”

渴望的眼神看向村医。他些许漆黑的脸庞有着丝丝皱纹，若隐若现地覆盖着形状清晰的毛孔，皮肤如潮水起起伏伏。嘴唇厚实且干涩，隐隐约约有少许裂痕，一张一合地说着话：“听说过，咱在抖音上听的。”

“抖音”，这熟悉又陌生的二字让我一颤。它的出现时常是伴有负面情绪的：低价多巴胺、注意力涣散、短视频毒药这些词妖魔化了这个软件。初中时，一台装着抖音的手机能让我躺在床上一天不动弹，新鲜的刺激高强度地攻击着脑部神经。每当我倦了，上滑屏幕清除抖音后台，再关闭屏显准备做些旁事时，空虚感总会在脑海蔓延。疲惫的它病怏怏地看着各种纷彩的事情：篮球、阅读、骑车，却提不起任何兴趣。大脑晕糊的连起身的动力都消散了，只能再翻身拿起手机，点开这个黑底白音符的软件，听着重复的网络红曲，看着套路一致的视频。因此，上了高中后，抖音从未在我的手机上出现过。然而，万事皆有两面性，而村医的话照亮了这把双刃剑的另一半。抖音凭借其顺应人性的应用逻辑吸引了跨度极大的用户群，从青少年至老年，含括不同的收入及地理群体。就算是远在山村里的居民，只要有网络信号，多少都有访问过短视频。而短视频碎片化的消息虽总体质量不高，但涵盖面却广，作为知识基础普及的媒介是绰绰有余，只要保证消息的真实及准确性。

“抖音本身就是技术平权的展现，它让群众学会基本操控手机。它或许也是技术平权最方便的一种途径。”我心记下。

有着抖音基础的村医很快便熟练上手了软件，还把它添加至了桌面。“挺好的啊，我再试着用用，到时候给我的患者也推荐下。”他笑盈盈地收起了手机，目光向我们打量来。

“呼。”我轻轻吐出一口长气。气体被吹到了手臂外的蓝色夹克，它微微一颤。初次探访的顺利是意想不到的丝滑，村医对于电子事物（甚至是人工智能）的接受程度是出乎意料的迅速，让我不禁对后续充满了信心。转头望向窗外，红白的眼球对上了烈日，却也没那么刺眼。

然而，站长妻子的一番话却让我走出村所的步伐逐渐沉重。

“这村医儿年轻着、这村又发展好点儿，所以他估计听过人工智能。咱们去一些比较偏远的乡，见一些老村医就不好说了。”

我默默往回一瞟。印入眼帘的是一个简单的白瓦房，和一位坐在钢桌前、写着处方单的村医。他脸上的皱纹依稀可见。

---

太阳继续向上攀爬着，白黄色的光芒洒向天空幕布。万里无云，蔚蓝色在空中洒开，均匀得有些无趣。

早晨九点，微风依旧。我踏下车门，微微一抖将蓝色夹克的衣帽甩向中间，迎着阳光走在另一块坚硬的水泥地上。“中牟县保护文物”，眼前土楼旁的石牌写着。那是一幢二层平房，全身都由土砖砌成。四百年的历史让砖体染上了种种颜色：或灰、或青、或棕、或红，交错着堆叠起来。方方正正、垂直对称的设计从远处看颇像块灰暗的长方体坚毅地屹立在土地之上。石头搭建的屋檐在左右两角微微翘起，好似河马的两只小耳，为建筑增添了些许灵气。

“真是有历史的地方。”我却暗暗捏了把汗。

村卫生所坐落在平房之后。水泥墙，木屋檐，风格颇像闽南地区的”祖屋“。门前两侧贴墙放置着木质矮柜，台面上晒着刚收割的青菜，颇有“赤脚大夫”的风范。可惜少下农田的我却认不出这蔬菜的种类。

“你先吃这个药，明儿再来找我看看。”未进门，先闻声。纯正的河南话传入耳，幸好中原的方言和普通话都颇为相似。

顺着声左拐便是卫生室。患者是一位头发皆白、驼着背的老妇人，右手正拿着未开封的西药盒，包装上的“布洛芬”三字尤为显眼。待她出来我们就掠开珠链进了房间。

屋子里的陈设与上间村所的现代风浑然不同。纯白漆水泥墙已悄悄变灰，白色的划痕好似是这块墙面的外来者。两张木制桌子呈九十度沿墙角摆开，上面放着足有三十厘米高的处方笺，被沉红色、有斑斑锈迹的铁架子艰难地夹着。纸叠旁是深色的木算盘，算珠上下摆开。一台黑色的一体机却放置在算盘旁，尽管屏幕关着并有少许灰尘。亮白色西药盒散落在桌面，案上物品的摆放如同大杂烩： 有古有今、有中有西。

站长妻子再次亲切地介绍着：“这俩孩子是北京来的高中生，他们做了个人工智能软件来帮助咱们村医。高科技啊，让他们给你讲讲。”

我望向了她朝着的村医。后者皮肤黝黑且粗糙，略微泛黄的牙齿似乎还带着些许烟味。头发黑白相间，稀疏地扒拉在头皮上。听到“高科技”一词，他下意识得身子往后一倾，窘迫地说：“我不懂什么高科技。”呲起的笑嘴好似在掩饰着自己的尴尬，令人心酸。

“您会用微信吗，会用微信就肯定会这个。”我急忙安慰道。见他点点头，我继续介绍道，“您能打开电脑一下吗。”

他又默默地点了点头，伸手在显示器背面按下了开机键。久违的开场动画令我微微失神 — 这台电脑装有Windows 7操作系统，一个2009年开发的“老古董”。我往前站了站，接过了鼠标的操控权，躬身看着眼前的电脑。

“你们坐，快坐。”他客气道，从位置上站了起来，怯怯地看着屏幕。我和同行有些受宠若惊，连声劝说让他坐下 — 我们眼前的是一位爷爷辈、为公共健康奉献一辈子、值得尊敬的乡村工作者。

注意力重回屏幕。我习惯性地同时按下键盘上的Windows和S键，想调出搜索栏以打开浏览器，但试了几次却无果，只好在桌面上查找相关图标。打开微软Edge浏览器，输入网址，进入主页，一气呵成。对着屏幕，我和同行开始了介绍与演示。

“中（好）啊，中啊。”两声河南方言突然插入了我们滔滔不绝的话语，吓得我们声音乍然而止。我转头望向村医，惊喜地发现他的表情和刚刚提到“高科技”时一样，正咧嘴笑着。与之不同的是，他的眼神正笔直盯着前方屏幕，脖子微微前倾，背也略躬了起来，好似在认真阅读屏幕上的每一个文字。“康尔”运用了流式输出，随着字符一个接一个出现在对话屏幕内，村医嘴角的弧度也一度度地变大。

“中，中，中，中啊！后生可畏啊，它能帮我大忙咯，省事儿啊。”看完“康尔”完整的回答，他感叹道，“你们能不能把这个软件给我下载下来，这样我以后立马能用。”

我们立马在桌面为他创建了一个网页快捷方式。

“它不仅能辅助我们这些老头子，我们还可以在平常和他的聊天中学到医疗知识长进自己嘞。”他补充道，手已经伸向了键盘，“让我试试其他问题。”

这番话点出了我们未曾设想的“康尔”的好处。实践中学习，在不断和“康尔”沟通的过程中，村医们不仅能得到辅助，更能汲取新的医学知识或强化已有知识，从而潜移默化地提高自己的医疗服务水平。

目光掠过正在认真“对话”的老村医。他伸出皮肤略微松塌的食指正一个个字符地点击着键盘，眼神在键盘与显示屏间来回飘忽。屏幕上布满了他的聊天记录。尽管从未听闻何为“人工智能”，身为医疗从业者的他对相关知识的准确性却极为敏感。因此，在目睹”康尔“生成的准确又符合乡村实际需求的信息后，就会选择使用甚至相信这软件。如同大众使用抖音、微信等互联网应用时，他们仅见识到了这类程式的强大实用性，便选择将它们融入自己的日常生活。或许这些程序背后的原理与逻辑对大众来说并不重要。因此，技术普及者最聪明的办法是找到科技能带来便利生活的应用场景，并通过此场景向大众进行宣发，而不是一昧地向大众举办公开课，枯燥地传授人们不觉重要的知识。当人们真实用上这项科技时，也许他们不知道原理，但总得到了效率上的提升，而技术也就被普及到了。这便是“康尔”努力的方向 — 以乡村医疗为切入口让群众用上人工智能。

然而，这需要普及者坚守初心，也是最难得的。群众不明原理时便是最易被渗透时：科技提供者可以简单地植入后门，收集用户信息，或通过其他方式将大众变成牟利的“僵尸”。固然，科技普及是达到了，但却离科技平权的基本目的渐行渐远。大众享受生产力提高的同时又被压榨着价值，经济分裂只会越演越烈，弱势群体会逐渐失去自由。人们总想追逐自由，享受随心所欲的、对自我的掌控感。赚钱追求的是拥有财富后可以自由地花销，自由地购买能带来物质或情绪价值的产品，自由地享受花钱时带来的满足或其他正反馈。这份自由源于不用担心借钱时那种“欠”对方的、低下的、被“控制”的心理，或没钱时求而不得的百般难受。尽管生活会强迫我们在特定方面大量开销，但拥有财富后支配这些钱的权利还是掌握在自己手中（或许他就想叛逆生活呢）。诚然，绝对的自由是不存在的。人需要突破自我、世俗、自然三层束缚后才能真正随心所欲地做任何事情，但人身为自然规律演化出的产物，“自然”不可能打破自然之道。仍然，人的一生总是走在破缚、解放的路上。尽管绝对自由不可达，但每层次的自由（如经济自由、上下班自由）都会带来极高的正反馈，促使人们追寻。

“这个 — 这个软件要 — 要收费吗？”直冲的河南话打散了我的思绪。只见村医上身略微转向了我们，但双目始终盯着显示屏上正在生成的文字。

“不不不，我们这个是公益项目，主要是学了这么多技术想真的把他用上，向社会做些贡献。”我急忙解释道，生怕他产生顾虑，认为我们别有所图，“这个软件永远是免费的，我们保证是永远免费。”

我们并没有把“科技平权”的目标挂在嘴边 — 人们可能无法同感它的重要性，更无法理解高中生（甚至任何人）追求它的目的，而显得我们在大力宣扬浮夸的名词以获得名利。在功利主义、骗术纷乱的社会背景下（或许这只是我作为即将申请的高中生所见到的社会），这些“高尚的觉悟”令人嗤之以鼻，好似它们仅是饰掩一些功利目标的面纱，稍微暴露在光之下便会透出网纱后对钱、权、名的追求。我们尽量“接着地气”，只说是为社会做些贡献，是学生在做社会实践。

村医满意地点点头，身子又转向了屏幕。木凳的四角与坚硬的水泥地摩擦，“噌噌“做响。

我与同行相视一笑，与村医作别后便掀开珠链，迈步踏出了略许昏暗的小室。

---

在这幢木屋檐、单层水泥平房中的经历是这次中牟探访的缩影。十间村卫生所共十三位村医，他们大多都未曾听闻“人工智能”一词，但互联网的普及拔高了他们对电子事物的接受度，而脑海里的医学知识又让他们验证了“康尔”的可行性，并因此愿意使用、相信、甚至帮助推广这软件。走访过程十分顺利，平均二十分钟就能探问完一间村所，也并没有遇到软件被拒之门外的情形 — 这般顺利是我在出发前始料未及、梦寐以求的。

同样大开眼界的是中国乡村公共医疗卫生系统的发展。“赤脚医生”的时代早已落幕，如今的从业者都是拥有专业资格证、受定期培训的“村医”。他们也从光着脚、亲自踩着田野路上门医治的“郎中”，变成了在诊所里坐堂的大夫，用上了专业的电脑和村医管理系统，药柜上摆满了各色中西药。村所的分布十分密集，我们走访时每两所间的平均路程不超十五分钟，有些直线距离甚至仅少数公里。2022年，中国共有136.7万村卫生室工作者，其中执业（助理）医师和持乡村医生证的人员共114.1万人。同时，中国约有50.9万个行政村，平均一个村有2.2位持证村医（*2022年卫生健康事业发展统计公报*，2023）。然而，这般密度却仍使陪同我们的疾控中心站长忧心忡忡：

“这狼城岗镇共有大概四万居民，注册村医有不到四十人，但许多都是挂个名，经常在外面跑但不在村所里的。真正一直在岗的也就二十来人，要服务四万人，这还是有些心有余而力不足啊。”

诚然，统计数据只能说明概况，却无法涵盖个体偏差，尤其对于河南这个人口大省。没有调查，没有发言权。实地走访也是“调查”的关键。这便是我决定亲自进乡推广“康尔”的最大推手 — 能实地目睹村医的反应，亲身体会乡村的生存、工作环境，才能设计出更符合需求的产品，更精准、高效地推动弱势群体的技术平权。

回程的轿车快速地穿梭在田野间的水泥路上，窗外是金灿灿与绿油油。平原地貌孕育了一望无际的耕地，在这玉米与麦子成熟的季节结满了丰收的果实。带着草帽的爷爷奶奶惬意地穿过片片农田，为这纯色、单调的背景增添了人的灵动。

麦秆倾斜着立在空中，在视野中成片的迅速倒退，空中留下金黄的残影。阳光洒下，麦子被光芒依稀环绕，闪闪发亮。

太阳仍高挂在空中，但它将身子往下略挪一二，更近地照耀着我们。一阵刺眼，我转头望向了前方空阔、宽大的车道。尽管轿车仍在不停向前行驶着，但这路却望不到尽头。

路漫漫其修远兮，吾将上下而求索。

---
### Technical Updates (2024-06-03)
I am dedicated to continuously perfect the app so that it can reach a larger audience and realistically help people in the underpriviledged areas. Four core features of KangEr have been updated to enhance accuracy and accessiblity.

#### 1. More powerful LLM Backbone
IFlyTeck has just released a new version of their LLM, `iFlyTekSpark-3.5`, which, as announced by the company, has a comparable performace with the state-of-the-art `gpt4-turbo` (although in practice the qualitative result lacks a bit). The new model has been integrated into KangEr. The system prompt ability also comes with the new API, and, by rounds of prompt engineering, I finally managed to make the model generate responses adhering to the healthcare aspect (as previously it will generate irrelevant content). The new backbone is exceptional in generating longer responses and answering multi-round questions, which are foundamental for a more holistic understanding of the problem and for diving deeper into a specific issue.

#### 2. More accessible Speech-to-Text and Text-to-Speech APIs
Since KangEr mainly focuses on rural areas, where the literacy rate is relatively low, voice accessiblity becomes a crucial ability. The previous version handles this issue with two local Flutter packages, `flutter_tts` and `speech_to_text`, which, on most devices, are working fine. However, these packages function through calling the local STT or TSS APIs of the browser or the phone, but many relatively cheaper devices in rural areas would lack these API. Hence, I decide to integrate Baidu's STT and TTS APIs, which are more robust and can be accessed through the web. These cloud-based APIs are not only device-independent but also more able in (i) detecting longer sequences and (ii) generating natural voices. 

Baidu's APIs are the choice I made due to its cost-efficiency and connectivity in China, comparing to the iFlyTeck's and the Azure's. Several tetchnical difficulties should been mentioned when interating the APIs. The documentation doesn't mention that the API endpoints practice CORS policy, and hence I have to set up a proxy server to bypass the restriction. Also, many Flutter packages are not optimized for web, and hence I have to write raw code to query the Media APIs of the browser for playing audio. The Media API doesn't work for audio recording used for STT, as it records in the `.webm` format which is not supported by Baidu's API, yet the conversion is difficult. Hence, I use the `record` package for recording. Notably, the `record` package doesn't work for Flutter web app built with `--web-renderer` set specifically to `canvaskit`, but the `auto` setting works fine even though it still uses `canvaskit` for desktop devices. Another technical detail is that the `flutter-svg` package, when the rendering engine is `html`, will directly use the color specified by the `fill` property in the SVG file for any image, instead of using the color specified by the `color` property in the `SvgPicture` widget. Hence, I have to manually change the color in the SVG file to make the image look good.

Sadly, Safari on MacOS seems to have a bug that doesn't allow voice to be accurately captured and transcribed through STT, yet, fortunately, this bug doesn't occur on any other browser or device. I am still investigating the issue.

#### 3. Variable Font Size
KangEr aims at a diversed user group covering different age groups and education levels. Hence, the font size should be adjustable to cater to the needs of different users (e.g., the elderl who needs large fonts or the visually imparied). The previous version uses a fixed font size and the font size is 12pt for body text and 14 pt for titles, which is not user-friendly. I have updated the app to allow users to adjust the font size, in real time, smoothly with a slider. The font size can be adjusted from 10px to 20px for body texts, as larger fonts will crowd the screen and make it unreadable. The font size is stored in the local storage of the browser, and the app will remember the user's preference when they revisit the app. Users will be directed to the help and setting page immediately when they first visit the app, where they can adjust the font size.

#### 4. Adaptive Rendering Engine
Frankly speaking, the biggest drawback of KangEr is its long initial waiting time for the web app to build, arised due to Flutter Web's inefficiencies. I've always tried to mitigate this issue. Previously, both desktop and mobile devices use the same rendering engine, `canvaskit`, which is not optimized for mobile devices and require a relatively long rendering time, despite better rendering quality and colors. The updated version of KangEr will use `html` as the rendering engine for mobile devices, with `canvaskit` still as the engine for the desktop platform, which is more local and will significantly reduce the initial waiting time. The rendering quality will be slightly reduced (and some components don't even have a right color), yet the deficiency is indetectable for most users as KangEr's UI is relatively straightforward.
