---
layout: post
title: "A Naive-bayse-classify Document classify writed by ruby"
date: 2011-11-22 18:11
comments: true
categories: [ruby, source code, naive bayse classify]
---

<h2>== Description:</h2>

<h4>naive_bayes_classify.rb</h4>
    naive_bayes_classify is a document classify programme.
<pre>
    Usage:
        naive_bayes_classify [options] <Dirname>+
    where [options] are:
    --train, -t \<s\>:   Train a model from a Dir
    --test, -e \<s\>:   Test a dir from Mode
    --model, -m \<s\>:   Model name for test or the output of train
    --thres, -h \<f\>:   Threshold value for Naive Bayes Classify (default: 1.5)
    --version, -v:   Print version and exit
    --help, -l:   Show this message
</pre>

<h4>result_analyze.rb</h4>
    result_analyze is a naive_bayes_classify result analyze programme.
<pre>
    Usage:
        result_analyze [options] <filename>
    where [options] are:
    --file, -f \<s\>:   Output file of "naive_bayes_classify"
    --version, -v:   Print version and exit
    --help, -h:   Show this message
</pre>

<h2>== Example:</h2>

Sample Data: http://people.csail.mit.edu/jrennie/20Newsgroups/
<h4>train</h4>
<pre>
    naive_bayes_classify.rb -t 20news-bydate-train -m 20news-bydate-train.model -h 1.5
</pre>
<h4>test</h4>
<pre>
    naive_bayes_classify.rb -e 20news-bydate-test -m 20news-bydate-train.model > 20news-bydate-test.res
</pre>
<h4>result analysis</h4>
<pre>
    result_analyze -f 20news-bydate-test.res
</pre>
