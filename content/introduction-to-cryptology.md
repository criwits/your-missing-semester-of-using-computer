---
title: 以密码之剑护网安之盾
type: docs
draft: true
---

# 以密码之剑护网安之盾

{{<hint danger>}}
本文正在施工中……
{{</hint>}}

{{< hint info >}}

{{< /hint >}}

今天的世界已经离不开网络，从我们的日常生活到政府各项事务的管理，从企业的高效运转到顶尖的科学技术，网络已经成为了这一切的基石。可是你是否想过，这个网络世界其实「危机四伏」？我们在网络上传输的信息，可以很轻易地被拦截和篡改；国与国之间、企业与企业之间，网络更已经成为「没有销烟的战场」。在这样的环境之下，密码学技术帮助人们保护信息的安全，而在此基础之上，人们构建起了网络安全的完整体系。

## 危机四伏的世界

网络世界之所以「危机四伏」，从某种意义上来说，和当今互联网的底层技术——「分组交换」——脱不了干系。

我们说网络连接了世界的每一个角落，但这种连接并不是「点对点」的直接连接，而是由许多结点之间相互连接进行「转发」的。事实上，网络之所以称为「网络」，正是因为它在结构上由许多「结点」张成。今天，我们可以使用网络与远在地球另一端的朋友交流，并不是因为我们之间用一根无比长的网线牵着，而是因为我们之间有许许多多相互连接的结点，它们在我们之间搭成了一条「通路」。

为了提升传输的效率，网络会将我们需要发送的数据「切」成许多一定长度的小片段。这些片段就像一个个快递包裹一样，流入一个个结点。每个结点如同快递转运中心，会根据片段上标记的「目的地」信息，将片段转发给去往目的地的下一个结点。就这样，经过一次又一次的转发，我们的数据片段最终都会抵达终点，并被重新组装为完整的数据。这种传输方式被称为「分组交换」，它奠定了互联网的传输基础。

这个过程看似十分完美，但在实际上充满危机。数据在网络上传输时可以很轻易地被截获，甚至对它们进行修改也不是什么难事。攻击者只需攻击、控制网络中的一个结点，所有经过它的数据片段都将被一览无余。在此之上，攻击者还可以修改数据片段里面的内容，使得最终发送到目的地的数据被篡改；或者将数据「拦下」，让目的地收到不完整的信息甚至完全收不到数据。攻击者甚至可以伪造我们的名字，以我们的名义发送伪造的信息，从而造成具有破坏性的后果。

如果将数据加密，这些问题就能得到一定程度的解决。加密后的信息即使被截获，攻击者也无法得知其中内容，更无从谈及篡改和伪造。密码技术的发展，让高效的加密成为了可能。接下来，让我们推开密码世界的大门，领略今天的密码之「剑」如何铸成。

## 蓬勃发展的密码学

### 人类的「传统艺能」

几千年来，人类的交锋见证了密码学的发展，从古代战场间的传令、军中机要情报的转移、能工巧匠家里的祖传秘方，到如今网络世界的信息流转……种种危机四伏的场景，如何让这些重要信息不被不相关的人员所知晓，便是这种「仅有我认识」的文字技艺的用武之地了。跨越几千年的时间长河，我们从头来看「密码」的力量如何铸就诸多信息的安全无虞。

<p style="font-size: 6px; font-weight: 100; color: lightgray; text-align-last:justify; margin: -4px">S t e g a n o g r a p h y</p>
让我们首先把目光投向密码学的孪生兄弟——「隐写术」（Steganography）。
「隐写术」，顾名思义，就是把重要信息「隐藏着写下来」，让读它的人基本不会注意到重要信息的手段。虽然它不算一种密码，但在「使信息对不知道的人来说很难看出来」这方面，它和密码是一样的。
古罗马的古典诗人奥维德就曾记录过用新鲜牛奶写信的隐写术——这样写在纸上的字很快就会消失不见，但是如果点燃字迹的一角，就可以将字迹显现出来。除了牛奶外，一些植物汁液、明矾、果汁等也被用作隐形墨水。另外一些隐写术则和今天学生的小抄有些类似——将信息写在树叶上、衣服里或是身体上，再运用多种方法进行遮掩。

与隐写术相比，密码学（Cryptography）的目标，则是将内容「变换」，使之变成常人看不懂的模样。公元前 5 世纪，古代的斯巴达人使用过一种叫做「密码棒」的器械，那是一根上面缠绕有羊皮纸条儿的木棍。人们把信息竖着写在羊皮纸条儿上，写完后将其从木棍上取下，原本的字母顺序就被打乱，难以再看出原本的信息。需要阅读时，只需取一根同样规格的木棍，将羊皮纸重新缠绕即可。这种密码棒是人类历史上已知的最早的密码器械。

据说古罗马的凯撒大帝使用过这样一种方法来保护重要的军事信息：将每个字母向后移动 3 位。例如，需要传递的信息是

```text
AMICUS PLATO, SED MAGIS AMICA VERITAS
```

将每个字母后推 3 位，即 A 变成 D，B 变成 E……可以得到下面的句子：

```text
DPLFXV SODWR, VHG PDJLV DPLFD YHULWDV
```

若不知道这种方式的具体细节——甚至，即使知道采用移动字母的方式，如果不知道具体移动的长度，他人就很难从后面这个句子猜出原本的内容。这种密码被称为「凯撒密码」。

在这些例子中，原本的可以直接理解的信息称为「明文」，经过处理后，难以理解的信息被称为「密文」。将明文转换为密文的过程被称为「加密」，而反向的过程就是「解密」。在加密和解密过程中，需要使用称为「密钥」的额外信息——就像一把钥匙一样，加密需要使用它，解密也需要用到。例如，对于密码棒来说，密码棒的尺寸信息是密钥。而对于凯撒密码，移动长度 3 这个数字就是它的密钥。

在古代，人们还发明过许多其他有趣的加密方式，如维吉尼亚密码。

密码学伴随着人们保密意识的产生而诞生，然而直到 20 世纪 50 年代，密码学的本质并没有什么变化。各种加密方式都可以归类为「代换」和「置换」两种变换或它们的组合：「代换」指的是「用一种字母替代另一种字母」，而「置换」指的是「变更不同字母的位置」。上文提到的密码棒就是一种置换代码，而凯撒密码是一种代换密码。

这一时期的密码的安全性，来源于代换和置换的精巧设计；而这样的设计，则基于经验或直觉。因此，此时的密码学更像是一门「艺术」——比起严格的论证，它的主观性更强。同时，这些密码大多可以通过频率分析的方法进行破解：由于文章、句子中不同字母的出现频率是存在规律的，通过对密文中字母的分布进行分析，就有可能反推出密码所使用的置换方式。现在，我们把这整个时期的密码学都称为「古典密码学」，而相关的密码则称为「古典密码」。

1949 年，美国数学家、工程师香农的《保密系统通信理论》（Communication Theory of Secrecy Systems）从数学和信息论的角度阐明了关于密码系统的分析、评价和设计的科学思想，提出了有关密码学的完整数学模型。