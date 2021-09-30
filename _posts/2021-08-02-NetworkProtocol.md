---
layout: post
title:  "计算机网络协议全面总结"
date:   2021-08-02 14:49:23
categories: 转 网络协议
tags: 转 网络 协议 计算机网络 Protocol Network
---

<p align='center'>
<a href="https://blog.csdn.net/LiangJGo/article/details/90080011" target="_blank" ><img height="50" src="https://img.shields.io/badge/-计算机网络协议全面总结 原址-F08080" alt="计算机网络协议全面总结 原址"/></a>
</p>

<div id="content_views" class="markdown_views prism-atom-one-dark">
                    <svg xmlns="http://www.w3.org/2000/svg" style="display: none;">
                        <path stroke-linecap="round" d="M5,0 0,2.5 5,5z" id="raphael-marker-block" style="-webkit-tap-highlight-color: rgba(0, 0, 0, 0);"></path>
                    </svg>
                    <h1><a name="t0"></a><a name="t0"></a><a id="_0"></a>计算机网络协议全面总结</h1> 
<h2><a name="t1"></a><a name="t1"></a><a id="OSI_2"></a><strong>一、OSI七层协议</strong></h2> 
<p><strong>物理层：</strong><br> 很久很久以前，那时候还没有现在的外星人超级电脑，或者华为的P30。比较调皮的小明想要把自己机器上写好的一些个人游戏心得（如何玩好王者农药）发给小红（校花），希望博得芳心。小明个人比较勤，游戏总结心得总结的比较详细（大概有100M）。但是到底怎么才能从自己的机器上传给小红的机器呢，进过一番打听，他发现远在太平洋另一端的科学家已经发明了一种技术 <strong>物理层</strong>，专门用来解决小明这种单身狗问题。<strong>该层主要定义物理设备标准，如网线的接口类型、光纤的接口类型、各种传输介质的传输速率等。它的主要作用是传输比特流(就是由1、0转化为电流强弱来进行传输，到达目的地后在转化为1、0，也就是我们常说的数模转换与模数转换)。这一层的数据叫做比特。</strong><br> 他很兴奋，通过一个月的努力终于搭建起了这个物理层。</p> 
<p><strong>数据链路层：</strong><br> 然而上天却好像和小明开了一个玩笑，楼下的小润发超市的网线、光纤最近卖光了，但是这个物理层传输数据只能通过网线传输。到底怎么办！！。<br> 此时，他体内的雄性激素促使着他的大脑以光速运转。终于他饿了，无奈得走去学校饭堂三楼吃麻辣烫。此时听到隔壁坐着的那位王叔叔（老王）说，科学家已经发明了一种技术可以通过无线电来传输。What？这不是完美解决了自己的困扰吗。小明连忙对隔壁老王说谢谢，老王留下了幸福的泪水！！<br> 右通过一番努力查资料，小明发现：<strong>这种技术可以通过电线我能发数据流，也可以通过其它介质来传输。然后还要保证了传输过去的比特流是正确的，有纠错功能。定义了如何让格式化数据以进行传输，以及如何让控制对物理介质的访问。这一层通常还提供错误检测和纠正，以确保数据的可靠传输。</strong><br> 小明把层技术称为：<strong>数据链路层</strong></p> 
<p><strong>网络层：</strong><br> 由于小明家离小红家比较远，无线电信号无法传输到哪里，但是这完全难不到小明。他通过在离小红家的路上搭建了多个节点（路由器，交换机），用于信号的传输。但是由于他有时候被雄性激素冲昏了头脑，搭建的信号节点有点乱，而且很多。那他又想用最短的路径来传输怎么办呢？在小明沮丧走回家的时候已深夜，他看见今天看到的那位王叔叔匆匆的从自己家走出来，他连忙拉住王叔叔，向他诉说自己的烦恼，希望王叔叔能给自己一些帮助。当小明说完后，王叔叔从紧张变为和蔼，和小明说：其实已经有人<strong>发明了网络层。即路由器，交换机那些具有寻址功能的设备所实现的功能。这一层定义的是IP地址，通过IP地址寻址。所以产生了IP协议。该层能选择最佳路径，这就是路由要做的事。</strong></p> 
<p><strong>传输层</strong><br> 为了趁热打铁，小明通宵查资料来学习相关信息，并且简单搭建好网络层，开始传输数据，趁着传输过程好好睡一觉。当他起来的时候，噩梦才刚刚开始，因为他传输的数据太大（100M）只传输了一部分，而且断断续续的，有一部分数据根本传不出去。那怎么办？<br> “加一层传输层！！！”：王叔叔在楼下大声喊着，“资料在你妈妈的床头柜”，王叔叔继续说。小明连忙找到资料，上面写着：“<br> <strong>发正确的发比特流数据到另一台计算机了，但是当我发大量数据时候，可能需要好长时间，例如一个视频格式的，网络会中断好多次（事实上，即使有了物理层和数据链路层，网络还是经常中断，只是中断的时间是毫秒级别的）。<br> 那么，我还须要保证传输大量文件时的准确性。于是，我要对发出去的数据进行封装。就像发快递一样，一个个地发。<br> 例如TCP，是用于发大量数据的，我发了1万个包出去，另一台电脑就要告诉我是否接受到了1万个包，如果缺了3个包，就告诉我是第1001，234，8888个包丢了，那我再发一次。这样，就能保证对方把这个视频完整接收了。<br> 例如UDP，是用于发送少量数据的。我发20个包出去，一般不会丢包，所以，我不管你收到多少个。在多人互动游戏，也经常用UDP协议，因为一般都是简单的信息，而且有广播的需求。如果用TCP，效率就很低，因为它会不停地告诉主机我收到了20个包，或者我收到了18个包，再发我两个！如果同时有1万台计算机都这样做，那么用TCP反而会降低效率，还不如用UDP，主机发出去就算了，丢几个包你就卡一下，算了，下次再发包你再更新。<br> TCP协议是会绑定IP和端口的协议，下面会介绍IP协议。</strong><br> ”<br> 通过如此这般的操作，他！小明同学终于把自己100M的游戏心得发送给了小红</p> 
<p><strong>会话层(解除与建立与别的接口的联系)</strong><br> 然而，小红根本不玩游戏。得知这个消息后，小明楞逼了。但是他没有放弃，而是把自己猜到小红喜欢的信息都发给他，但是小明每发一次，<strong>难道我每次都要调用TCP去打包，然后调用IP协议去找路由</strong>，这一来一回就是一天，那怎么办呢？<br> 他又翻了翻王叔叔的笔记本资料，写着：<strong>会话层可以帮助我们建立和管理应用程序之间的通信，封装了调用TCP去打包，然后调用IP协议去找路由等操作</strong><br> 如此一来，他只需要十几二十分钟就能够成功搭建好传输数据的机器。</p> 
<p><strong>表示层(数据格式化，代码转换，数据加密)</strong><br> 有一次，小明传了一份数据，是关于如何选购化妆品的文章，小红对此非常感兴趣，但是当小红想用自己的window开该文件时发现根本无法打开，后来小红在下课的时候和小明说自己无法打开这个文件，小明想自己用Linux系统明明完整地发送给了小红啊，那就奇怪了，但是出于耍帅，小明只是轻轻地说“我放学后再发你一份！”。<br> 这时虽然小明不知道是出了什么问题，但是他坚信老王叔叔的资料笔记会有答案的。果然！上清清楚楚的写着：“<strong>现在我能保证应用程序自动收发包和寻址了。但是我要用Linux给window发包，两个系统语法不一致，就像安装包一样，exe是不能在linux下用的，shell在window下也是不能直接运行的。于是需要表示层（presentation），帮我们解决不同系统之间的通信语法问题。</strong>”<br> 小明立即用了一个通宵手动搭好了表示层，传输了一份完美的文件给小红</p> 
<p><strong>应用层(文件传输，电子邮件，文件服务，虚拟终端)</strong></p> 
<p>官方OSI说明图：<br> <img src="https://img-blog.csdnimg.cn/20190510165918512.jpg" alt="在这里插入图片描述"></p> 
<h2><a name="t2"></a><a name="t2"></a><a id="TCPIP_43"></a>TCP/IP协议</h2> 
<p>TCP/IP协议是由七层模型简化成四层而来。（TPC/IP协议其实泛指了四层模型中的全部协议，区别开TCP协议，IP协议）<br> 七层有底向上分别是：<strong>物理层、数据链路层、网络层、传输层、会话层、表示层、应用层。</strong><br> 简化后的四层分别是：<strong>主机到网络层（比特）、网络层（数据帧）、传输层（数据包）、应用层（数据段）。</strong><br> 每一层对于上一层来讲是透明的，上层只需要使用下层提供的接口，并不关心下层是如何实现的。</p> 
<p><strong>与OSI七层协议的对比：</strong><br> <img src="https://img-blog.csdnimg.cn/20190511221941704.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0xpYW5nSkdv,size_16,color_FFFFFF,t_70" alt="在这里插入图片描述"></p> 
<h3><a name="t3"></a><a name="t3"></a><a id="_52"></a>传输层：</h3> 
<p>网络层是主机与主机之间的通讯，而传输层则是进程之间的通讯。</p> 
<ul><li>为何要有传输层？<br> 应为进程是资源分配的基本单位，计算机之间的信息传输也只是一台计算机的进程传输到另外一台计算机的进程中</li><li>一台计算机如何找到另外一台计算机呢，那就是通过IP协议来完成的（复用，多个进程都可以把信息通过传输层到IP层，再传输到另外一台计算机中）。</li><li>那如何找到另外一台计算机的进程（pid）呢，那就是用端口（分用，到达另外一台计算机后还要通过端口号找到对应进程）</li></ul> 
<h4><a id="UDPTCP_60"></a>传输层主要有两种协议：UDP和TCP</h4> 
<h4><a id="UDP_62"></a>一、UDP协议</h4> 
<h5><a id="_63"></a>特点：</h5> 
<ul><li>无连接，传输数据时不需要建立连接，减小开销</li><li>尽最大努力交付，不确保可靠交付</li><li>面向报文</li><li>没有拥塞控制、确保信息实时性</li><li>支持一对一，一对多，多对一，多对多</li><li>首部开销小，只有8个字节</li></ul> 
<h5><a id="UDPUDP_71"></a>UDP的首部格式（UDP头）：</h5> 
<ul><li>源端口，发送方的端口</li><li>目标端口，接收方的端口</li><li>长度，首部长度 + 用户数据包的长度（可以没有数据包，所用最小值为8）</li><li>检验和，检查UDP用户数据传输中是否与错，有错就丢弃（检查首部长度 + 用户数据包）</li></ul> 


<!-- rowspan colspan --> 

<table align="center" bordercolor="#cccccc" cellspacing="0" cellpadding="0" border="1">
<tbody align="center" id="udp_head">
<tr align="center">
<td><strong>源端端口</strong></td>
<td><strong>目的端端口</strong></td>
</tr>
<tr align="center">
<td><strong>用户数据包长度</strong></td>
<td><strong>检查和</strong></td>
</tr>
<tr align="center">
<td colspan="2"><strong>数据</strong></td>
</tr>
</tbody>
</table>



<h5><a id="TCP_79"></a>二、TCP协议</h5> 
<h6><a id="A_80"></a>A、特点：</h6> 
<ul><li>面向连接的协议。数据传输之前都要建立连接（三次挥手），数据传输结束都要释放连接（四次挥手）</li><li>一条TCP连接只能有两个端点，端点是socket（结构 <strong>IP地址:端口号</strong>），并非主机或进程。</li><li>可靠交付</li><li>全双工通信（一端既可以做发送方也可以做接收方）</li><li>面向字节流</li></ul> 
<h6><a id="BTCP_87"></a>B、为何TCP是可靠的呢？</h6> 
<p>其实TCP是依赖停止 <strong>等待协议</strong>和<strong>连续ARQ 协议+滑动窗口协议</strong>才达到可靠的目的</p> 
<h6><a id="a_89"></a>a、等待协议</h6> 
<ul><li>特点：资源利用率非常低</li><li>工作原理<br> 客户发送一次数据到服务端，必须等到服务端响应后才发第二次数据，中间的等待时间RTT占了大部分时间，中间如果出现差错（超时或确认丢失）都需要从新传输。</li></ul> 
<h6><a id="bARQ_94"></a>b、连续ARQ协议</h6> 
<ul><li>连续ARQ协议工作原理<br> 维持一个发送窗口（记录了当前可以发送的数据包数量n），在窗口内的数据都可以连续发送出去，服务器只在接收完一个发送窗口的数据后才回响应（累计确认），发送端接收到响应就把发送窗口移动n位，开始新一轮数据发送。</li></ul> 
<p><strong>以上只是简单了解TCP协议的发送流程，如果要清楚发送细节，必须知道TCP报文首部</strong></p> 
<h5><a id="TCP_100"></a>TCP报文段的首部格式</h5> 
<p>虽然说TCP是面向字节流的，但是TCP传输的数据单元却是报文段，报文段由首部和数据两部分组成，如图</p> 


<table align="center" bordercolor="#cccccc" cellspacing="0" cellpadding="0" border="1">
<tbody align="center" id="tcp_head_style">
<tr align="center">
<td colspan="8"><strong>16位源端口号</strong></td>
<td><strong>16位目的端口号</strong></td>
</tr>
<tr align="center">
<td colspan="9"><strong>32位序号</strong></td>
</tr>
<tr align="center">
<td colspan="9"><strong>32位确认序号</strong></td>
</tr>
<tr align="center">
<td><strong>4位首部长度</strong></td>
<td><strong>保留(6位)</strong></td>
<td><strong>URG</strong></td>
<td><strong>ACK</strong></td>
<td><strong>PSH</strong></td>
<td><strong>RST</strong></td>
<td><strong>SYN</strong></td>
<td><strong>FIN</strong></td>
<td><strong>16位窗口大小</strong></td>
</tr>
<tr align="center">
<td colspan="8"><strong>16位检验和</strong></td>
<td><strong>16位紧急指针</strong></td>
</tr>
<tr align="center">
<td colspan="9"><strong>选项</strong></td>
</tr>
<tr align="center">
<td colspan="9"><strong>数据</strong></td>
</tr>
</tbody>
</table>

<p>一、源端口和目标端口（各占两字节）<br> 二、序号（占4字节）：TCP连接传输的数据每一个字节都有一个序号，而一个报文段可能会有多个字节的数据，这个序号指的是TCP报文段中起始的序号，下一个报文段的序号则是该序号加上报文数据长度（三次握手和四次挥手时说的SYN或ACK会消耗一个序号就是指该序号）<br> 三、确认号（占4字节）：因为一次数据传输会分成多个报文段，接收方接收完一次报文段后如果要发送确认（有可能不用确认，因为是接收完发送窗口的报文段才确认的），则会携带一个确认号，表示接收方想要接收的下一个报文的序号<br> 四、数据偏移（占4字位）：数据部分的起始位置离报文段起始位置的距离，就是报文首部的长度，单位是4字节，所以4位能表示最大值是十进制的15，就是15 x 4字节 = 60字节，TCP报文首部最大长度为60字节<br> 五、保留（占6位）：未被使用，全置为0<br> 六、紧急URG：当URG=1时紧急数据才有效。注意，这里URG并不是紧急数据，只是一个标志，标志着紧急数据是否有效<br> 七、确认ACK：当ACK=1时确认号才有效，当建立连接后全部传输的报文都要把ACK设置为1<br> 八、推送PSH：接收方机器会有一个接收，当接收缓存慢了才回把接收到的数据交付到接收应用进程中，而如果发送端把报文的PSH设为1，接收方接收到该报文会立即交付到应用的进程中<br> 九、复位RST：两个作用，1、当RST=1时，表示TCP连接中出现严重差错，必须释放连接，然后重新建立运输连接。2、当RST=1时，拒绝一个非法的报文段或拒绝打开一个连接。<br> 十、同步SYN：用于同步序号（告诉另外一方，他们之间从该序号开始传输报文段），当SYN=1,ACK=0表示这时一个连接请求报文。<br> 十一、终止FIN：用于释放一个连接。当FIN=1时，表明此报文的发送方的数据已经发送完毕，并要求释放运输连接。<br> 十二、窗口（占2字节），是一个接收窗口，接收方允许发送方发送的数据量<br> 十三、检验和（占2字节）：检验接收过来的报文段（报文首部和用户数据）是否有误<br> 十四、紧急指针（占2字节）：当URG=1时才有效，指出紧急数据未尾位置（开始位置是整个报文段中用户数据的开头）<br> 十五、选项，长度可变，最长40字节</p> 
<p><strong>那到底TCP是如何实现可靠传输的呢？</strong></p> 
<h4><a id="TCP_122"></a>TCP可靠传输的实现</h4> 
<h5><a id="_123"></a>一、通过滑动窗口来发送数据</h5> 
<p><img src="https://img-blog.csdnimg.cn/20190512145219559.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0xpYW5nSkdv,size_16,color_FFFFFF,t_70" alt="在这里插入图片描述"></p> 
<ul><li>发送窗口有两部分组成，已发送的报文段 和 能够发送但未发送的报文段（等待已发送报文段全部接收完发回来的确认就可以发送了）</li><li>当收到确认后发送窗口会向右移动到7位置，作为窗口的起始位置。</li><li>发送窗口，发送窗口有可能会收缩（因为接收窗口有可能因为接收缓存不够而变小）</li></ul> 
<h5><a id="_129"></a>二、超时重传时间的选择</h5> 
<p>采用一个根据RTT动态计算的时间，并不是直接采用一个固定的时间<br> RTT：发送一个报文段到收到对应的ACK所花费的时间<br> RTO：超时重传时间<br> RTTs是一个加权平均RTT时间<br> RTTd是RTTs偏差的加权平均<br> RTO = RTTs + 4 * RTTd<br> 如果发生了重传 ，这次的RTT会让RTTs会变大，此时是不会用该RTT来计算RTTs的</p> 
<h5><a id="SACK_138"></a>三、确认SACK</h5> 
<p>是一个TCP报文首部的选项。<br> 当数据传输过程中，接收方可能会未按顺收到部分报文段，此时序号告诉发送方从新传输这些报文段，SACK选项就是用于告诉发送方需要传输那些报文段的</p> 
<h4><a id="TCP_143"></a>TCP传输连接管理</h4> 
<p>连接的三个阶段：建立连接、数据传输、连接释放<br> 在建立连接的过程中要解决三个问题：<br> 1、使每一方都知道对方的存在<br> 2、协商一些参数<br> 3、能够运输实体资源</p> 
<p>主动建立连接的一端叫客户端，被动等待连接建立的一方叫服务器</p> 
<h5><a id="_152"></a>连接建立（三次握手）</h5> 
<p>如图：<br> <img src="https://img-blog.csdnimg.cn/20190512154818950.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0xpYW5nSkdv,size_16,color_FFFFFF,t_70" alt="在这里插入图片描述"><br> 每次发送一个seq时，都会消耗一个序号，所以会发现在确认时，ack总等于另一端请求的seq+1</p> 
<ul><li>为何需要第三次握手？<br> 假设没有第三次握手（即A再次确认）<br> 在很久很久以前，A发了一个连接请求给B，但是网络滞留的原因，请求没有到达B，所以B也没有确认返回给A，所以A右发送了一个连接请求给B，此时B收到了连接请求并返回了一个确认给A，此时连端开始愉快的数据传输之旅。当传输结束时，分别断开连接，各自干各自的活儿。但是过了一段时间，之间滞留在网络中的A发出的连接请求到达了B中，B以为A又要传输数据，便右回了一个确认给A，但是A并不需要输出传输，也没有理会这个确认，而B却在傻傻等待A传输数据，这个就会浪费B的资源。<br> 但是如果有第三次A的确认，A这个滞留的连接传给B，B返回一个确认，但是A不想传输数据了，便没有回一个确认给B（第三次握手），B没有收到该确认也不会等待A传输数据。</li></ul> 
<h5><a id="_162"></a>连接释放（四次挥手）</h5> 
<p>如图：<br> <img src="https://img-blog.csdnimg.cn/20190512161947663.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0xpYW5nSkdv,size_16,color_FFFFFF,t_70" alt="在这里插入图片描述"><br> 第一次挥手：客户端发送连接，FIN=1标志着A已经完成了数据的发送。<br> 第二次挥手：B回了一个确认，此时A与B的发送连接就断开了。<br> 第三次挥手：因为TCP连接是全双工通信的，B还保留着一个对A大发送连接，如果等到B也不需要发送数据给A时，B会发送一个连接给A，seq等于一个大于或等于v的值（因为A与B断开发送连接到B与A断开发送连接期间有可能B向A发送了数据，就是消耗序号）。<br> 第四次挥手：当A收到B的连接时，要回一个响应给B，但是此时会有一个2MSL长的等待时间，时间一过，就真正的断开与B的全部连接了。</p> 
<ul><li>为什么需要2MSL的等待时间？<br> MSL：最长报文寿命<br> 当A发送确认给A后，如果此时出现了一些状况（连接被丢弃等），确认无法到达B中，B会重新发送一个连接给A，但是A就停止了，B就一直等待（其实有一个保活时间）。<br> 如果有了这个等待时间，就算A的ACK确认丢失了，B也会再从新发送一个连接给A，A接收到该连接后，会从新计算等待时间。A会再确认一次</li></ul> 
<h3><a name="t4"></a><a name="t4"></a><a id="_178"></a>应用层</h3> 
<h4><a id="HTTP_179"></a>HTTP协议</h4> 
<h5><a id="_180"></a>特点：</h5> 
<ul><li>支持客户端 / 服务器模式</li><li>简单快速</li><li>灵活</li><li>无连接，在完成一次请求获得响应后就会断开</li><li>无状态，没有记忆的，请求完一次后，就结束了，后面如果要再获得数据必须从新请求</li></ul> 
<h5><a id="_187"></a>请求报文的结构</h5> 
<p><img src="https://img-blog.csdnimg.cn/20190512171540961.png" alt="在这里插入图片描述"></p> 
<p>请求头部：用于设置请求的的一些参数如：ContentType<br> 请求空行：就算请求数据为空，都要有空行，表示请求首部的结束</p> 
<p>从浏览器地址栏键入URL，回车后会尽力的流程：</p> 
<ul><li>DNS解析</li><li>TCP连接</li><li>发送HTTP请求</li><li>服务器处理请求，并返回HTTP报文</li><li>浏览器解析渲染页面</li><li>连接结束</li></ul> 
<p>GET请求与POST请求的区别</p> 
<ul><li>HTTP报文层面：GET请求信息放在URL中，POST放在报文体中</li><li>数据库层面：GET符合幂等性和安全性，POST不符合</li><li>其他层面：GET可以被缓存、储存，而POST不行</li></ul> 
<p>Cookie和Session的区别</p> 
<ul><li>为什么会有这两种技术？<br> 在使用一些需要登录的网站时，每次访问，都会需要验证个人信息，即登录。这样做比较繁琐，能否将个人的账号和密码存起来，访问的时候直接用存取来的个人信息进行验证呢？解决这个问题的就是Cookie和Session</li><li>Cookie：通过客户端（浏览器）来缓存个人信息。当用户第一次登录时，服务器会将个人信息放在了响应中， 浏览器接收到响应时候会将个人信息以Cookie的形式访问浏览器中保存起来，在下一次访问服务器的时候会带上该Cookie，Cookie中有个人信息，服务器能解析出来，所以不同再次登录验证了。（不够安全，对服务器的开销小）<img src="https://img-blog.csdnimg.cn/20190512200202886.PNG?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0xpYW5nSkdv,size_16,color_FFFFFF,t_70" alt="在这里插入图片描述"></li><li>Session通过服务端来缓存信息，根据请求中是否包含Session id的字段，如果不存在则创建一个，并返回给浏览器缓存起来。如果存在则通过该Session id在服务器存储中获得对应的Session信息，直接验证。（安全，服务器的开销变大）<br> 
<img src="https://img-blog.csdnimg.cn/20190512201338966.PNG?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0xpYW5nSkdv,size_16,color_FFFFFF,t_70" alt="在这里插入图片描述"></li></ul> 
<h4><a id="HTTPHTTPS_214"></a>HTTP与HTTPS的区别：</h4> 
<p>1、HTTPS需要到CA申请证书，HTTP不需要<br> 2、HTTPS密文传输、HTTP明文传输<br> 3、连接方式不同，HTTPS默认使用443端口，HTTP使用80端口<br> 4、HTTPS = HTTP + 加密+认证+完整性保护，较HTTP安全</p> 
<p>其实也不一定就安全，原因是用户不会再访问时候加上http:// 或 https://, 浏览器就默认会加上http://，然后通过转发的方式转成https:// 这个过程http就有可能会被劫持了。<br> 此时会用到一个技术 HSTS(HTTP Strict Transort Security)</p>
                </div>