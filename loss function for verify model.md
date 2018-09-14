---


---

<h1 id="loss-function-for-verification-model">loss function for verification model</h1>
<p>这篇MD是用于记录可以使用在verification model中loss function</p>
<h2 id="introduction">introduction</h2>
<ul>
<li>
<p>task of  verification</p>
<ul>
<li>对输入数据进行编码，使之为一个feature vector，同时这个vector需要保证一个性质。即相似的数据，属于同一个label的数据，其编码向量之间使用distance function计算出的distant尽可能小，而相异的数据差异值较大。</li>
<li>算法使用一个margin来保证相似的数据和相异的数据其距离值需要保持一个显著的差值。</li>
</ul>
<blockquote>
<p>pull similar images closer in embedding space and push dissimilar images apart.</p>
</blockquote>
<ul>
<li>这种学习被称为 embedding learn，原理类似词嵌入，将输入数据encoding成向量。并用距离函数将其不同类别的数据分割开。</li>
</ul>
</li>
<li>
<p>在这个任务中最重要的是如何在mapping中，如何定义distance，用其计算loss，而是在进行loss计算中如何采样（如何尽可能逼近数据中的分布）。</p>
</li>
</ul>
<blockquote>
<p>This provides us with two knobs to turn: the loss and the sampling strategy.</p>
</blockquote>
<ul>
<li>之前的一些loss function
<ul>
<li>contrastive loss
<ul>
<li>这个loss是完全通过欧氏距离进行映射，将输入数据映射到一个高维的欧氏空间中，优点是收敛速度快，健壮性强。缺点是不能良好的面对当categories之间的分布不符合欧氏空间 存在变形时，不能很好的保证区分margin</li>
</ul>
</li>
<li>
<h2 id="triplet-loss">triplet loss</h2>
</li>
</ul>
</li>
</ul>
<blockquote>
<p>Written with <a href="https://stackedit.io/">StackEdit</a>.</p>
</blockquote>

