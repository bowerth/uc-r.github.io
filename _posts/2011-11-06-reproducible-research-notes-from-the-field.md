---
id: 385
title: 'Reproducible research: Notes from the field'
date: 2011-11-06T16:13:05+00:00
author: admin
layout: post
guid: http://simplystatistics.wordpress.com/2011/11/06/reproducible-research-notes-from-the-field
permalink: /2011/11/06/reproducible-research-notes-from-the-field/
tumblr_simplystatistics_permalink:
  - http://simplystatistics.tumblr.com/post/12421558195/reproducible-research-notes-from-the-field
tumblr_simplystatistics_id:
  - 12421558195
dsq_thread_id:
  - 934683053
categories:
  - Uncategorized
tags:
  - reproducibility
---
Over the past year, I&#8217;ve been doing a lot of talking about reproducible research. Talking to people, talking on panel discussions, and talking about <a href="http://simplystatistics.tumblr.com/post/12243614318/i-gave-a-talk-on-reproducible-research-back-in" target="_blank">some of my own work</a>. It seems to me that interest in the topic has exploded recently, in part due to some recent scandals, such as the <a href="http://simplystatistics.tumblr.com/post/10068195751/the-duke-saga" target="_blank">Duke clinical trials fiasco</a>.

If you are unfamiliar with the term &#8220;reproducible research&#8221;, the basic idea is that authors of published research should make available the necessary materials so that others may reproduce to a very high degree of similarity the published findings. If that definitions seems imprecise, well that&#8217;s because it is.

<!-- more -->I think reproducibility becomes easier to define in the context of a specific field or application. Reproducibility often comes up in the context of computational science. In computational science fields, often much of the work is done on the computer using often very large amounts of data. In other words, the analysis of the data is of comparable difficulty as the collection of the data (maybe even more complicated). Then the notion of reproducibility typically comes down to the idea of making the analytic data and the computer code available to others. That way, knowledgeable people can run your code on your data and presumably get your results. If others do not get your results, then that may be a sign of a problem, or perhaps a misunderstanding. In either case, a resolution needs to be found. Reproducibility is key to science much the way it is key to programming. When bugs are found in software, being able to reproduce the bug is an important step to fixing it. Anyone learning to program in C knows the pain of dealing with a memory-related bug, which will often exhibit seemingly random and non-reproducible behavior.

My discussions with others about the need for reproducibility in science often range far and wide. One reason is that many people have very different ideas what (a) what is reproducibility and (b) why we need it. Here is my take on various issues.

  * **Reproducibility is not replication**. There&#8217;s often honest confusion between the notion of reproducibility and what I would call a &#8220;full replication&#8221;. A full replication doesn&#8217;t analyze the same dataset, but rather involves an independent investigator collecting an independent dataset conducting an independent analysis. Full replication has been a fundamental component of science for a long time now and will continue to be the primary yardstick for measuring the plausibility of scientific claims. I think most would agree that full replication is preferable, but often it is simply not possible.
  * **Reproducibility is not needed solely to prevent fraud**. I&#8217;ve heard many people emphasize reproducibility as a means to prevent fraud. Journal editors seem to think this is the main reason for demanding reproducibility. It is_ one_ reason, but to be honest, I&#8217;m not sure it&#8217;s all that useful for detecting fraud. If someone truly wants to commit fraud, then it&#8217;s possible to make the fraud reproducible. If I just generate a bunch of numbers and claim it as data that I collected, any analysis from that dataset can be reproducible. While demanding reproducibility may be useful for ferreting out certain types of fraud, it&#8217;s not a general solution and it&#8217;s not the primary reason we need it. 
  * **Reproducibility is not as easy as it sounds**. Making one&#8217;s research reproducible is hard. It&#8217;s especially hard when you try to do it _after_ the research has been done. In that case it&#8217;s more like an audit, and I&#8217;m guessing for most people the word &#8220;audit&#8221; is NOT synonymous with &#8220;fun&#8221;. Even if you set out to make your work reproducible from the get go, it&#8217;s easy to miss things. Code can get lost (even with a version control system) and metadata can slip through the cracks. Even when you&#8217;ve done everything right, computers and software can change. Virtual machines like Amazon EC2 and others seem to have some potential. The single most useful tool that I have found is a good version control system, like <a href="http://git-scm.com/" target="_blank">git</a>. 
  * **At this point, anything would be better than nothing**. Right now, I think the bar for reproducibility is quite low in the sense that most published work is not reproducible. Even if data are available, often the code that analyzed the data is not available. So if you&#8217;re publishing research and you want to make it at least partially reproducible, just put what you can out there. On the web, on <a href="http://github.com" target="_blank">github</a>, in a data repository, wherever you can. If you can&#8217;t publish the data, make your code available. Even that is better than nothing. In fact, I find reading someone&#8217;s code to be very informative and often questions can arise without looking at the data. Until we have a better infrastructure for distributing reproducible research, we will have to make do with what we have. But if we all start putting stuff out there, the conversation will turn from &#8220;Why should I make stuff available?&#8221; to &#8220;Why wouldn&#8217;t I make stuff available?&#8221;