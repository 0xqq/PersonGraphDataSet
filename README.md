# PersonGraphDataSet
PersonGraphDataSet, nearly 10 thousand person2person relationship facts that build from extraction method, which can be applied to person kg search and inference applications。  人物图谱数据集，近十万的人物关系图谱事实数据库，通过人物关系抽取算法抽取+人工整理得出，可用于人物关系搜索、查询、人物关系多跳问答，以及人物关系推理等场景提供基础数据。

# 项目由来
关于为什么要开放这个项目，主要有以下几个方面的缘由：  
1、阶段性总结。以刻画人物复杂关系为核心的网络关系网构建，居于十分重要的现实意义，两年前，带着个人兴趣，发布了一个未完成版的人物关系知识图谱项目(https://github.com/liuhuanyong/PersonRelationKnowledgeGraph)，    尝试采用基于知识库的数据回标,基于远程监督与bootstrapping方法的人物关系抽取，并以此完成基于知识图谱的知识问答等应用。但但由于工作时间为题，一直没能更新。今天，先对该工作的一个结果数据集开放出来，以对之前的项目做一个阶段性的总结。  
2、数据集空缺。目前，面向中文领域的人物关系抽取数据集，还相对较少，代表性有ccks2019的开放数据集（https://arxiv.org/abs/1907.12801） ，该数据集公开了亲属关系、社交关系、师生关系三大类，现夫、潜伏、朋友、恋人等34小类的人物关系数据集。该数据集是面向评测使用的，其所涉及的人物关系类型有限，并且不提供现成可用的人物关系数据。  
3、应用驱动。当前，面向知识图谱入门级别的知识图谱推理、知识图谱可视化、知识问答、图谱搜索等场景，还缺乏可用的数据集。目前关于人物关系方面的应用，目前看到的，主要是百科类的展示以及搜狗人物图谱（https://www.sogou.com/tupu/person.html） 为代表，虽说是娱乐导向，但目前还缺乏这样的练手的数据和项目。  
4、应用支撑。基于开放出来的人物关系知识数据，大家可以在此基础上进行多种应用尝试，包括算法训练、知识图谱入门、培训等等，这十分有意义。  
 
# 项目构成
本项目一共包括三个文件，分别记录人物关系元组信息以及关系类型信息：  
1、big_rel_distribution.txt：大类关系及其分布文件。  
2、person_rel_kg.data：人物关系图谱数据集文件。    
3、small_rel_distribution.txt：小类关系及其分布文件      

# 数据概况
本数据集，一共包括97,158条人物关系数据，涉及人物71,243个，大类关系102个，小类关系266条，大致的情况具体如下：    

| 数据类型 | 数据规模 | 示例 |
| :--- | :---: | :---: |  
| 关系数目 | 97,158 | 父亲、母亲、女友 | 
| 人物数目 | 71,243 | 姚明、易建联、乔布斯 | 
| 大类关系数 | 102 | 父亲、母亲、朋友 | 
| 小类关系数 | 266 | 闺蜜、女好友、前妻 | 

# 关系类型
本数据集对人物关系进行了上下级分类，针对小类关系进一步归类整理成了若干个大类，选取小类数大于3的大类进行展示，如下表所示：
| 关系大类 | 关系小类 |
| :--- | :--- |
|敌人|死敌;传闻不和;竞争对手;死对头;敌人;对手;骂战|
|父亲|父亲;其父;继父;生父;干爹;义父;养父|
|学生|学生;爱徒;徒孙|
|合作|同伙;合作人;相声搭档;合作演员;合作;影视搭档;戏曲搭档;搭档;同时期队友;前队友;队友;国家队队友;女双搭档;主持搭档;合作伙伴;盟友;戏曲合作;混双搭档;合伙人|
|情人|初恋;配偶;情侣;情人;伴侣;情敌;旧爱;情夫;爱人;前任;恋人;心上人;分手|
|朋友|圈中好友;同伴;密友;友人;伙伴;好友;圈内好友;红颜知己;挚友;女好友|
|丈夫|未婚夫;第二任丈夫;现任丈夫;前夫;第一任丈夫;丈夫|
|祖先|祖先;鼻祖;始祖;先祖|
|姐姐|大姐;二姐;姐姐|
|妻子|妻妾;第二任妻子;现任妻子;第三任妻子;未婚妻;前妻;妻子;第一任妻子|
|同门|同门师兄;校友;师妹;师弟;师兄弟;师姐|
|弟弟|义弟;三弟;弟弟;五弟;四弟;六弟;胞弟;二弟|
|女儿|女儿;继女;大女儿;养女;次女;干女儿;义女;三女;长女;二女儿;小女儿|
|儿子|四子;三子;大儿子;干儿子;儿子;次子;五子;继子;义子;小儿子;二儿子;养子;幼子;长子|
|哥哥|三哥;哥哥;长兄;二哥;四哥;大哥;五哥|
|家人|亲戚;家属;亲属;近亲;亲人;孩子;家人;长辈|
|老师|启蒙教练;师祖;师;师叔;师承;老师;现任教练;教练;班主任;伯乐|
|母亲|义母;生母;养母;继母;干妈;母亲|
|下属|下级;下属;属下;部下;君臣|
|同学|同班同学;同学;同门|
|继任者|继任者;后裔;继承人;后人;后代;继任|
|偶像|喜欢的演员;最喜欢的歌手;喜欢的歌手;偶像|
|妹妹|义妹;二妹;三妹;妹妹|

# 数据分布
目前，共涉及大类关系102个，小类关系266条，大类的top20样例如下：
| 关系类型 | 关系规模 | 示例 | 关系类型 | 关系规模 | 示例 |
| :--- | :---: | :---: |:--- | :---: | :---: |   
| 合作 | 14,048 | <左永邦,合作演员,合作,王珞丹> |哥哥 | 2,379 | <周星霞,哥哥,哥哥,周星驰> |  
| 朋友 | 13,632 | <祖孙登,好友,朋友,张正见> |学生 | 2,017 | <左宏元,学生,学生,邓丽君> |  
| 父亲 | 6,857 | <左太北,父亲,父亲,左权> | 敌人 | 1,948 | <左武王,死敌,敌人,诸葛正我> | 
| 丈夫 | 5,348 | <左蓝,未婚夫,丈夫,余则成> | 弟弟 | 1,880 | <祝龙,弟弟,弟弟,祝彪> | 
| 情人 | 4,880 | <庄睿,爱人,情人,秦萱冰> | 同学 | 1,695 | <祖峰,同学,同学,黄晓明> | 
| 老师 | 4,727 | <左欣然,老师,老师,许蕙兰> | 女友 | 1,427 | <邹世龙,前女友,女友,梅艳芳> |
| 儿子 | 4,631 | <左武王,儿子,儿子,安祯侯> | 妹妹 | 1,384 | <祝齐英,妹妹,妹妹,祝英台> |
| 妻子 | 4,491 | <祖峰,现任妻子,妻子,刘天池> |姐姐 | 1,149 | <卓龙,姐姐,姐姐,卓凤> |  
| 母亲 | 3,832 | <卓玥,母亲,母亲,邓榕> | 子女 | 977 | <朱寿,子女,子女,朱厚熜> |
| 女儿 | 2,583 | <宗庆后,女儿,女儿,宗馥莉> | 祖父 | 962 | <周璟馨,祖父,祖父,周海婴> |

# 数据样例
1、数据格式为：<人物1,小类关系,大类关系,人物2>，为四元组形式，以满足不同的数据需求。  
2、注意：为了对存在歧义的实体，采用了实体[实体简短描述]的方式进行区分处理。
3、样例数据：  

    """
        周洋,队友,合作,孙琳琳
        周洋,队友,合作,王濛
        周洋,队友,合作,张会
        周洋,启蒙教练,老师,崔顺子
        周洋,老师,老师,李琰
        周扬[中国内地女演员],搭档,合作,叶童
        周扬[中国内地女演员],好友,朋友,蒋欣
        周扬[中国内地女演员],同学,同学,黄渤
        周扬,搭档,合作,高圆圆
        周扬,搭档,合作,叶童
        周扬,好友,朋友,蒋欣
        周扬,好友,朋友,霍思燕
        周扬,好友,朋友,佟丽娅
        周扬,同学,同学,黄渤
    """
# 数据应用
拥有了刻画人与人之间的复杂关系数据集，可以支撑包括知识问答、多跳推理、图谱可视化、未知关系推理、数据回标、特征增强、人物推荐、人物建模等多种应用尝试和科学研究：     
| 大类场景 | 小类场景 | 应用举例 |
| :--- | :---: | :---: |  
| 信息检索 | 知识问答 | 姚明的老婆是谁？ | 
| 信息检索 | 多跳推理 | 姚明的女儿的爷爷是谁？ | 
| 信息检索 | 图谱可视化 | 将数据导入图数据库，进行图谱可视化展示 | 
| 信息检索 | 未知关系推理 | 给定两个人物节点，进行人物之间的潜在关联路径发现 | 
| 信息抽取 | 数据回标 | 根据结构化人物关系数据，利用远程监督方法进行回标 | 
| 信息抽取 | 特征增强 | 根据结构化人物关系数据，将用户的关联关系作为某个用户的某个特征 | 
| 信息推荐 | 人物推荐 | 根据关注某个人物，类推出与该人物相关的其他人物 | 
| 用户画像 | 人物建模 | 利用某个人物的关联信息，对其进行特征表示和画像建模 | 

# 项目总结
1、本项目开放了一个人物关系知识图谱数据集，一共包括97,158条人物关系数据，涉及人物71,243个，大类关系102个，小类关系266条。  
2、本项目采用了数据格式为：<人物1,小类关系,大类关系,人物2>，为四元组形式，可以满足不同的数据使用需求。  
3、基于本项目，可以支撑包括知识问答、多跳推理、图谱可视化、未知关系推理、数据回标、特征增强、人物推荐、人物建模等多种应用尝试和科学研究工作。    
4、本项目面向开放文本，采用人物关系抽取模型进行抽取形成，经人工矫正后，可以保证数据的质量。  

# 关于作者

刘焕勇，中国科学院软件研究所，专注金融、情报两大领域，从事事件抽取、事件演化、情感分析、事理（知识）图谱、常识推理、语言资源构建与应用等研发工作。如有自然语言处理、知识图谱、事理图谱、社会计算、语言资源建设等问题或合作，可联系我：  
1、我的github项目介绍：https://liuhuanyong.github.io  
2、我的csdn技术博客：https://blog.csdn.net/lhy2014  
3、我的联系方式: 刘焕勇，中国科学院软件研究所，lhy_in_blcu@126.com.  
4、我的共享知识库项目：刘焕勇，数据地平线，http://www.openkg.cn/organization/datahorizon.  
5、我的工业项目：刘焕勇，数据地平线，大规模实时事理学习系统：https://xueji.datahorizon.cn.  
6、我的工业项目：刘焕勇，数据地平线，面向事件和语义的自然语言处理工具箱：https://nlp.datahorizon.cn  
