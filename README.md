# Awesome Bias and Fairness Datasets and Benchmarks in Language Models

---

# 🔍 Contents
- [💡 Acknowledgement](#-Acknowledgement)
- [Datasets and Benchmarks](#dataset1)
- [Metrics](#metrics)
  - [Counterfactual input](#counterfactual-input)
  - [Prompt input](#prompt)

---



# 💡 Acknowledgement

Thanks to the contributions of Zhiting Fan and Ruiling Xu at Zhejiang University. This repository is sponsored by the ZJU-AI4H Lab at Zhejiang University.


# Datasets and Benchmarks
| Dataset | Number of Data | Year | &emsp；Description &emsp；| Category/Task | Targeted Social Group | Input | Category of Metrics | Paper| Dataset Link |
| :---: | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **Winogender**  | 720 | 2018 | 揭示模型根据代词性别将代词识别为与特定职业相关的情况<img src="./imag/Winogender1.png" /><img src="./imag/Winogender1.png"> | Masked Tokens | gender | Counterfactual input | Probability-Based | Gender Bias in Coreference Resolution | [Link](https://github.com/rudinger/winogender-schemas/tree/master/data) |
|  **Winobias**   | 3160 | 2018 | | Masked Tokens | gender | Counterfactual input | Probability-Based | Gender Bias in Coreference Resolution: Evaluation and Debiasing Methods | [link](https://github.com/uclanlp/corefBias/tree/master/WinoBias/wino/data) |
|  **GAP**   | 8908 | 2018 | 一个性别平衡的标记语料库，包含 8,908 个模糊代词-名称对 <img src="./imag/GAP.png"> | Masked Tokens | gender | Counterfactual input | Probability-Based | Mind the GAP: A Balanced Corpus of Gendered Ambiguou | [link](https://github.com/google-research-datasets/gap-coreference) |
|  **BUG**  | 109419 | 2021 | 在来自三个领域的语料库获取包含刻板和非刻板性别角色分配（例如女护士与男舞者）的语法模式，从而产生了第一个包含 108K 不同现实世界英语的大规模性别偏见数据集句子。<img src="./imag/BUG.png">  | Masked Tokens | gender | Counterfactual input | Probability-Based | Collecting a Large-Scale Gender Bias Dataset for Coreference Resolution and Machine Translation | [link](https://github.com/SLAB-NLP/BUG) |
|  **StereoSet**  | 16995 | 2021 | 对于每个social group编写刻板印象、反刻板印象和不相关的属性词。提供包含目标术语的上下文填空句，其中的空白可以用刻板印象术语或反刻板印象术语来填充，但不能用不相关的术语来填充。<img src="./imag/StereoSet.png" height="200%" width="200%">  | Masked Tokens | gender, race, religion, others | Counterfactual input | Probability-Based | StereoSet: Measuring stereotypical bias in pretrained language models | [link](https://github.com/moinnadeem/StereoSet) |
|  **BEC-Pro**  | 5400 | 2020 | | Masked Tokens | gender | Counterfactual input | Probability-Based | Unmasking Contextual Stereotypes: Measuring and Mitigating BERT's Gender Bias | [link](https://github.com/marionbartl/gender-bias-BERT) |
|  **WinoQueer**  | 包含 45540 个句子对，涵盖 11 个模板句子、9 个酷儿身份组、3 组代词、60 个常用名称和 182 个独特谓词。| 2023 | 根据 CrowS-Pairs配对句子偏差检测构建。<br> 模版样例: I don’t like <name> because they are <identity>.<img src="./imag/WinoQueer.png"> | Unmasked Sentences | Sexual-Orientation | Counterfactual input | Probability-Based | WinoQueer: A Community-in-the-Loop Benchmark for Anti-LGBTQ+ Bias in Large Language Models | [link](https://github.com/katyfelkner/winoqueer/tree/main/data) |
|  **CrowS-Pairs**  | 1508 | 2020 | 一组数据包含两个句子：对优势群体的刻板印象和对弱势群体的反刻板印象，它们之间唯一变化的单词是那些标识所谈论的群体的单词。用于**测量模型相对于反刻板印象的句子倾向于刻板印象句子的程度**。<img src="./imag/CrowS-Pairs.png"> | Unmasked Sentences | Age <br> Disability <br> Gender <br> Nationality <br> Physical Appearance <br> Race <br> Religion <br> Sexual-Orientation <br> Other | Counterfactual input | Probability-Based——Pseudo-Log-Likelihood | Probability-Based——Pseudo-Log-Likelihood | [link](https://github.com/nyu-mll/crows-pairs) |
|  **RedditBias** | 11873 | 2021 | **人类标注者**对检索到的评论和对应的目标术语上下文进行标注，**判断是否表达了负面的刻板印象偏见或是否存在包含偏见的短语。** <img src="./imag/RedditBias.png "height="400%" width="400%"> | Unmasked Sentences | Gender <br> Race <br> Religion <br> Sexual-Orientation | Counterfactual input | Classifier | RedditBias: A Real-World Resource for Bias Evaluation and Debiasing of Conversational Language Models | [link](https://github.com/umanlp/RedditBias/tree/master/data) |
|  **RealToxicityPrompts**  | 100,100 | 2020 | 一个由 10 万个自然发生的句子级prompt组成的数据集，这些prompt源自大量英语网络文本语料库 <img src="./imag/RealToxicity.png"> | Sentence Completions | Other | Prompt | Classifier <br> 与来自广泛使用的毒性分类器的毒性分数配对 | RealToxicityPrompts: Evaluating neural toxic degeneration in language models. | [link](https://github.com/allenai/real-toxicity-prompts/tree/master/data) |
|  **BOLD**  | 23,679 | 2021 | 从维基百科收集英文prompt，抓取相关句子。例如，对于每个职业，选取句子的前 8 个单词中提到该职业的句子，从而截断句子以获得prompt | <img src="./imag/BOLD.png"> | Sentence Completions | Gender <br> Religion <br> Race <br> Other | Prompt | Lexicon <br> 利用情绪、毒性、尊重和情感词典作为衡量标准，计算相关评分衡量模型生成质量。| | |
|  **TrustGPT**  | 9* | 2023 | 提供评估社会群体之间表现差异的prompt <img src="./imag/TrustGPT.jpg"> | Sentence Completions | Gender <br> Religion <br> Race <br> | Prompt | Classifier <br> 采用三个指标来评估 LLM 的偏差：各个组的平均毒性；不同组类型的标准差；从对不同组的毒性分布进行的 Mann-Whitney U 检验获得的 p 值。| TRUSTGPT: A Benchmark for Trustworthy and Responsible Large Language Models | [link](https://github.com/HowieHwong/TrustGPT/tree/master/bias) |
|  **HONEST**  | 420 | 2021 | 提供 420 个句子句子完成中的负面性别刻板印象。每个句子都遵循基于完形填空的形式，提示中带有性别身份术语，可以通过提示自由文本延续来完成；也可以通过替换单个 [MASK] 令牌来完成完成，这可以与基于masked-token的指标兼容 <img src="./imag/HONEST.png"> | Sentence Completions | Gender | Prompt | Lexicon / masked-token的指标 | HONEST: Measuring hurtful sentence completion in language models. | [link](https://github.com/MilaNLProc/honest/tree/main/resources) |
|  **BiasAsker**  | 一个包含11个属性下的841个社会群体的综合社会偏见数据集；以及 12 个类别的 8,110 个社会偏见属性 | 2023 | BiasAsker 自动生成问题，并采用基于存在测量的新颖方法来识别会话系统中的两种类型的偏差（即绝对偏差和相关偏差）。<img src="./imag/BiasAsker.png"> | Question-Answering | Ability <br> Age <br> Body <br> Character <br> Culture <br> Gender <br> Profession <br> Race <br> Race <br> Religion <br> Social <br> Victim | Prompt | Classifier | BiasAsker: Measuring the Bias in Conversational AI System | [link](https://github.com/yxwan123/BiasAsker) |
|  **BBQ**  | 58492 | 2022 | 衡量一个模型何时依赖于刻板印象。问题要求一个社会群体要么符合消极的刻板印象，要么符合积极的刻板印象，其背景是模棱两可的 <img src="./imag/BBQ.png"> | Question-Answering | Age <br> Disability <br> Gender <br> Nationality <br> Physical <br> Appearance <br> Race <br> Religion <br> Sexual-Orientation <br> Other | Prompt | Classifier <br> **准确率评分** 将准确率分为两部分，即正确答案是否强化或违背了现有的社会偏见，以评估模型的表现是否受到社会偏见在回答问题时的影响。<br> **偏见分数** 引入了一个偏见分数来量化模型以一种有偏见的方式回答问题的程度。偏见分数反映了与社会偏见一致的非UNKNOWN输出的百分比 <img src="./imag/BBQ2.png"> | BBQ: A hand-built bias benchmark for question answering | [link](https://github.com/nyu-mll/BBQ) |
|  **UnQover**  | 30* | 2020 | 使用**不加明确描述**的问题来揭示下游问答模型中的刻板印象偏见。不加明确描述所以**没有支持任一选择的事实背景**，从而检测模型是否存在刻板印象，所有答案都表明存在刻板印象偏差 <img src="./imag/UnQover.png"> | Question-Answering | Gender <br> Nationality <br> Race <br> Religion | Prompt | Classifier | UNQOVERing Stereotyping Biases via Underspecified Questions | [link](https://github.com/allenai/unqover) |
|  **Grep-BiasIR**  | 118 | 2023 | 使用与性别相关的118个Query与708个document，其中一半的document与Query有关，另一半无关。从而更加深入的探索了检索系统的性别表示。<img src="./imag/Grep-BiasIR.png"> | Question-Answering | Gender | Prompt | NA | Grep-BiasIR: A Dataset for Investigating Gender Representation Bias in Information Retrieval Results | [link](https://github.com/gender-bias/gender-bias) |
|  **MGBR**  | | 2024 | 在给定由女性、男性和刻板职业单词组成的单词列表的情况下预测女性或男性单词的数量 <br>（利用“How many of the following words are definitely female/male?”进行提问) <img src="./imag/MGBR.png"> | Question-Answering | Gender | Prompt | Distribution | Evaluating Gender Bias in Large Language Models via Chain-of-Thought Prompting. | |
|  **Pythia**  | | 2023 | 一个更全面的评估套件 | NA | | NA | NA | Pythia: A Suite for Analyzing Large Language Models Across Training and Scaling | |
 
# Metrics <a id = "metrics"></a>

#### Counterfactual input

A. Masked Tokens

**Description** Masked Tokens数据集包含了语言模型必须填充的带有blank的句子。填空选项是预先指定的，如“他/她/他们”的代词，或者是刻板印象和反刻板印象选项。<br /> 
<div align=center><img src="./imag/Mask1.PNG" width="70%" height="80%" /></div>
<div align=center><img src="./imag/Mask2.JPEG" width="70%" height="80%" /></div>

**Metrics** 这些数据集最适合使用masked token probability-based metrics，或者使用pseudo-log-likelihood metrics来评估给定句子条件下的Masked Tokens的概率。在多个选择选项的情况下，也可以使用标准的指标，如Accuracy。<br />
<div align=center><img src="./imag/Mask3.PNG" width="70%" height="80%" /></div>

B. Unmasked Sentences

**Description** 基于Unmasked Sentences数据集的模型计算一组句子中哪个句子生成或被选中的概率最大。<br \>
<div align=center><img src="./imag/Mask4.JPEG" width="70%" height="80%" /></div>
<div align=center><img src="./imag/Mask5.PNG" width="70%" height="80%" /></div>

**Metrics** 该框架下的数据集于masked-token based数据集适用的度量指标相似，特别是pseudo-log-likelihood metrics，以衡量给定不同人口统计学术语的句子的概率。此外，这些数据集使用更多更灵活的度量方式，例如，句子对可以提示两个文本生成，这可以与生成的基于文本的度量进行比较。


#### Prompt
A. Sentence Completions

**Description** Sentence Completions 框架下将数据集改编为输入句子来条件文本的延续，指定句子中的前几个单词要求模型提供一个延续。这些数据集不是像反事实输入数据集那样使用人为设定的偏差触发器，而是匹配人类书写文本的分布，以模拟更多的自然语言使用和潜在的非目标偏见。
<div align=center><img src="./imag/Sentence Completions.PNG" width="70%" height="80%" /></div>

B. Question-Answering
**Description**Question-Answering框架下数据集被提出来作为prompt，提出一个问题并要求模型提供一个答案。
<div align=center><img src="./imag/Question-Answering.JPEG" width="70%" height="80%" /></div>

**Metrics** 
基于prompt框架数据集的模型多数采用Generated Text-Based Metrics，对于无法直接利用来自LLM的概率或嵌入的黑箱模型，它可以直接对LLM生成的文本进行评价。常见的方法是利用一组已知具有偏见或毒性的提示使模型生成有偏或有毒性的文本，基于上述结果测量模型的有偏程度。
1) Distribution Metrics  通过比较与一个社会群体相关联的标记与与另一个群体相关联的标记的分布，可以在生成的文本中检测到偏见。
2) Classifier Metrics  依赖于一个辅助模型来对生成的文本输出进行评分，以评估其毒性、情感或任何其他维度的偏差。如果从相似的提示中产生的文本，但具有不同的社会群体，则可以检测到偏见。
3) Lexicon Metrics  对生成的输出进行单词级别的分析，将每个单词与预先编译的有害单词列表进行比较，或者为每个单词分配预先计算的偏差分数。
<div align=center><img src="./imag/Question-Answering_Metrics.PNG" width="70%" height="80%" /></div>
