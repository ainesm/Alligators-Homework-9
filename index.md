

<html>

<head>

<meta name="generator" content="pandoc" />
<meta http-equiv="X-UA-Compatible" content="IE=EDGE" />


<meta name="author" content="Ammar Plumber, Elaina Lin, Kim Nguyen, Meghan Aines, Ryan Karbowicz" />


<title>Homework 9 - Alligators</title>

<script src="site_libs/header-attrs-2.7/header-attrs.js"></script>
<script src="site_libs/jquery-1.11.3/jquery.min.js"></script>
<meta name="viewport" content="width=device-width, initial-scale=1" />
<link href="site_libs/bootstrap-3.3.5/css/yeti.min.css" rel="stylesheet" />
<script src="site_libs/bootstrap-3.3.5/js/bootstrap.min.js"></script>
<script src="site_libs/bootstrap-3.3.5/shim/html5shiv.min.js"></script>
<script src="site_libs/bootstrap-3.3.5/shim/respond.min.js"></script>
<style>h1 {font-size: 34px;}
       h1.title {font-size: 38px;}
       h2 {font-size: 30px;}
       h3 {font-size: 24px;}
       h4 {font-size: 18px;}
       h5 {font-size: 16px;}
       h6 {font-size: 12px;}
       code {color: inherit; background-color: rgba(0, 0, 0, 0.04);}
       pre:not([class]) { background-color: white }</style>
<script src="site_libs/navigation-1.1/tabsets.js"></script>
<script src="site_libs/kePrint-0.0.1/kePrint.js"></script>
<link href="site_libs/lightable-0.0.1/lightable.css" rel="stylesheet" />

<style type="text/css">
  code{white-space: pre-wrap;}
  span.smallcaps{font-variant: small-caps;}
  span.underline{text-decoration: underline;}
  div.column{display: inline-block; vertical-align: top; width: 50%;}
  div.hanging-indent{margin-left: 1.5em; text-indent: -1.5em;}
  ul.task-list{list-style: none;}
    </style>


<style type="text/css">
  code {
    white-space: pre;
  }
  .sourceCode {
    overflow: visible;
  }
</style>
<style type="text/css" data-origin="pandoc">
pre > code.sourceCode { white-space: pre; position: relative; }
pre > code.sourceCode > span { display: inline-block; line-height: 1.25; }
pre > code.sourceCode > span:empty { height: 1.2em; }
code.sourceCode > span { color: inherit; text-decoration: inherit; }
div.sourceCode { margin: 1em 0; }
pre.sourceCode { margin: 0; }
@media screen {
div.sourceCode { overflow: auto; }
}
@media print {
pre > code.sourceCode { white-space: pre-wrap; }
pre > code.sourceCode > span { text-indent: -5em; padding-left: 5em; }
}
pre.numberSource code
  { counter-reset: source-line 0; }
pre.numberSource code > span
  { position: relative; left: -4em; counter-increment: source-line; }
pre.numberSource code > span > a:first-child::before
  { content: counter(source-line);
    position: relative; left: -1em; text-align: right; vertical-align: baseline;
    border: none; display: inline-block;
    -webkit-touch-callout: none; -webkit-user-select: none;
    -khtml-user-select: none; -moz-user-select: none;
    -ms-user-select: none; user-select: none;
    padding: 0 4px; width: 4em;
    color: #aaaaaa;
  }
pre.numberSource { margin-left: 3em; border-left: 1px solid #aaaaaa;  padding-left: 4px; }
div.sourceCode
  {  background-color: #f8f8f8; }
@media screen {
pre > code.sourceCode > span > a:first-child::before { text-decoration: underline; }
}
code span.al { color: #ef2929; } /* Alert */
code span.an { color: #8f5902; font-weight: bold; font-style: italic; } /* Annotation */
code span.at { color: #c4a000; } /* Attribute */
code span.bn { color: #0000cf; } /* BaseN */
code span.cf { color: #204a87; font-weight: bold; } /* ControlFlow */
code span.ch { color: #4e9a06; } /* Char */
code span.cn { color: #000000; } /* Constant */
code span.co { color: #8f5902; font-style: italic; } /* Comment */
code span.cv { color: #8f5902; font-weight: bold; font-style: italic; } /* CommentVar */
code span.do { color: #8f5902; font-weight: bold; font-style: italic; } /* Documentation */
code span.dt { color: #204a87; } /* DataType */
code span.dv { color: #0000cf; } /* DecVal */
code span.er { color: #a40000; font-weight: bold; } /* Error */
code span.ex { } /* Extension */
code span.fl { color: #0000cf; } /* Float */
code span.fu { color: #000000; } /* Function */
code span.im { } /* Import */
code span.in { color: #8f5902; font-weight: bold; font-style: italic; } /* Information */
code span.kw { color: #204a87; font-weight: bold; } /* Keyword */
code span.op { color: #ce5c00; font-weight: bold; } /* Operator */
code span.ot { color: #8f5902; } /* Other */
code span.pp { color: #8f5902; font-style: italic; } /* Preprocessor */
code span.sc { color: #000000; } /* SpecialChar */
code span.ss { color: #4e9a06; } /* SpecialString */
code span.st { color: #4e9a06; } /* String */
code span.va { color: #000000; } /* Variable */
code span.vs { color: #4e9a06; } /* VerbatimString */
code span.wa { color: #8f5902; font-weight: bold; font-style: italic; } /* Warning */

</style>
<script>
// apply pandoc div.sourceCode style to pre.sourceCode instead
(function() {
  var sheets = document.styleSheets;
  for (var i = 0; i < sheets.length; i++) {
    if (sheets[i].ownerNode.dataset["origin"] !== "pandoc") continue;
    try { var rules = sheets[i].cssRules; } catch (e) { continue; }
    for (var j = 0; j < rules.length; j++) {
      var rule = rules[j];
      // check if there is a div.sourceCode rule
      if (rule.type !== rule.STYLE_RULE || rule.selectorText !== "div.sourceCode") continue;
      var style = rule.style.cssText;
      // check if color or background-color is set
      if (rule.style.color === '' && rule.style.backgroundColor === '') continue;
      // replace div.sourceCode by a pre.sourceCode rule
      sheets[i].deleteRule(j);
      sheets[i].insertRule('pre.sourceCode{' + style + '}', j);
    }
  }
})();
</script>







<style type = "text/css">
.main-container {
  max-width: 940px;
  margin-left: auto;
  margin-right: auto;
}
img {
  max-width:100%;
}
.tabbed-pane {
  padding-top: 12px;
}
.html-widget {
  margin-bottom: 20px;
}
button.code-folding-btn:focus {
  outline: none;
}
summary {
  display: list-item;
}
pre code {
  padding: 0;
}
</style>


<style type="text/css">
.dropdown-submenu {
  position: relative;
}
.dropdown-submenu>.dropdown-menu {
  top: 0;
  left: 100%;
  margin-top: -6px;
  margin-left: -1px;
  border-radius: 0 6px 6px 6px;
}
.dropdown-submenu:hover>.dropdown-menu {
  display: block;
}
.dropdown-submenu>a:after {
  display: block;
  content: " ";
  float: right;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
  border-width: 5px 0 5px 5px;
  border-left-color: #cccccc;
  margin-top: 5px;
  margin-right: -10px;
}
.dropdown-submenu:hover>a:after {
  border-left-color: #adb5bd;
}
.dropdown-submenu.pull-left {
  float: none;
}
.dropdown-submenu.pull-left>.dropdown-menu {
  left: -100%;
  margin-left: 10px;
  border-radius: 6px 0 6px 6px;
}
</style>

<script type="text/javascript">
// manage active state of menu based on current page
$(document).ready(function () {
  // active menu anchor
  href = window.location.pathname
  href = href.substr(href.lastIndexOf('/') + 1)
  if (href === "")
    href = "index.html";
  var menuAnchor = $('a[href="' + href + '"]');

  // mark it active
  menuAnchor.tab('show');

  // if it's got a parent navbar menu mark it active as well
  menuAnchor.closest('li.dropdown').addClass('active');

  // Navbar adjustments
  var navHeight = $(".navbar").first().height() + 15;
  var style = document.createElement('style');
  var pt = "padding-top: " + navHeight + "px; ";
  var mt = "margin-top: -" + navHeight + "px; ";
  var css = "";
  // offset scroll position for anchor links (for fixed navbar)
  for (var i = 1; i <= 6; i++) {
    css += ".section h" + i + "{ " + pt + mt + "}\n";
  }
  style.innerHTML = "body {" + pt + "padding-bottom: 40px; }\n" + css;
  document.head.appendChild(style);
});
</script>

<!-- tabsets -->

<style type="text/css">
.tabset-dropdown > .nav-tabs {
  display: inline-table;
  max-height: 500px;
  min-height: 44px;
  overflow-y: auto;
  border: 1px solid #ddd;
  border-radius: 4px;
}

.tabset-dropdown > .nav-tabs > li.active:before {
  content: "???";
  font-family: 'Glyphicons Halflings';
  display: inline-block;
  padding: 10px;
  border-right: 1px solid #ddd;
}

.tabset-dropdown > .nav-tabs.nav-tabs-open > li.active:before {
  content: "&#xe258;";
  border: none;
}

.tabset-dropdown > .nav-tabs.nav-tabs-open:before {
  content: "???";
  font-family: 'Glyphicons Halflings';
  display: inline-block;
  padding: 10px;
  border-right: 1px solid #ddd;
}

.tabset-dropdown > .nav-tabs > li.active {
  display: block;
}

.tabset-dropdown > .nav-tabs > li > a,
.tabset-dropdown > .nav-tabs > li > a:focus,
.tabset-dropdown > .nav-tabs > li > a:hover {
  border: none;
  display: inline-block;
  border-radius: 4px;
  background-color: transparent;
}

.tabset-dropdown > .nav-tabs.nav-tabs-open > li {
  display: block;
  float: none;
}

.tabset-dropdown > .nav-tabs > li {
  display: none;
}
</style>

<!-- code folding -->




</head>

<body>


<div class="container-fluid main-container">




<div class="navbar navbar-default  navbar-fixed-top" role="navigation">
  <div class="container">
    <div class="navbar-header">
      <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#navbar">
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
      </button>
      <a class="navbar-brand" href="index.html">Meghan Aines</a>
    </div>
    <div id="navbar" class="navbar-collapse collapse">
      <ul class="nav navbar-nav">
        <li>
  <a href="about.html">About</a>
</li>
<li>

<div id="header">



<h1 class="title toc-ignore">Homework 9 - Alligators</h1>
<h4 class="author">Ammar Plumber, Elaina Lin, Kim Nguyen, Meghan Aines, Ryan Karbowicz</h4>
<h4 class="date">4/13/2021</h4>

</div>


<div id="i.-introduction" class="section level1">
<h1>I. Introduction</h1>
<p>We will be examining the difference in tweet communications between TikTok and Facebook. These are two popular social media platforms but with very different target audiences. Thus, the two brands may differ in their communication styles and language. We set out to identify the particular ways in which they differ and to build a model that can attribute each tweet to the correct user.</p>
</div>
<div id="ii.-methodology" class="section level1">
<h1>II. Methodology</h1>
<p>First, after getting tweets using the Twitter API and R package rtweet, we use basic tools of data exploration to transform, visualize, and examine different features of the datasets, such as source, time, length, and particular contents (e.g., picture/links) of the tweets. We produce bar charts to visualize the most popular words used by each twitter account, as well as the most popular sentiments associated with tweets that each account produces. A word cloud also helps paint a clearer picture of each company???s most commonly used words.</p>
<p>Second, we transform the datasets into tidytext format for sentiment analysis. The two lexicons that we use are NRC and AFINN.</p>
<p>Finally, we train four different models to predict if a tweet was posted by either Facebook or TikTok. The inputs of these models are as follows:</p>
<ul>
<li><p>length of the tweet</p></li>
<li><p>the number of times each of the twenty most common words from each account appear</p></li>
<li><p>presence of pictures</p></li>
<li><p>sentiment words, which reflect anger, anticipation, disgust, negative, postive, trust, joy, surprise, fear and sadness</p></li>
<li><p>positive/negative valence, estimated by averaging AFINN scores over each tweet.</p></li>
</ul>
<p>The first model is a Simple Decision Tree, the second model is a Bagging Model, the third model is a Random Forest and the fourth model is a Gradient Boosting Model.</p>
<p>We report the residual sum of squares on the training and test sets to determine which models have the smallest differences between the predicted tweeter and actual tweeter. We also show confusion matrices to determine the predictive efficacy of the four models.</p>
</div>
<div id="iii.-setup-and-preliminary-analysis" class="section level1">
<h1>III. Setup and Preliminary Analysis</h1>
<p>First, we import all non-base packages to be used in this analysis.</p>
<div class="sourceCode" id="cb1"><pre class="sourceCode r"><code class="sourceCode r"><span id="cb1-1"><a href="#cb1-1" aria-hidden="true" tabindex="-1"></a><span class="fu">library</span>(rtweet)</span>
<span id="cb1-2"><a href="#cb1-2" aria-hidden="true" tabindex="-1"></a><span class="fu">library</span>(tidyverse)</span>
<span id="cb1-3"><a href="#cb1-3" aria-hidden="true" tabindex="-1"></a><span class="fu">library</span>(lubridate)</span>
<span id="cb1-4"><a href="#cb1-4" aria-hidden="true" tabindex="-1"></a><span class="fu">library</span>(scales)</span>
<span id="cb1-5"><a href="#cb1-5" aria-hidden="true" tabindex="-1"></a><span class="fu">library</span>(tidytext)</span>
<span id="cb1-6"><a href="#cb1-6" aria-hidden="true" tabindex="-1"></a><span class="fu">library</span>(wordcloud)</span>
<span id="cb1-7"><a href="#cb1-7" aria-hidden="true" tabindex="-1"></a><span class="fu">library</span>(textdata)</span>
<span id="cb1-8"><a href="#cb1-8" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb1-9"><a href="#cb1-9" aria-hidden="true" tabindex="-1"></a><span class="fu">library</span>(caret)       <span class="co"># for general model fitting</span></span>
<span id="cb1-10"><a href="#cb1-10" aria-hidden="true" tabindex="-1"></a><span class="fu">library</span>(rpart)       <span class="co"># for fitting decision trees</span></span>
<span id="cb1-11"><a href="#cb1-11" aria-hidden="true" tabindex="-1"></a><span class="fu">library</span>(rpart.plot)</span>
<span id="cb1-12"><a href="#cb1-12" aria-hidden="true" tabindex="-1"></a><span class="fu">library</span>(ipred)       <span class="co"># for fitting bagged decision trees</span></span>
<span id="cb1-13"><a href="#cb1-13" aria-hidden="true" tabindex="-1"></a><span class="fu">library</span>(ranger)</span>
<span id="cb1-14"><a href="#cb1-14" aria-hidden="true" tabindex="-1"></a><span class="fu">library</span>(gbm)</span>
<span id="cb1-15"><a href="#cb1-15" aria-hidden="true" tabindex="-1"></a><span class="fu">library</span>(vip)</span>
<span id="cb1-16"><a href="#cb1-16" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb1-17"><a href="#cb1-17" aria-hidden="true" tabindex="-1"></a><span class="fu">library</span>(kableExtra)</span></code></pre></div>
<p>Now, we import the tweets that we pulled using the get_timeline() function and saved to a CSV file. There are ~3200 tweets from each user in our dataset.</p>
<div class="sourceCode" id="cb2"><pre class="sourceCode r"><code class="sourceCode r"><span id="cb2-1"><a href="#cb2-1" aria-hidden="true" tabindex="-1"></a><span class="co"># Run these two lines to get the tweets </span></span>
<span id="cb2-2"><a href="#cb2-2" aria-hidden="true" tabindex="-1"></a><span class="co"># and then save them as a csv for future use</span></span>
<span id="cb2-3"><a href="#cb2-3" aria-hidden="true" tabindex="-1"></a><span class="co"># tiktok &lt;- get_timeline(&quot;tiktok_us&quot;, n=3200)</span></span>
<span id="cb2-4"><a href="#cb2-4" aria-hidden="true" tabindex="-1"></a><span class="co"># tiktok %&gt;% write_as_csv(&#39;tiktok.csv&#39;)</span></span>
<span id="cb2-5"><a href="#cb2-5" aria-hidden="true" tabindex="-1"></a><span class="co"># </span></span>
<span id="cb2-6"><a href="#cb2-6" aria-hidden="true" tabindex="-1"></a><span class="co"># facebook &lt;- get_timeline(&quot;Facebook&quot;, n=3200)</span></span>
<span id="cb2-7"><a href="#cb2-7" aria-hidden="true" tabindex="-1"></a><span class="co"># facebook %&gt;% write_as_csv(&quot;facebook.csv&quot;)</span></span>
<span id="cb2-8"><a href="#cb2-8" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb2-9"><a href="#cb2-9" aria-hidden="true" tabindex="-1"></a>tiktok <span class="ot">&lt;-</span></span>
<span id="cb2-10"><a href="#cb2-10" aria-hidden="true" tabindex="-1"></a>  <span class="fu">read_csv</span>(<span class="st">&#39;tiktok.csv&#39;</span>) <span class="sc">%&gt;%</span> </span>
<span id="cb2-11"><a href="#cb2-11" aria-hidden="true" tabindex="-1"></a>  <span class="fu">select</span>(status_id, source, text, created_at) <span class="sc">%&gt;%</span> </span>
<span id="cb2-12"><a href="#cb2-12" aria-hidden="true" tabindex="-1"></a>  <span class="fu">as.data.frame</span>()</span>
<span id="cb2-13"><a href="#cb2-13" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb2-14"><a href="#cb2-14" aria-hidden="true" tabindex="-1"></a>facebook <span class="ot">&lt;-</span></span>
<span id="cb2-15"><a href="#cb2-15" aria-hidden="true" tabindex="-1"></a>  <span class="fu">read_csv</span>(<span class="st">&#39;facebook.csv&#39;</span>) <span class="sc">%&gt;%</span> </span>
<span id="cb2-16"><a href="#cb2-16" aria-hidden="true" tabindex="-1"></a>  <span class="fu">select</span>(status_id, source, text, created_at)</span>
<span id="cb2-17"><a href="#cb2-17" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb2-18"><a href="#cb2-18" aria-hidden="true" tabindex="-1"></a>nrc <span class="ot">&lt;-</span> <span class="fu">read_rds</span>(<span class="st">&quot;nrc.rds&quot;</span>)</span>
<span id="cb2-19"><a href="#cb2-19" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb2-20"><a href="#cb2-20" aria-hidden="true" tabindex="-1"></a>facebook <span class="sc">%&gt;%</span> <span class="fu">head</span>()</span></code></pre></div>
<pre><code>## # A tibble: 6 x 4
##   status_id        source      text                                                                     created_at         
##   &lt;chr&gt;            &lt;chr&gt;       &lt;chr&gt;                                                                    &lt;dttm&gt;             
## 1 x13820200803434~ Twitter We~ &quot;Ramadan Mubarak &lt;U+0001F319&gt;\n \nThis #MonthofGood, check out all the ~ 2021-04-13 17:17:18
## 2 x13817344290186~ Khoros CX   &quot;@MeenalK1 Hi Meenal. Do you have the reference numbers for your submit~ 2021-04-12 22:22:13
## 3 x13817333826320~ Khoros CX   &quot;@Afrojalipro Thanks for updating us, Afroj! We&#39;re so happy to hear tha~ 2021-04-12 22:18:04
## 4 x13817326683881~ Khoros CX   &quot;@CallandManning Hi Calland. If you do not have access to the phone num~ 2021-04-12 22:15:14
## 5 x13817113768763~ Khoros CX   &quot;@BHARTINANDAN4 Hello! Please visit this Help Center article if you are~ 2021-04-12 20:50:37
## 6 x13817105484761~ Khoros CX   &quot;@weathermatt22 Hi Matt. Please visit our Help Center to report an issu~ 2021-04-12 20:47:20</code></pre>
<p>Now, for each user, we produce a line chart showing the percent of all tweets from each source by hour.</p>
<div class="sourceCode" id="cb4"><pre class="sourceCode r"><code class="sourceCode r"><span id="cb4-1"><a href="#cb4-1" aria-hidden="true" tabindex="-1"></a>facebook <span class="sc">%&gt;%</span></span>
<span id="cb4-2"><a href="#cb4-2" aria-hidden="true" tabindex="-1"></a>  <span class="fu">count</span>(source, <span class="at">hour =</span> <span class="fu">hour</span>(<span class="fu">with_tz</span>(created_at, <span class="st">&quot;EST&quot;</span>))) <span class="sc">%&gt;%</span></span>
<span id="cb4-3"><a href="#cb4-3" aria-hidden="true" tabindex="-1"></a>  <span class="fu">mutate</span>(<span class="at">percent =</span> n<span class="sc">/</span><span class="fu">sum</span>(n)) <span class="sc">%&gt;%</span></span>
<span id="cb4-4"><a href="#cb4-4" aria-hidden="true" tabindex="-1"></a>  <span class="fu">ggplot</span>(<span class="fu">aes</span>(<span class="at">x =</span> hour, <span class="at">y =</span> percent, <span class="at">color =</span> source)) <span class="sc">+</span></span>
<span id="cb4-5"><a href="#cb4-5" aria-hidden="true" tabindex="-1"></a>  <span class="fu">labs</span>(<span class="at">x =</span> <span class="st">&quot;Hour of day (EST)&quot;</span>, <span class="at">y =</span> <span class="st">&quot;% of tweets&quot;</span>, <span class="at">color =</span> <span class="st">&quot;&quot;</span>) <span class="sc">+</span> </span>
<span id="cb4-6"><a href="#cb4-6" aria-hidden="true" tabindex="-1"></a>  <span class="fu">scale_y_continuous</span>(<span class="at">labels =</span> <span class="fu">percent_format</span>()) <span class="sc">+</span></span>
<span id="cb4-7"><a href="#cb4-7" aria-hidden="true" tabindex="-1"></a>  <span class="fu">geom_line</span>() <span class="sc">+</span></span>
<span id="cb4-8"><a href="#cb4-8" aria-hidden="true" tabindex="-1"></a>  <span class="fu">ggtitle</span>(<span class="st">&#39;Facebook Source Breakdown by Hour&#39;</span>)</span></code></pre></div>
<p><img src="figure-html/unnamed-chunk-4-1.png" width="672" /></p>
<div class="sourceCode" id="cb5"><pre class="sourceCode r"><code class="sourceCode r"><span id="cb5-1"><a href="#cb5-1" aria-hidden="true" tabindex="-1"></a>tiktok <span class="sc">%&gt;%</span></span>
<span id="cb5-2"><a href="#cb5-2" aria-hidden="true" tabindex="-1"></a>  <span class="fu">count</span>(source, <span class="at">hour =</span> <span class="fu">hour</span>(<span class="fu">with_tz</span>(created_at, <span class="st">&quot;EST&quot;</span>))) <span class="sc">%&gt;%</span></span>
<span id="cb5-3"><a href="#cb5-3" aria-hidden="true" tabindex="-1"></a>  <span class="fu">mutate</span>(<span class="at">percent =</span> n<span class="sc">/</span><span class="fu">sum</span>(n)) <span class="sc">%&gt;%</span></span>
<span id="cb5-4"><a href="#cb5-4" aria-hidden="true" tabindex="-1"></a>  <span class="fu">ggplot</span>(<span class="fu">aes</span>(<span class="at">x =</span> hour, <span class="at">y =</span> percent, <span class="at">color =</span> source)) <span class="sc">+</span></span>
<span id="cb5-5"><a href="#cb5-5" aria-hidden="true" tabindex="-1"></a>  <span class="fu">labs</span>(<span class="at">x =</span> <span class="st">&quot;Hour of day (EST)&quot;</span>, <span class="at">y =</span> <span class="st">&quot;% of tweets&quot;</span>, <span class="at">color =</span> <span class="st">&quot;&quot;</span>) <span class="sc">+</span> </span>
<span id="cb5-6"><a href="#cb5-6" aria-hidden="true" tabindex="-1"></a>  <span class="fu">scale_y_continuous</span>(<span class="at">labels =</span> <span class="fu">percent_format</span>()) <span class="sc">+</span></span>
<span id="cb5-7"><a href="#cb5-7" aria-hidden="true" tabindex="-1"></a>  <span class="fu">geom_line</span>() <span class="sc">+</span></span>
<span id="cb5-8"><a href="#cb5-8" aria-hidden="true" tabindex="-1"></a>  <span class="fu">ggtitle</span>(<span class="st">&#39;Tiktok Source Breakdown by Hour&#39;</span>)</span></code></pre></div>
<p><img src="figure-html/unnamed-</ul>
</div><!--/.nav-collapse -->-4-2.png" width="672" /></p>
<p>We see that the vast majority of Facebook???s tweets are put out using Khoros Publishing between the hours of 10 AM and 8 PM. TikTok publishes most of its tweets through the Twitter Web App and Fan Experiences Platform???usually between 10 AM and 8 PM, like Facebook.</p>
<p>We want to see if both users??? tweets tend to differ in length, so we create a histogram for each user.</p>
<div class="sourceCode" id="cb6"><pre class="sourceCode r"><code class="sourceCode r"><span id="cb6-1"><a href="#cb6-1" aria-hidden="true" tabindex="-1"></a>fb_wordcounts <span class="ot">&lt;-</span> </span>
<span id="cb6-2"><a href="#cb6-2" aria-hidden="true" tabindex="-1"></a>  facebook <span class="sc">%&gt;%</span></span>
<span id="cb6-3"><a href="#cb6-3" aria-hidden="true" tabindex="-1"></a>  <span class="fu">mutate</span>(<span class="at">tweetLength =</span> <span class="fu">str_length</span>(text)) <span class="sc">%&gt;%</span> </span>
<span id="cb6-4"><a href="#cb6-4" aria-hidden="true" tabindex="-1"></a>  <span class="fu">filter</span>(tweetLength <span class="sc">&lt;</span> <span class="dv">500</span>)</span>
<span id="cb6-5"><a href="#cb6-5" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb6-6"><a href="#cb6-6" aria-hidden="true" tabindex="-1"></a>tiktok_wordcounts <span class="ot">&lt;-</span> </span>
<span id="cb6-7"><a href="#cb6-7" aria-hidden="true" tabindex="-1"></a>  tiktok <span class="sc">%&gt;%</span></span>
<span id="cb6-8"><a href="#cb6-8" aria-hidden="true" tabindex="-1"></a>  <span class="fu">mutate</span>(<span class="at">tweetLength =</span> <span class="fu">str_length</span>(text)) <span class="sc">%&gt;%</span> </span>
<span id="cb6-9"><a href="#cb6-9" aria-hidden="true" tabindex="-1"></a>  <span class="fu">filter</span>(tweetLength <span class="sc">&lt;</span> <span class="dv">500</span>)</span>
<span id="cb6-10"><a href="#cb6-10" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb6-11"><a href="#cb6-11" aria-hidden="true" tabindex="-1"></a><span class="fu">writeLines</span>(<span class="fu">c</span>(<span class="fu">paste0</span>(<span class="st">&quot;Facebook Mean Tweet Length: &quot;</span>, </span>
<span id="cb6-12"><a href="#cb6-12" aria-hidden="true" tabindex="-1"></a>                  <span class="fu">mean</span>(fb_wordcounts<span class="sc">$</span>tweetLength)), </span>
<span id="cb6-13"><a href="#cb6-13" aria-hidden="true" tabindex="-1"></a>           <span class="fu">paste0</span>(<span class="st">&quot;TikTok Mean Tweet Length: &quot;</span>, </span>
<span id="cb6-14"><a href="#cb6-14" aria-hidden="true" tabindex="-1"></a>                  <span class="fu">mean</span>(tiktok_wordcounts<span class="sc">$</span>tweetLength))))</span></code></pre></div>
<pre><code>## Facebook Mean Tweet Length: 163.289555972483
## TikTok Mean Tweet Length: 112.557921102066</code></pre>
<div class="sourceCode" id="cb8"><pre class="sourceCode r"><code class="sourceCode r"><span id="cb8-1"><a href="#cb8-1" aria-hidden="true" tabindex="-1"></a><span class="fu">hist</span>(tiktok_wordcounts<span class="sc">$</span>tweetLength, <span class="at">main =</span> <span class="st">&quot;TikTok - Histogram of Tweet Lengths&quot;</span>)</span></code></pre></div>
<p><img src="figure-html/unnamed-chunk-5-1.png" width="672" /></p>
<div class="sourceCode" id="cb9"><pre class="sourceCode r"><code class="sourceCode r"><span id="cb9-1"><a href="#cb9-1" aria-hidden="true" tabindex="-1"></a><span class="fu">hist</span>(fb_wordcounts<span class="sc">$</span>tweetLength, <span class="at">main =</span> <span class="st">&quot;Facebook - Histogram of Tweet Lengths&quot;</span>)</span></code></pre></div>
<p><img src="figure-html/unnamed-chunk-5-2.png" width="672" /></p>
<p>As we see, TikTok???s tweet lengths are right-skewed, with most tweets being around 100 words long. Facebook, on the other hand, seems to post longer tweets, with a more normal distribution centered around 150 words long. Tweet length seems like a useful feature to include in our predictive model.</p>
<p>Next, we look at whether there is a difference in the share of Tweets that include pictures.</p>
<div class="sourceCode" id="cb10"><pre class="sourceCode r"><code class="sourceCode r"><span id="cb10-1"><a href="#cb10-1" aria-hidden="true" tabindex="-1"></a>fb_picture_counts <span class="ot">&lt;-</span> </span>
<span id="cb10-2"><a href="#cb10-2" aria-hidden="true" tabindex="-1"></a>  facebook <span class="sc">%&gt;%</span></span>
<span id="cb10-3"><a href="#cb10-3" aria-hidden="true" tabindex="-1"></a>  <span class="fu">filter</span>(<span class="sc">!</span><span class="fu">str_detect</span>(text, <span class="st">&#39;^&quot;&#39;</span>)) <span class="sc">%&gt;%</span></span>
<span id="cb10-4"><a href="#cb10-4" aria-hidden="true" tabindex="-1"></a>  <span class="fu">count</span>(<span class="at">picture =</span> <span class="fu">ifelse</span>(<span class="fu">str_detect</span>(text, <span class="st">&quot;t.co&quot;</span>),</span>
<span id="cb10-5"><a href="#cb10-5" aria-hidden="true" tabindex="-1"></a>                         <span class="st">&quot;Picture/link&quot;</span>, <span class="st">&quot;No picture/link&quot;</span>))</span>
<span id="cb10-6"><a href="#cb10-6" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb10-7"><a href="#cb10-7" aria-hidden="true" tabindex="-1"></a>fb_picture_counts <span class="ot">&lt;-</span> </span>
<span id="cb10-8"><a href="#cb10-8" aria-hidden="true" tabindex="-1"></a>  fb_picture_counts <span class="sc">%&gt;%</span> </span>
<span id="cb10-9"><a href="#cb10-9" aria-hidden="true" tabindex="-1"></a>  <span class="fu">mutate</span>(<span class="at">prop =</span> n <span class="sc">/</span> <span class="fu">sum</span>(fb_picture_counts<span class="sc">$</span>n) <span class="sc">*</span><span class="dv">100</span>)</span>
<span id="cb10-10"><a href="#cb10-10" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb10-11"><a href="#cb10-11" aria-hidden="true" tabindex="-1"></a>tiktok_picture_counts <span class="ot">&lt;-</span> </span>
<span id="cb10-12"><a href="#cb10-12" aria-hidden="true" tabindex="-1"></a>  tiktok <span class="sc">%&gt;%</span></span>
<span id="cb10-13"><a href="#cb10-13" aria-hidden="true" tabindex="-1"></a>  <span class="fu">filter</span>(<span class="sc">!</span><span class="fu">str_detect</span>(text, <span class="st">&#39;^&quot;&#39;</span>)) <span class="sc">%&gt;%</span></span>
<span id="cb10-14"><a href="#cb10-14" aria-hidden="true" tabindex="-1"></a>  <span class="fu">count</span>(<span class="at">picture =</span> <span class="fu">ifelse</span>(<span class="fu">str_detect</span>(text, <span class="st">&quot;t.co&quot;</span>),</span>
<span id="cb10-15"><a href="#cb10-15" aria-hidden="true" tabindex="-1"></a>                         <span class="st">&quot;Picture/link&quot;</span>, <span class="st">&quot;No picture/link&quot;</span>))</span>
<span id="cb10-16"><a href="#cb10-16" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb10-17"><a href="#cb10-17" aria-hidden="true" tabindex="-1"></a>tiktok_picture_counts <span class="ot">&lt;-</span> </span>
<span id="cb10-18"><a href="#cb10-18" aria-hidden="true" tabindex="-1"></a>  tiktok_picture_counts <span class="sc">%&gt;%</span> </span>
<span id="cb10-19"><a href="#cb10-19" aria-hidden="true" tabindex="-1"></a>  <span class="fu">mutate</span>(<span class="at">prop =</span> n <span class="sc">/</span> <span class="fu">sum</span>(tiktok_picture_counts<span class="sc">$</span>n) <span class="sc">*</span><span class="dv">100</span>)</span>
<span id="cb10-20"><a href="#cb10-20" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb10-21"><a href="#cb10-21" aria-hidden="true" tabindex="-1"></a>fb_picture_counts <span class="sc">%&gt;%</span> </span>
<span id="cb10-22"><a href="#cb10-22" aria-hidden="true" tabindex="-1"></a>  <span class="fu">ggplot</span>(<span class="fu">aes</span>(<span class="at">x =</span> <span class="st">&quot;&quot;</span>, <span class="at">y =</span> n, <span class="at">fill =</span> picture)) <span class="sc">+</span></span>
<span id="cb10-23"><a href="#cb10-23" aria-hidden="true" tabindex="-1"></a>  <span class="fu">geom_bar</span>(<span class="at">width =</span> <span class="dv">1</span>, <span class="at">stat =</span> <span class="st">&quot;identity&quot;</span>) <span class="sc">+</span></span>
<span id="cb10-24"><a href="#cb10-24" aria-hidden="true" tabindex="-1"></a>  <span class="fu">coord_polar</span>(<span class="st">&quot;y&quot;</span>, <span class="at">start=</span><span class="dv">0</span>) <span class="sc">+</span></span>
<span id="cb10-25"><a href="#cb10-25" aria-hidden="true" tabindex="-1"></a>  <span class="fu">theme_void</span>() <span class="sc">+</span></span>
<span id="cb10-26"><a href="#cb10-26" aria-hidden="true" tabindex="-1"></a>  <span class="fu">geom_text</span>(<span class="fu">aes</span>(<span class="at">label =</span> <span class="fu">paste0</span>(<span class="fu">round</span>(prop,<span class="dv">2</span>), <span class="st">&quot;%&quot;</span>)), </span>
<span id="cb10-27"><a href="#cb10-27" aria-hidden="true" tabindex="-1"></a>            <span class="at">position =</span> <span class="fu">position_stack</span>(<span class="at">vjust =</span> <span class="fl">0.5</span>), <span class="at">size =</span> <span class="dv">4</span>) <span class="sc">+</span> </span>
<span id="cb10-28"><a href="#cb10-28" aria-hidden="true" tabindex="-1"></a>  <span class="fu">ggtitle</span>(<span class="st">&quot;Percent of Facebook Tweets with Picture/link and Without&quot;</span>)</span></code></pre></div>
<p><img src="figure-html/unnamed-chunk-6-1.png" width="672" /></p>
<div class="sourceCode" id="cb11"><pre class="sourceCode r"><code class="sourceCode r"><span id="cb11-1"><a href="#cb11-1" aria-hidden="true" tabindex="-1"></a>tiktok_picture_counts <span class="sc">%&gt;%</span> </span>
<span id="cb11-2"><a href="#cb11-2" aria-hidden="true" tabindex="-1"></a>  <span class="fu">ggplot</span>(<span class="fu">aes</span>(<span class="at">x =</span> <span class="st">&quot;&quot;</span>, <span class="at">y =</span> n, <span class="at">fill =</span> picture)) <span class="sc">+</span></span>
<span id="cb11-3"><a href="#cb11-3" aria-hidden="true" tabindex="-1"></a>  <span class="fu">geom_bar</span>(<span class="at">width =</span> <span class="dv">1</span>, <span class="at">stat =</span> <span class="st">&quot;identity&quot;</span>) <span class="sc">+</span></span>
<span id="cb11-4"><a href="#cb11-4" aria-hidden="true" tabindex="-1"></a>  <span class="fu">coord_polar</span>(<span class="st">&quot;y&quot;</span>, <span class="at">start=</span><span class="dv">0</span>) <span class="sc">+</span></span>
<span id="cb11-5"><a href="#cb11-5" aria-hidden="true" tabindex="-1"></a>  <span class="fu">theme_void</span>() <span class="sc">+</span></span>
<span id="cb11-6"><a href="#cb11-6" aria-hidden="true" tabindex="-1"></a>  <span class="fu">geom_text</span>(<span class="fu">aes</span>(<span class="at">label =</span> <span class="fu">paste0</span>(<span class="fu">round</span>(prop,<span class="dv">2</span>), <span class="st">&quot;%&quot;</span>)), </span>
<span id="cb11-7"><a href="#cb11-7" aria-hidden="true" tabindex="-1"></a>            <span class="at">position =</span> <span class="fu">position_stack</span>(<span class="at">vjust =</span> <span class="fl">0.5</span>), <span class="at">size =</span> <span class="dv">4</span>) <span class="sc">+</span> </span>
<span id="cb11-8"><a href="#cb11-8" aria-hidden="true" tabindex="-1"></a>  <span class="fu">ggtitle</span>(<span class="st">&quot;Percent of TikTok Tweets with Picture/link and Without&quot;</span>)</span></code></pre></div>
<p><img src="figure-html/unnamed-chunk-6-2.png" width="672" /></p>
<p>~86% of Facebook???s tweets contain pictures/links, while only ~52% of TikTok???s tweets contain pictures/links. This could be another useful predictor to include in our model.</p>
</div>
<div id="iv.-sentiment-analysis" class="section level1">
<h1>IV. Sentiment Analysis</h1>
<p>Now, we split the tweets into tokens so that we can perform sentiment analysis on them.</p>
<div class="sourceCode" id="cb12"><pre class="sourceCode r"><code class="sourceCode r"><span id="cb12-1"><a href="#cb12-1" aria-hidden="true" tabindex="-1"></a>reg <span class="ot">&lt;-</span> <span class="st">&quot;([^A-Za-z</span><span class="sc">\\</span><span class="st">d#@&#39;]|&#39;(?![A-Za-z</span><span class="sc">\\</span><span class="st">d#@]))&quot;</span></span>
<span id="cb12-2"><a href="#cb12-2" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb12-3"><a href="#cb12-3" aria-hidden="true" tabindex="-1"></a><span class="co"># Unnest the text strings into a data frame of words</span></span>
<span id="cb12-4"><a href="#cb12-4" aria-hidden="true" tabindex="-1"></a>fb_words <span class="ot">&lt;-</span> </span>
<span id="cb12-5"><a href="#cb12-5" aria-hidden="true" tabindex="-1"></a>  facebook <span class="sc">%&gt;%</span></span>
<span id="cb12-6"><a href="#cb12-6" aria-hidden="true" tabindex="-1"></a>  <span class="fu">filter</span>(<span class="sc">!</span><span class="fu">str_detect</span>(text, <span class="st">&#39;^&quot;&#39;</span>)) <span class="sc">%&gt;%</span></span>
<span id="cb12-7"><a href="#cb12-7" aria-hidden="true" tabindex="-1"></a>  <span class="fu">mutate</span>(<span class="at">text =</span> <span class="fu">str_replace_all</span>(text, </span>
<span id="cb12-8"><a href="#cb12-8" aria-hidden="true" tabindex="-1"></a>                                <span class="st">&quot;https://t.co/[A-Za-z</span><span class="sc">\\</span><span class="st">d]+|&amp;amp;&quot;</span>, </span>
<span id="cb12-9"><a href="#cb12-9" aria-hidden="true" tabindex="-1"></a>                                <span class="st">&quot;&quot;</span>)) <span class="sc">%&gt;%</span></span>
<span id="cb12-10"><a href="#cb12-10" aria-hidden="true" tabindex="-1"></a>  <span class="fu">unnest_tokens</span>(word, text, </span>
<span id="cb12-11"><a href="#cb12-11" aria-hidden="true" tabindex="-1"></a>                <span class="at">token =</span> <span class="st">&quot;regex&quot;</span>, </span>
<span id="cb12-12"><a href="#cb12-12" aria-hidden="true" tabindex="-1"></a>                <span class="at">pattern =</span> reg) <span class="sc">%&gt;%</span></span>
<span id="cb12-13"><a href="#cb12-13" aria-hidden="true" tabindex="-1"></a>  <span class="fu">filter</span>(<span class="sc">!</span>word <span class="sc">%in%</span> stop_words<span class="sc">$</span>word,</span>
<span id="cb12-14"><a href="#cb12-14" aria-hidden="true" tabindex="-1"></a>         <span class="fu">str_detect</span>(word, <span class="st">&quot;[a-z]&quot;</span>))</span>
<span id="cb12-15"><a href="#cb12-15" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb12-16"><a href="#cb12-16" aria-hidden="true" tabindex="-1"></a>tiktok_words <span class="ot">&lt;-</span> </span>
<span id="cb12-17"><a href="#cb12-17" aria-hidden="true" tabindex="-1"></a>  tiktok <span class="sc">%&gt;%</span></span>
<span id="cb12-18"><a href="#cb12-18" aria-hidden="true" tabindex="-1"></a>  <span class="fu">filter</span>(<span class="sc">!</span><span class="fu">str_detect</span>(text, <span class="st">&#39;^&quot;&#39;</span>)) <span class="sc">%&gt;%</span></span>
<span id="cb12-19"><a href="#cb12-19" aria-hidden="true" tabindex="-1"></a>  <span class="fu">mutate</span>(<span class="at">text =</span> <span class="fu">str_replace_all</span>(text, </span>
<span id="cb12-20"><a href="#cb12-20" aria-hidden="true" tabindex="-1"></a>                                <span class="st">&quot;https://t.co/[A-Za-z</span><span class="sc">\\</span><span class="st">d]+|&amp;amp;&quot;</span>, </span>
<span id="cb12-21"><a href="#cb12-21" aria-hidden="true" tabindex="-1"></a>                                <span class="st">&quot;&quot;</span>)) <span class="sc">%&gt;%</span></span>
<span id="cb12-22"><a href="#cb12-22" aria-hidden="true" tabindex="-1"></a>  <span class="fu">unnest_tokens</span>(word, text, </span>
<span id="cb12-23"><a href="#cb12-23" aria-hidden="true" tabindex="-1"></a>                <span class="at">token =</span> <span class="st">&quot;regex&quot;</span>, </span>
<span id="cb12-24"><a href="#cb12-24" aria-hidden="true" tabindex="-1"></a>                <span class="at">pattern =</span> reg) <span class="sc">%&gt;%</span></span>
<span id="cb12-25"><a href="#cb12-25" aria-hidden="true" tabindex="-1"></a>  <span class="fu">filter</span>(<span class="sc">!</span>word <span class="sc">%in%</span> stop_words<span class="sc">$</span>word,</span>
<span id="cb12-26"><a href="#cb12-26" aria-hidden="true" tabindex="-1"></a>         <span class="fu">str_detect</span>(word, <span class="st">&quot;[a-z]&quot;</span>))</span>
<span id="cb12-27"><a href="#cb12-27" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb12-28"><a href="#cb12-28" aria-hidden="true" tabindex="-1"></a><span class="co"># Inspect the first six rows of tweet_words</span></span>
<span id="cb12-29"><a href="#cb12-29" aria-hidden="true" tabindex="-1"></a><span class="fu">head</span>(fb_words)</span></code></pre></div>
<pre><code>## # A tibble: 6 x 4
##   status_id            source          created_at          word        
##   &lt;chr&gt;                &lt;chr&gt;           &lt;dttm&gt;              &lt;chr&gt;       
## 1 x1382020080343470082 Twitter Web App 2021-04-13 17:17:18 ramadan     
## 2 x1382020080343470082 Twitter Web App 2021-04-13 17:17:18 mubarak     
## 3 x1382020080343470082 Twitter Web App 2021-04-13 17:17:18 0001f319    
## 4 x1382020080343470082 Twitter Web App 2021-04-13 17:17:18 #monthofgood
## 5 x1382020080343470082 Twitter Web App 2021-04-13 17:17:18 check       
## 6 x1382020080343470082 Twitter Web App 2021-04-13 17:17:18 kindness</code></pre>
<p>We produce two horizontal bar graphs that show the most common words along with a word cloud for each user.</p>
<div class="sourceCode" id="cb14"><pre class="sourceCode r"><code class="sourceCode r"><span id="cb14-1"><a href="#cb14-1" aria-hidden="true" tabindex="-1"></a>fb_most_common <span class="ot">&lt;-</span> </span>
<span id="cb14-2"><a href="#cb14-2" aria-hidden="true" tabindex="-1"></a>  fb_words <span class="sc">%&gt;%</span></span>
<span id="cb14-3"><a href="#cb14-3" aria-hidden="true" tabindex="-1"></a>  <span class="fu">count</span>(word, <span class="at">sort =</span> <span class="cn">TRUE</span>) <span class="sc">%&gt;%</span></span>
<span id="cb14-4"><a href="#cb14-4" aria-hidden="true" tabindex="-1"></a>  <span class="fu">head</span>(<span class="dv">20</span>) <span class="sc">%&gt;%</span></span>
<span id="cb14-5"><a href="#cb14-5" aria-hidden="true" tabindex="-1"></a>  <span class="fu">mutate</span>(<span class="at">word =</span> <span class="fu">reorder</span>(word, n))</span>
<span id="cb14-6"><a href="#cb14-6" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb14-7"><a href="#cb14-7" aria-hidden="true" tabindex="-1"></a>fb_most_common <span class="sc">%&gt;%</span></span>
<span id="cb14-8"><a href="#cb14-8" aria-hidden="true" tabindex="-1"></a>  <span class="fu">ggplot</span>(<span class="fu">aes</span>(<span class="at">x =</span> word, <span class="at">y =</span> n)) <span class="sc">+</span></span>
<span id="cb14-9"><a href="#cb14-9" aria-hidden="true" tabindex="-1"></a>  <span class="fu">geom_bar</span>(<span class="at">stat =</span> <span class="st">&quot;identity&quot;</span>) <span class="sc">+</span></span>
<span id="cb14-10"><a href="#cb14-10" aria-hidden="true" tabindex="-1"></a>  <span class="fu">ylab</span>(<span class="st">&quot;Occurrences&quot;</span>) <span class="sc">+</span></span>
<span id="cb14-11"><a href="#cb14-11" aria-hidden="true" tabindex="-1"></a>  <span class="fu">coord_flip</span>() <span class="sc">+</span> </span>
<span id="cb14-12"><a href="#cb14-12" aria-hidden="true" tabindex="-1"></a>  <span class="fu">ggtitle</span>(<span class="st">&quot;Facebook Word Frequency&quot;</span>)</span></code></pre></div>
<p><img src="figure-html/unnamed-chunk-8-1.png" width="672" /></p>
<div class="sourceCode" id="cb15"><pre class="sourceCode r"><code class="sourceCode r"><span id="cb15-1"><a href="#cb15-1" aria-hidden="true" tabindex="-1"></a>tiktok_most_common <span class="ot">&lt;-</span> </span>
<span id="cb15-2"><a href="#cb15-2" aria-hidden="true" tabindex="-1"></a>  tiktok_words <span class="sc">%&gt;%</span></span>
<span id="cb15-3"><a href="#cb15-3" aria-hidden="true" tabindex="-1"></a>  <span class="fu">count</span>(word, <span class="at">sort =</span> <span class="cn">TRUE</span>) <span class="sc">%&gt;%</span></span>
<span id="cb15-4"><a href="#cb15-4" aria-hidden="true" tabindex="-1"></a>  <span class="fu">head</span>(<span class="dv">20</span>) <span class="sc">%&gt;%</span></span>
<span id="cb15-5"><a href="#cb15-5" aria-hidden="true" tabindex="-1"></a>  <span class="fu">mutate</span>(<span class="at">word =</span> <span class="fu">reorder</span>(word, n))</span>
<span id="cb15-6"><a href="#cb15-6" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb15-7"><a href="#cb15-7" aria-hidden="true" tabindex="-1"></a>tiktok_most_common <span class="sc">%&gt;%</span></span>
<span id="cb15-8"><a href="#cb15-8" aria-hidden="true" tabindex="-1"></a>  <span class="fu">ggplot</span>(<span class="fu">aes</span>(<span class="at">x =</span> word, <span class="at">y =</span> n)) <span class="sc">+</span></span>
<span id="cb15-9"><a href="#cb15-9" aria-hidden="true" tabindex="-1"></a>  <span class="fu">geom_bar</span>(<span class="at">stat =</span> <span class="st">&quot;identity&quot;</span>) <span class="sc">+</span></span>
<span id="cb15-10"><a href="#cb15-10" aria-hidden="true" tabindex="-1"></a>  <span class="fu">ylab</span>(<span class="st">&quot;Occurrences&quot;</span>) <span class="sc">+</span></span>
<span id="cb15-11"><a href="#cb15-11" aria-hidden="true" tabindex="-1"></a>  <span class="fu">coord_flip</span>() <span class="sc">+</span></span>
<span id="cb15-12"><a href="#cb15-12" aria-hidden="true" tabindex="-1"></a>  <span class="fu">ggtitle</span>(<span class="st">&quot;TikTok Word Frequency&quot;</span>)</span></code></pre></div>
<p><img src="figure-html/unnamed-chunk-8-2.png" width="672" /></p>
<div class="sourceCode" id="cb16"><pre class="sourceCode r"><code class="sourceCode r"><span id="cb16-1"><a href="#cb16-1" aria-hidden="true" tabindex="-1"></a>facebook_cloud <span class="ot">&lt;-</span> </span>
<span id="cb16-2"><a href="#cb16-2" aria-hidden="true" tabindex="-1"></a>  fb_words  <span class="sc">%&gt;%</span> </span>
<span id="cb16-3"><a href="#cb16-3" aria-hidden="true" tabindex="-1"></a>  <span class="fu">count</span>(word) <span class="sc">%&gt;%</span> </span>
<span id="cb16-4"><a href="#cb16-4" aria-hidden="true" tabindex="-1"></a>  <span class="fu">arrange</span>(<span class="sc">-</span>n)</span>
<span id="cb16-5"><a href="#cb16-5" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb16-6"><a href="#cb16-6" aria-hidden="true" tabindex="-1"></a><span class="fu">wordcloud</span>(facebook_cloud<span class="sc">$</span>word, </span>
<span id="cb16-7"><a href="#cb16-7" aria-hidden="true" tabindex="-1"></a>          facebook_cloud<span class="sc">$</span>n, <span class="at">max.words =</span> <span class="dv">200</span>, </span>
<span id="cb16-8"><a href="#cb16-8" aria-hidden="true" tabindex="-1"></a>          <span class="at">colors =</span> <span class="fu">c</span>(<span class="st">&quot;#00B2FF&quot;</span>, <span class="st">&quot;red&quot;</span>, </span>
<span id="cb16-9"><a href="#cb16-9" aria-hidden="true" tabindex="-1"></a>                     <span class="st">&quot;#FF0099&quot;</span>, <span class="st">&quot;#6600CC&quot;</span>, </span>
<span id="cb16-10"><a href="#cb16-10" aria-hidden="true" tabindex="-1"></a>                     <span class="st">&quot;green&quot;</span>, <span class="st">&quot;orange&quot;</span>, </span>
<span id="cb16-11"><a href="#cb16-11" aria-hidden="true" tabindex="-1"></a>                     <span class="st">&quot;blue&quot;</span>, <span class="st">&quot;brown&quot;</span>))</span></code></pre></div>
<p><img src="figure-html/unnamed-chunk-8-3.png" width="672" /></p>
<div class="sourceCode" id="cb17"><pre class="sourceCode r"><code class="sourceCode r"><span id="cb17-1"><a href="#cb17-1" aria-hidden="true" tabindex="-1"></a>tiktok_cloud <span class="ot">&lt;-</span> </span>
<span id="cb17-2"><a href="#cb17-2" aria-hidden="true" tabindex="-1"></a>  tiktok_words  <span class="sc">%&gt;%</span> </span>
<span id="cb17-3"><a href="#cb17-3" aria-hidden="true" tabindex="-1"></a>  <span class="fu">count</span>(word) <span class="sc">%&gt;%</span> </span>
<span id="cb17-4"><a href="#cb17-4" aria-hidden="true" tabindex="-1"></a>  <span class="fu">arrange</span>(<span class="sc">-</span>n)</span>
<span id="cb17-5"><a href="#cb17-5" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb17-6"><a href="#cb17-6" aria-hidden="true" tabindex="-1"></a><span class="fu">wordcloud</span>(tiktok_cloud<span class="sc">$</span>word, </span>
<span id="cb17-7"><a href="#cb17-7" aria-hidden="true" tabindex="-1"></a>          tiktok_cloud<span class="sc">$</span>n, <span class="at">max.words =</span> <span class="dv">200</span>, </span>
<span id="cb17-8"><a href="#cb17-8" aria-hidden="true" tabindex="-1"></a>          <span class="at">colors =</span> <span class="fu">c</span>(<span class="st">&quot;#00B2FF&quot;</span>, <span class="st">&quot;red&quot;</span>, </span>
<span id="cb17-9"><a href="#cb17-9" aria-hidden="true" tabindex="-1"></a>                     <span class="st">&quot;#FF0099&quot;</span>, <span class="st">&quot;#6600CC&quot;</span>, </span>
<span id="cb17-10"><a href="#cb17-10" aria-hidden="true" tabindex="-1"></a>                     <span class="st">&quot;green&quot;</span>, <span class="st">&quot;orange&quot;</span>, </span>
<span id="cb17-11"><a href="#cb17-11" aria-hidden="true" tabindex="-1"></a>                     <span class="st">&quot;blue&quot;</span>, <span class="st">&quot;brown&quot;</span>))</span></code></pre></div>
<p><img src="figure-html/unnamed-chunk-8-4.png" width="672" /></p>
<p>The most common word that Facebook uses is ???kn,??? and it???s unclear what this means. We did a quick search and found that Facebook signs off a lot of its replies with ???-KN.??? See here: <a href="https://twitter.com/Facebook/status/1185298970832244736" class="uri">https://twitter.com/Facebook/status/1185298970832244736</a></p>
<p>Facebook frequently uses neutral and security-/support-related words: ???account,??? ???report,??? ???secure,??? ???experiencing,??? etc.</p>
<p>TikTok uses a lot more anticipatory words like ???tomorrow,??? ???prizes,??? ???nomination,??? ???winner.??? TikTok???s Twitter account actually has a lot of sweepstakes.</p>
<p>Both accounts, of course, reference their own company names frequently.</p>
<p>We will use the number of times these forty words appear as predictors in our model.</p>
<p>We now join the NRC Word-Emotion Association Lexicon to our data, which will allow us to identify words associated with eight basic emotions (anger, fear, anticipation, trust, surprise, sadness, joy, and disgust) and two sentiments (negative and positive).</p>
<div class="sourceCode" id="cb18"><pre class="sourceCode r"><code class="sourceCode r"><span id="cb18-1"><a href="#cb18-1" aria-hidden="true" tabindex="-1"></a>fb_sentiment <span class="ot">&lt;-</span></span>
<span id="cb18-2"><a href="#cb18-2" aria-hidden="true" tabindex="-1"></a>  <span class="fu">inner_join</span>(fb_words, nrc, <span class="at">by =</span> <span class="st">&quot;word&quot;</span>)</span>
<span id="cb18-3"><a href="#cb18-3" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb18-4"><a href="#cb18-4" aria-hidden="true" tabindex="-1"></a>tiktok_sentiment <span class="ot">&lt;-</span></span>
<span id="cb18-5"><a href="#cb18-5" aria-hidden="true" tabindex="-1"></a>  <span class="fu">inner_join</span>(tiktok_words, nrc, <span class="at">by =</span> <span class="st">&quot;word&quot;</span>)</span>
<span id="cb18-6"><a href="#cb18-6" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb18-7"><a href="#cb18-7" aria-hidden="true" tabindex="-1"></a>fb_sentiment <span class="sc">%&gt;%</span> <span class="fu">head</span>()</span></code></pre></div>
<pre><code>## # A tibble: 6 x 5
##   status_id            source          created_at          word      sentiment   
##   &lt;chr&gt;                &lt;chr&gt;           &lt;dttm&gt;              &lt;chr&gt;     &lt;chr&gt;       
## 1 x1382020080343470082 Twitter Web App 2021-04-13 17:17:18 kindness  positive    
## 2 x1381733382632001536 Khoros CX       2021-04-12 22:18:04 happy     anticipation
## 3 x1381733382632001536 Khoros CX       2021-04-12 22:18:04 happy     joy         
## 4 x1381733382632001536 Khoros CX       2021-04-12 22:18:04 happy     positive    
## 5 x1381733382632001536 Khoros CX       2021-04-12 22:18:04 happy     trust       
## 6 x1381733382632001536 Khoros CX       2021-04-12 22:18:04 wonderful joy</code></pre>
<p>Here, we compare Facebook???s and TikTok???s sentiments.</p>
<div class="sourceCode" id="cb20"><pre class="sourceCode r"><code class="sourceCode r"><span id="cb20-1"><a href="#cb20-1" aria-hidden="true" tabindex="-1"></a>fb_sentiment_analysis <span class="ot">&lt;-</span> </span>
<span id="cb20-2"><a href="#cb20-2" aria-hidden="true" tabindex="-1"></a>  fb_sentiment <span class="sc">%&gt;%</span> </span>
<span id="cb20-3"><a href="#cb20-3" aria-hidden="true" tabindex="-1"></a>  <span class="fu">count</span>(word, sentiment) <span class="sc">%&gt;%</span> </span>
<span id="cb20-4"><a href="#cb20-4" aria-hidden="true" tabindex="-1"></a>  <span class="fu">group_by</span>(sentiment)</span>
<span id="cb20-5"><a href="#cb20-5" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb20-6"><a href="#cb20-6" aria-hidden="true" tabindex="-1"></a>fb_sentiment_analysis <span class="sc">%&gt;%</span>  </span>
<span id="cb20-7"><a href="#cb20-7" aria-hidden="true" tabindex="-1"></a>  <span class="fu">top_n</span>(<span class="dv">15</span>) <span class="sc">%&gt;%</span> </span>
<span id="cb20-8"><a href="#cb20-8" aria-hidden="true" tabindex="-1"></a>  <span class="fu">ggplot</span>(<span class="fu">aes</span>(<span class="at">x =</span> sentiment, <span class="at">y =</span> n )) <span class="sc">+</span></span>
<span id="cb20-9"><a href="#cb20-9" aria-hidden="true" tabindex="-1"></a>  <span class="fu">geom_bar</span>(<span class="at">stat =</span> <span class="st">&quot;identity&quot;</span>) <span class="sc">+</span></span>
<span id="cb20-10"><a href="#cb20-10" aria-hidden="true" tabindex="-1"></a>  <span class="fu">coord_flip</span>() <span class="sc">+</span></span>
<span id="cb20-11"><a href="#cb20-11" aria-hidden="true" tabindex="-1"></a>  <span class="fu">ylab</span>(<span class="st">&quot;Frequency&quot;</span>) <span class="sc">+</span></span>
<span id="cb20-12"><a href="#cb20-12" aria-hidden="true" tabindex="-1"></a>  <span class="fu">xlab</span>(<span class="st">&quot;Sentiment&quot;</span>) <span class="sc">+</span></span>
<span id="cb20-13"><a href="#cb20-13" aria-hidden="true" tabindex="-1"></a>  <span class="fu">labs</span>(<span class="at">title=</span><span class="st">&quot;Facebook Sentiment&quot;</span>)</span></code></pre></div>
<p><img src="figure-html/unnamed-chunk-10-1.png" width="672" /></p>
<div class="sourceCode" id="cb21"><pre class="sourceCode r"><code class="sourceCode r"><span id="cb21-1"><a href="#cb21-1" aria-hidden="true" tabindex="-1"></a>tiktok_sentiment_analysis <span class="ot">&lt;-</span> </span>
<span id="cb21-2"><a href="#cb21-2" aria-hidden="true" tabindex="-1"></a>  tiktok_sentiment <span class="sc">%&gt;%</span> </span>
<span id="cb21-3"><a href="#cb21-3" aria-hidden="true" tabindex="-1"></a>  <span class="fu">count</span>(word, sentiment) <span class="sc">%&gt;%</span> </span>
<span id="cb21-4"><a href="#cb21-4" aria-hidden="true" tabindex="-1"></a>  <span class="fu">group_by</span>(sentiment)</span>
<span id="cb21-5"><a href="#cb21-5" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb21-6"><a href="#cb21-6" aria-hidden="true" tabindex="-1"></a>tiktok_sentiment_analysis <span class="sc">%&gt;%</span>  </span>
<span id="cb21-7"><a href="#cb21-7" aria-hidden="true" tabindex="-1"></a>  <span class="fu">top_n</span>(<span class="dv">15</span>) <span class="sc">%&gt;%</span> </span>
<span id="cb21-8"><a href="#cb21-8" aria-hidden="true" tabindex="-1"></a>  <span class="fu">ggplot</span>(<span class="fu">aes</span>(<span class="at">x =</span> sentiment, <span class="at">y =</span> n )) <span class="sc">+</span></span>
<span id="cb21-9"><a href="#cb21-9" aria-hidden="true" tabindex="-1"></a>  <span class="fu">geom_bar</span>(<span class="at">stat =</span> <span class="st">&quot;identity&quot;</span>) <span class="sc">+</span></span>
<span id="cb21-10"><a href="#cb21-10" aria-hidden="true" tabindex="-1"></a>  <span class="fu">coord_flip</span>() <span class="sc">+</span></span>
<span id="cb21-11"><a href="#cb21-11" aria-hidden="true" tabindex="-1"></a>  <span class="fu">ylab</span>(<span class="st">&quot;Frequency&quot;</span>) <span class="sc">+</span></span>
<span id="cb21-12"><a href="#cb21-12" aria-hidden="true" tabindex="-1"></a>  <span class="fu">xlab</span>(<span class="st">&quot;Sentiment&quot;</span>) <span class="sc">+</span></span>
<span id="cb21-13"><a href="#cb21-13" aria-hidden="true" tabindex="-1"></a>  <span class="fu">labs</span>(<span class="at">title=</span><span class="st">&quot;TikTok Sentiment&quot;</span>)</span></code></pre></div>
<p><img src="figure-html/unnamed-chunk-10-2.png" width="672" /></p>
<p>It looks like Facebook???s tweets use more trust words while TikTok uses more words that reflect anticipation. We now show specifically which words are conveying each of these observed sentiments.</p>
<div class="sourceCode" id="cb22"><pre class="sourceCode r"><code class="sourceCode r"><span id="cb22-1"><a href="#cb22-1" aria-hidden="true" tabindex="-1"></a>fb_sentiment_analysis <span class="sc">%&gt;%</span> <span class="fu">filter</span>(<span class="sc">!</span>sentiment <span class="sc">%in%</span> <span class="fu">c</span>(<span class="st">&quot;positive&quot;</span>, <span class="st">&quot;negative&quot;</span>)) <span class="sc">%&gt;%</span> </span>
<span id="cb22-2"><a href="#cb22-2" aria-hidden="true" tabindex="-1"></a>  <span class="fu">mutate</span>(<span class="at">sentiment =</span> <span class="fu">reorder</span>(sentiment, <span class="sc">-</span>n),</span>
<span id="cb22-3"><a href="#cb22-3" aria-hidden="true" tabindex="-1"></a>         <span class="at">word =</span> <span class="fu">reorder</span>(word, <span class="sc">-</span>n)) <span class="sc">%&gt;%</span> <span class="fu">top_n</span>(<span class="dv">10</span>) <span class="ot">-&gt;</span> fb_sentiment_analysis2</span>
<span id="cb22-4"><a href="#cb22-4" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb22-5"><a href="#cb22-5" aria-hidden="true" tabindex="-1"></a><span class="fu">ggplot</span>(fb_sentiment_analysis2, <span class="fu">aes</span>(<span class="at">x=</span>word, <span class="at">y=</span>n, <span class="at">fill =</span> n)) <span class="sc">+</span></span>
<span id="cb22-6"><a href="#cb22-6" aria-hidden="true" tabindex="-1"></a>  <span class="fu">facet_wrap</span>(<span class="sc">~</span> sentiment, <span class="at">scales =</span> <span class="st">&quot;free&quot;</span>)<span class="sc">+</span> </span>
<span id="cb22-7"><a href="#cb22-7" aria-hidden="true" tabindex="-1"></a>  <span class="fu">geom_bar</span>(<span class="at">stat =</span><span class="st">&quot;identity&quot;</span>) <span class="sc">+</span></span>
<span id="cb22-8"><a href="#cb22-8" aria-hidden="true" tabindex="-1"></a>  <span class="fu">theme</span>(<span class="at">axis.text.x =</span> <span class="fu">element_text</span>(<span class="at">angle =</span> <span class="dv">90</span>, <span class="at">hjust =</span> <span class="dv">1</span>)) <span class="sc">+</span> </span>
<span id="cb22-9"><a href="#cb22-9" aria-hidden="true" tabindex="-1"></a>  <span class="fu">labs</span>(<span class="at">y=</span><span class="st">&quot;count&quot;</span>, <span class="at">title=</span><span class="st">&quot;Facebook Sentiment Words&quot;</span>)</span></code></pre></div>
<p><img src="figure-html/unnamed-chunk-11-1.png" width="672" /></p>
<div class="sourceCode" id="cb23"><pre class="sourceCode r"><code class="sourceCode r"><span id="cb23-1"><a href="#cb23-1" aria-hidden="true" tabindex="-1"></a>tiktok_sentiment_analysis <span class="sc">%&gt;%</span> <span class="fu">filter</span>(<span class="sc">!</span>sentiment <span class="sc">%in%</span> <span class="fu">c</span>(<span class="st">&quot;positive&quot;</span>, <span class="st">&quot;negative&quot;</span>)) <span class="sc">%&gt;%</span> </span>
<span id="cb23-2"><a href="#cb23-2" aria-hidden="true" tabindex="-1"></a>  <span class="fu">mutate</span>(<span class="at">sentiment =</span> <span class="fu">reorder</span>(sentiment, <span class="sc">-</span>n),</span>
<span id="cb23-3"><a href="#cb23-3" aria-hidden="true" tabindex="-1"></a>         <span class="at">word =</span> <span class="fu">reorder</span>(word, <span class="sc">-</span>n)) <span class="sc">%&gt;%</span> <span class="fu">top_n</span>(<span class="dv">10</span>) <span class="ot">-&gt;</span> tiktok_sentiment_analysis2</span>
<span id="cb23-4"><a href="#cb23-4" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb23-5"><a href="#cb23-5" aria-hidden="true" tabindex="-1"></a><span class="fu">ggplot</span>(tiktok_sentiment_analysis2, <span class="fu">aes</span>(<span class="at">x=</span>word, <span class="at">y=</span>n, <span class="at">fill =</span> n)) <span class="sc">+</span></span>
<span id="cb23-6"><a href="#cb23-6" aria-hidden="true" tabindex="-1"></a>  <span class="fu">facet_wrap</span>(<span class="sc">~</span> sentiment, <span class="at">scales =</span> <span class="st">&quot;free&quot;</span>)<span class="sc">+</span> </span>
<span id="cb23-7"><a href="#cb23-7" aria-hidden="true" tabindex="-1"></a>  <span class="fu">geom_bar</span>(<span class="at">stat =</span><span class="st">&quot;identity&quot;</span>) <span class="sc">+</span></span>
<span id="cb23-8"><a href="#cb23-8" aria-hidden="true" tabindex="-1"></a>  <span class="fu">theme</span>(<span class="at">axis.text.x =</span> <span class="fu">element_text</span>(<span class="at">angle =</span> <span class="dv">90</span>, <span class="at">hjust =</span> <span class="dv">1</span>)) <span class="sc">+</span> </span>
<span id="cb23-9"><a href="#cb23-9" aria-hidden="true" tabindex="-1"></a>  <span class="fu">labs</span>(<span class="at">y=</span><span class="st">&quot;count&quot;</span>, <span class="at">title=</span><span class="st">&quot;Tik Tok Sentiment Words&quot;</span>)</span></code></pre></div>
<p><img src="figure-html/unnamed-chunk-11-2.png" width="672" /></p>
<p>Next, we examine texts on Facebook and Tiktok to see their positive-negative score by using the AFINN sentiment lexicon, a list of English terms manually rated for valence with an integer between -5 (negative) and +5 (positive) by Finn ??rup Nielsen between 2009 and 2011.</p>
<p>We use this lexicon to compute mean positivity scores for all words tweeted by each user.</p>
<div class="sourceCode" id="cb24"><pre class="sourceCode r"><code class="sourceCode r"><span id="cb24-1"><a href="#cb24-1" aria-hidden="true" tabindex="-1"></a><span class="co"># run this to get afinn lexicon and save it as a csv</span></span>
<span id="cb24-2"><a href="#cb24-2" aria-hidden="true" tabindex="-1"></a><span class="co"># get_sentiments (&quot;afinn&quot;) -&gt; afinn</span></span>
<span id="cb24-3"><a href="#cb24-3" aria-hidden="true" tabindex="-1"></a><span class="co">#</span></span>
<span id="cb24-4"><a href="#cb24-4" aria-hidden="true" tabindex="-1"></a><span class="co">#afinn %&gt;% write_as_csv(&quot;afinn.csv&quot;)</span></span>
<span id="cb24-5"><a href="#cb24-5" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb24-6"><a href="#cb24-6" aria-hidden="true" tabindex="-1"></a>afinn <span class="ot">&lt;-</span> <span class="fu">read_csv</span>(<span class="st">&#39;afinn.csv&#39;</span>)</span>
<span id="cb24-7"><a href="#cb24-7" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb24-8"><a href="#cb24-8" aria-hidden="true" tabindex="-1"></a>fb_afinn <span class="ot">&lt;-</span>    </span>
<span id="cb24-9"><a href="#cb24-9" aria-hidden="true" tabindex="-1"></a> <span class="fu">inner_join</span>(fb_words, </span>
<span id="cb24-10"><a href="#cb24-10" aria-hidden="true" tabindex="-1"></a>            afinn, </span>
<span id="cb24-11"><a href="#cb24-11" aria-hidden="true" tabindex="-1"></a>            <span class="at">by =</span> <span class="st">&quot;word&quot;</span>)</span>
<span id="cb24-12"><a href="#cb24-12" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb24-13"><a href="#cb24-13" aria-hidden="true" tabindex="-1"></a>tiktok_afinn <span class="ot">&lt;-</span>    </span>
<span id="cb24-14"><a href="#cb24-14" aria-hidden="true" tabindex="-1"></a> <span class="fu">inner_join</span>(tiktok_words, </span>
<span id="cb24-15"><a href="#cb24-15" aria-hidden="true" tabindex="-1"></a>            afinn, </span>
<span id="cb24-16"><a href="#cb24-16" aria-hidden="true" tabindex="-1"></a>            <span class="at">by =</span> <span class="st">&quot;word&quot;</span>)</span>
<span id="cb24-17"><a href="#cb24-17" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb24-18"><a href="#cb24-18" aria-hidden="true" tabindex="-1"></a>fb_mean_afinn <span class="ot">&lt;-</span> </span>
<span id="cb24-19"><a href="#cb24-19" aria-hidden="true" tabindex="-1"></a>  fb_afinn <span class="sc">%&gt;%</span> </span>
<span id="cb24-20"><a href="#cb24-20" aria-hidden="true" tabindex="-1"></a>  <span class="fu">summarise</span>(<span class="at">mean_fb_afinn =</span> <span class="fu">mean</span>(value))</span>
<span id="cb24-21"><a href="#cb24-21" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb24-22"><a href="#cb24-22" aria-hidden="true" tabindex="-1"></a>tiktok_mean_afinn <span class="ot">&lt;-</span> </span>
<span id="cb24-23"><a href="#cb24-23" aria-hidden="true" tabindex="-1"></a>  tiktok_afinn <span class="sc">%&gt;%</span> </span>
<span id="cb24-24"><a href="#cb24-24" aria-hidden="true" tabindex="-1"></a>  <span class="fu">summarise</span>(<span class="at">mean_tt_afinn =</span> <span class="fu">mean</span>(value))</span>
<span id="cb24-25"><a href="#cb24-25" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb24-26"><a href="#cb24-26" aria-hidden="true" tabindex="-1"></a><span class="fu">cat</span>(<span class="fu">paste0</span>(<span class="st">&quot;Average AFINN scores for all words by user</span><span class="sc">\n</span><span class="st">&quot;</span>,</span>
<span id="cb24-27"><a href="#cb24-27" aria-hidden="true" tabindex="-1"></a>           <span class="st">&quot;</span><span class="sc">\n</span><span class="st">Facebook: &quot;</span>, <span class="fu">round</span>(fb_mean_afinn, <span class="dv">3</span>), </span>
<span id="cb24-28"><a href="#cb24-28" aria-hidden="true" tabindex="-1"></a>           <span class="st">&quot;</span><span class="sc">\n</span><span class="st">TikTok: &quot;</span>, <span class="fu">round</span>(tiktok_mean_afinn, <span class="dv">3</span>)))</span></code></pre></div>
<pre><code>## Average AFINN scores for all words by user
## 
## Facebook: 0.785
## TikTok: 1.704</code></pre>
<p>Facebook???s mean AFINN value is 0.79 while TikTok???s mean AFINN value is 1.704. In general, words tweeted by Tiktok are more positive than those tweeted by Facebook.</p>
</div>
<div id="v.-training-predictive-models" class="section level1">
<h1>V. Training Predictive Models</h1>
<p>Here, using the text of a tweet, we attempt to predict the user who tweeted it.</p>
<p>The features we extracted are tweet length, the number of times each of the twenty most common words from each account appear, the presence of a picture/link, number of words for each sentiment, and mean AFINN score per tweet.</p>
<p>TikTok is encoded as 1, and Facebook is encoded as 0.</p>
<p>First, we prepare the data for training and produce a simple decision tree.</p>
<div class="sourceCode" id="cb26"><pre class="sourceCode r"><code class="sourceCode r"><span id="cb26-1"><a href="#cb26-1" aria-hidden="true" tabindex="-1"></a>fbcommon <span class="ot">&lt;-</span> </span>
<span id="cb26-2"><a href="#cb26-2" aria-hidden="true" tabindex="-1"></a>  <span class="fu">lapply</span>(fb_most_common<span class="sc">$</span>word, as.character) <span class="sc">%&gt;%</span> </span>
<span id="cb26-3"><a href="#cb26-3" aria-hidden="true" tabindex="-1"></a>  <span class="fu">unlist</span>()</span>
<span id="cb26-4"><a href="#cb26-4" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb26-5"><a href="#cb26-5" aria-hidden="true" tabindex="-1"></a>tiktokcommon <span class="ot">&lt;-</span> </span>
<span id="cb26-6"><a href="#cb26-6" aria-hidden="true" tabindex="-1"></a>  <span class="fu">lapply</span>(tiktok_most_common<span class="sc">$</span>word, as.character) <span class="sc">%&gt;%</span> </span>
<span id="cb26-7"><a href="#cb26-7" aria-hidden="true" tabindex="-1"></a>  <span class="fu">unlist</span>()</span>
<span id="cb26-8"><a href="#cb26-8" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb26-9"><a href="#cb26-9" aria-hidden="true" tabindex="-1"></a>commonwords <span class="ot">&lt;-</span> <span class="fu">c</span>(tiktokcommon, fbcommon)</span>
<span id="cb26-10"><a href="#cb26-10" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb26-11"><a href="#cb26-11" aria-hidden="true" tabindex="-1"></a>fb_word_predict <span class="ot">&lt;-</span> </span>
<span id="cb26-12"><a href="#cb26-12" aria-hidden="true" tabindex="-1"></a>  fb_words <span class="sc">%&gt;%</span> </span>
<span id="cb26-13"><a href="#cb26-13" aria-hidden="true" tabindex="-1"></a>  <span class="fu">filter</span>(word <span class="sc">%in%</span> commonwords) <span class="sc">%&gt;%</span> </span>
<span id="cb26-14"><a href="#cb26-14" aria-hidden="true" tabindex="-1"></a>  <span class="fu">group_by</span>(status_id) <span class="sc">%&gt;%</span> </span>
<span id="cb26-15"><a href="#cb26-15" aria-hidden="true" tabindex="-1"></a>  <span class="fu">count</span>(word) <span class="sc">%&gt;%</span> </span>
<span id="cb26-16"><a href="#cb26-16" aria-hidden="true" tabindex="-1"></a>  <span class="fu">ungroup</span>() <span class="sc">%&gt;%</span> </span>
<span id="cb26-17"><a href="#cb26-17" aria-hidden="true" tabindex="-1"></a>  <span class="fu">pivot_wider</span>(<span class="at">id_cols =</span> status_id, </span>
<span id="cb26-18"><a href="#cb26-18" aria-hidden="true" tabindex="-1"></a>              <span class="at">names_from =</span> word, </span>
<span id="cb26-19"><a href="#cb26-19" aria-hidden="true" tabindex="-1"></a>              <span class="at">values_from =</span> n,</span>
<span id="cb26-20"><a href="#cb26-20" aria-hidden="true" tabindex="-1"></a>              <span class="at">values_fill =</span> <span class="dv">0</span>)</span>
<span id="cb26-21"><a href="#cb26-21" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb26-22"><a href="#cb26-22" aria-hidden="true" tabindex="-1"></a>tiktok_word_predict <span class="ot">&lt;-</span> </span>
<span id="cb26-23"><a href="#cb26-23" aria-hidden="true" tabindex="-1"></a>  tiktok_words <span class="sc">%&gt;%</span> </span>
<span id="cb26-24"><a href="#cb26-24" aria-hidden="true" tabindex="-1"></a>  <span class="fu">filter</span>(word <span class="sc">%in%</span> commonwords) <span class="sc">%&gt;%</span> </span>
<span id="cb26-25"><a href="#cb26-25" aria-hidden="true" tabindex="-1"></a>  <span class="fu">group_by</span>(status_id) <span class="sc">%&gt;%</span> </span>
<span id="cb26-26"><a href="#cb26-26" aria-hidden="true" tabindex="-1"></a>  <span class="fu">count</span>(word) <span class="sc">%&gt;%</span> </span>
<span id="cb26-27"><a href="#cb26-27" aria-hidden="true" tabindex="-1"></a>  <span class="fu">ungroup</span>() <span class="sc">%&gt;%</span> </span>
<span id="cb26-28"><a href="#cb26-28" aria-hidden="true" tabindex="-1"></a>  <span class="fu">pivot_wider</span>(<span class="at">id_cols =</span> status_id, </span>
<span id="cb26-29"><a href="#cb26-29" aria-hidden="true" tabindex="-1"></a>              <span class="at">names_from =</span> word, </span>
<span id="cb26-30"><a href="#cb26-30" aria-hidden="true" tabindex="-1"></a>              <span class="at">values_from =</span> n,</span>
<span id="cb26-31"><a href="#cb26-31" aria-hidden="true" tabindex="-1"></a>              <span class="at">values_fill =</span> <span class="dv">0</span>)</span>
<span id="cb26-32"><a href="#cb26-32" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb26-33"><a href="#cb26-33" aria-hidden="true" tabindex="-1"></a>fb_piclinks <span class="ot">&lt;-</span></span>
<span id="cb26-34"><a href="#cb26-34" aria-hidden="true" tabindex="-1"></a>  facebook <span class="sc">%&gt;%</span></span>
<span id="cb26-35"><a href="#cb26-35" aria-hidden="true" tabindex="-1"></a>  <span class="fu">filter</span>(<span class="sc">!</span><span class="fu">str_detect</span>(text, <span class="st">&#39;^&quot;&#39;</span>)) <span class="sc">%&gt;%</span></span>
<span id="cb26-36"><a href="#cb26-36" aria-hidden="true" tabindex="-1"></a>  <span class="fu">mutate</span>(<span class="at">picture_link =</span> <span class="fu">ifelse</span>(<span class="fu">str_detect</span>(text, <span class="st">&quot;t.co&quot;</span>),</span>
<span id="cb26-37"><a href="#cb26-37" aria-hidden="true" tabindex="-1"></a>                         <span class="dv">1</span>, <span class="dv">0</span>)) <span class="sc">%&gt;%</span> </span>
<span id="cb26-38"><a href="#cb26-38" aria-hidden="true" tabindex="-1"></a>  <span class="fu">select</span>(<span class="dv">1</span>,<span class="dv">5</span>)</span>
<span id="cb26-39"><a href="#cb26-39" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb26-40"><a href="#cb26-40" aria-hidden="true" tabindex="-1"></a>tiktok_piclinks <span class="ot">&lt;-</span> </span>
<span id="cb26-41"><a href="#cb26-41" aria-hidden="true" tabindex="-1"></a>  tiktok <span class="sc">%&gt;%</span></span>
<span id="cb26-42"><a href="#cb26-42" aria-hidden="true" tabindex="-1"></a>  <span class="fu">filter</span>(<span class="sc">!</span><span class="fu">str_detect</span>(text, <span class="st">&#39;^&quot;&#39;</span>)) <span class="sc">%&gt;%</span></span>
<span id="cb26-43"><a href="#cb26-43" aria-hidden="true" tabindex="-1"></a>  <span class="fu">mutate</span>(<span class="at">picture_link =</span> <span class="fu">ifelse</span>(<span class="fu">str_detect</span>(text, <span class="st">&quot;t.co&quot;</span>),</span>
<span id="cb26-44"><a href="#cb26-44" aria-hidden="true" tabindex="-1"></a>                         <span class="dv">1</span>, <span class="dv">0</span>)) <span class="sc">%&gt;%</span> </span>
<span id="cb26-45"><a href="#cb26-45" aria-hidden="true" tabindex="-1"></a>  <span class="fu">select</span>(<span class="dv">1</span>,<span class="dv">5</span>)</span>
<span id="cb26-46"><a href="#cb26-46" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb26-47"><a href="#cb26-47" aria-hidden="true" tabindex="-1"></a>fb_tweet_afinn <span class="ot">&lt;-</span> </span>
<span id="cb26-48"><a href="#cb26-48" aria-hidden="true" tabindex="-1"></a>  fb_afinn <span class="sc">%&gt;%</span> </span>
<span id="cb26-49"><a href="#cb26-49" aria-hidden="true" tabindex="-1"></a>  <span class="fu">group_by</span>(status_id) <span class="sc">%&gt;%</span> </span>
<span id="cb26-50"><a href="#cb26-50" aria-hidden="true" tabindex="-1"></a>  <span class="fu">summarize</span>(<span class="at">afinn =</span> <span class="fu">mean</span>(value))</span>
<span id="cb26-51"><a href="#cb26-51" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb26-52"><a href="#cb26-52" aria-hidden="true" tabindex="-1"></a>tiktok_tweet_afinn <span class="ot">&lt;-</span> </span>
<span id="cb26-53"><a href="#cb26-53" aria-hidden="true" tabindex="-1"></a>  tiktok_afinn <span class="sc">%&gt;%</span> </span>
<span id="cb26-54"><a href="#cb26-54" aria-hidden="true" tabindex="-1"></a>  <span class="fu">group_by</span>(status_id) <span class="sc">%&gt;%</span> </span>
<span id="cb26-55"><a href="#cb26-55" aria-hidden="true" tabindex="-1"></a>  <span class="fu">summarize</span>(<span class="at">afinn =</span> <span class="fu">mean</span>(value))</span>
<span id="cb26-56"><a href="#cb26-56" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb26-57"><a href="#cb26-57" aria-hidden="true" tabindex="-1"></a>fb_sentiment_counts <span class="ot">&lt;-</span> </span>
<span id="cb26-58"><a href="#cb26-58" aria-hidden="true" tabindex="-1"></a>  fb_sentiment <span class="sc">%&gt;%</span> </span>
<span id="cb26-59"><a href="#cb26-59" aria-hidden="true" tabindex="-1"></a>  <span class="fu">group_by</span>(status_id) <span class="sc">%&gt;%</span> </span>
<span id="cb26-60"><a href="#cb26-60" aria-hidden="true" tabindex="-1"></a>  <span class="fu">count</span>(sentiment) <span class="sc">%&gt;%</span> </span>
<span id="cb26-61"><a href="#cb26-61" aria-hidden="true" tabindex="-1"></a>  <span class="fu">ungroup</span>() <span class="sc">%&gt;%</span> </span>
<span id="cb26-62"><a href="#cb26-62" aria-hidden="true" tabindex="-1"></a>  <span class="fu">pivot_wider</span>(<span class="at">id_cols =</span> status_id, </span>
<span id="cb26-63"><a href="#cb26-63" aria-hidden="true" tabindex="-1"></a>              <span class="at">names_from =</span> sentiment, </span>
<span id="cb26-64"><a href="#cb26-64" aria-hidden="true" tabindex="-1"></a>              <span class="at">values_from =</span> n,</span>
<span id="cb26-65"><a href="#cb26-65" aria-hidden="true" tabindex="-1"></a>              <span class="at">values_fill =</span> <span class="dv">0</span>)</span>
<span id="cb26-66"><a href="#cb26-66" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb26-67"><a href="#cb26-67" aria-hidden="true" tabindex="-1"></a>tiktok_sentiment_counts <span class="ot">&lt;-</span> </span>
<span id="cb26-68"><a href="#cb26-68" aria-hidden="true" tabindex="-1"></a>  tiktok_sentiment <span class="sc">%&gt;%</span> </span>
<span id="cb26-69"><a href="#cb26-69" aria-hidden="true" tabindex="-1"></a>  <span class="fu">group_by</span>(status_id) <span class="sc">%&gt;%</span> </span>
<span id="cb26-70"><a href="#cb26-70" aria-hidden="true" tabindex="-1"></a>  <span class="fu">count</span>(sentiment) <span class="sc">%&gt;%</span> </span>
<span id="cb26-71"><a href="#cb26-71" aria-hidden="true" tabindex="-1"></a>  <span class="fu">ungroup</span>() <span class="sc">%&gt;%</span> </span>
<span id="cb26-72"><a href="#cb26-72" aria-hidden="true" tabindex="-1"></a>  <span class="fu">pivot_wider</span>(<span class="at">id_cols =</span> status_id, </span>
<span id="cb26-73"><a href="#cb26-73" aria-hidden="true" tabindex="-1"></a>              <span class="at">names_from =</span> sentiment, </span>
<span id="cb26-74"><a href="#cb26-74" aria-hidden="true" tabindex="-1"></a>              <span class="at">values_from =</span> n,</span>
<span id="cb26-75"><a href="#cb26-75" aria-hidden="true" tabindex="-1"></a>              <span class="at">values_fill =</span> <span class="dv">0</span>)</span>
<span id="cb26-76"><a href="#cb26-76" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb26-77"><a href="#cb26-77" aria-hidden="true" tabindex="-1"></a>tiktok_feature_selection <span class="ot">&lt;-</span> </span>
<span id="cb26-78"><a href="#cb26-78" aria-hidden="true" tabindex="-1"></a>  tiktok_wordcounts <span class="sc">%&gt;%</span> </span>
<span id="cb26-79"><a href="#cb26-79" aria-hidden="true" tabindex="-1"></a>  <span class="fu">mutate</span>(<span class="at">user =</span> <span class="dv">1</span>) <span class="sc">%&gt;%</span> </span>
<span id="cb26-80"><a href="#cb26-80" aria-hidden="true" tabindex="-1"></a>  <span class="fu">left_join</span>(tiktok_sentiment_counts, </span>
<span id="cb26-81"><a href="#cb26-81" aria-hidden="true" tabindex="-1"></a>            <span class="at">by=</span><span class="st">&quot;status_id&quot;</span>) <span class="sc">%&gt;%</span> </span>
<span id="cb26-82"><a href="#cb26-82" aria-hidden="true" tabindex="-1"></a>  <span class="fu">left_join</span>(tiktok_tweet_afinn,</span>
<span id="cb26-83"><a href="#cb26-83" aria-hidden="true" tabindex="-1"></a>            <span class="at">by=</span><span class="st">&quot;status_id&quot;</span>) <span class="sc">%&gt;%</span> </span>
<span id="cb26-84"><a href="#cb26-84" aria-hidden="true" tabindex="-1"></a>  <span class="fu">left_join</span>(tiktok_piclinks,</span>
<span id="cb26-85"><a href="#cb26-85" aria-hidden="true" tabindex="-1"></a>            <span class="at">by=</span><span class="st">&quot;status_id&quot;</span>) <span class="sc">%&gt;%</span> </span>
<span id="cb26-86"><a href="#cb26-86" aria-hidden="true" tabindex="-1"></a>  <span class="fu">left_join</span>(tiktok_word_predict,</span>
<span id="cb26-87"><a href="#cb26-87" aria-hidden="true" tabindex="-1"></a>            <span class="at">by =</span> <span class="st">&quot;status_id&quot;</span>)</span>
<span id="cb26-88"><a href="#cb26-88" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb26-89"><a href="#cb26-89" aria-hidden="true" tabindex="-1"></a>facebook_feature_selection <span class="ot">&lt;-</span></span>
<span id="cb26-90"><a href="#cb26-90" aria-hidden="true" tabindex="-1"></a>  fb_wordcounts <span class="sc">%&gt;%</span> </span>
<span id="cb26-91"><a href="#cb26-91" aria-hidden="true" tabindex="-1"></a>  <span class="fu">mutate</span>(<span class="at">user =</span> <span class="dv">0</span>) <span class="sc">%&gt;%</span> </span>
<span id="cb26-92"><a href="#cb26-92" aria-hidden="true" tabindex="-1"></a>  <span class="fu">left_join</span>(fb_sentiment_counts, </span>
<span id="cb26-93"><a href="#cb26-93" aria-hidden="true" tabindex="-1"></a>            <span class="at">by=</span><span class="st">&quot;status_id&quot;</span>) <span class="sc">%&gt;%</span> </span>
<span id="cb26-94"><a href="#cb26-94" aria-hidden="true" tabindex="-1"></a>  <span class="fu">left_join</span>(fb_tweet_afinn,</span>
<span id="cb26-95"><a href="#cb26-95" aria-hidden="true" tabindex="-1"></a>            <span class="at">by=</span><span class="st">&quot;status_id&quot;</span>) <span class="sc">%&gt;%</span> </span>
<span id="cb26-96"><a href="#cb26-96" aria-hidden="true" tabindex="-1"></a>  <span class="fu">left_join</span>(fb_piclinks,</span>
<span id="cb26-97"><a href="#cb26-97" aria-hidden="true" tabindex="-1"></a>            <span class="at">by=</span><span class="st">&quot;status_id&quot;</span>) <span class="sc">%&gt;%</span> </span>
<span id="cb26-98"><a href="#cb26-98" aria-hidden="true" tabindex="-1"></a>  <span class="fu">left_join</span>(fb_word_predict,</span>
<span id="cb26-99"><a href="#cb26-99" aria-hidden="true" tabindex="-1"></a>            <span class="at">by =</span> <span class="st">&quot;status_id&quot;</span>)</span>
<span id="cb26-100"><a href="#cb26-100" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb26-101"><a href="#cb26-101" aria-hidden="true" tabindex="-1"></a>both_users <span class="ot">&lt;-</span> </span>
<span id="cb26-102"><a href="#cb26-102" aria-hidden="true" tabindex="-1"></a>  tiktok_feature_selection <span class="sc">%&gt;%</span> </span>
<span id="cb26-103"><a href="#cb26-103" aria-hidden="true" tabindex="-1"></a>  dplyr<span class="sc">::</span><span class="fu">bind_rows</span>(facebook_feature_selection) <span class="sc">%&gt;%</span></span>
<span id="cb26-104"><a href="#cb26-104" aria-hidden="true" tabindex="-1"></a>  <span class="fu">mutate_if</span>(is.numeric,coalesce,<span class="dv">0</span>)</span>
<span id="cb26-105"><a href="#cb26-105" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb26-106"><a href="#cb26-106" aria-hidden="true" tabindex="-1"></a><span class="fu">set.seed</span>(<span class="dv">123</span>)</span>
<span id="cb26-107"><a href="#cb26-107" aria-hidden="true" tabindex="-1"></a>index <span class="ot">&lt;-</span> </span>
<span id="cb26-108"><a href="#cb26-108" aria-hidden="true" tabindex="-1"></a>  <span class="fu">createDataPartition</span>(both_users<span class="sc">$</span>user,</span>
<span id="cb26-109"><a href="#cb26-109" aria-hidden="true" tabindex="-1"></a>                      <span class="at">p =</span> <span class="fl">0.8</span>, <span class="at">list =</span> <span class="cn">FALSE</span>)</span>
<span id="cb26-110"><a href="#cb26-110" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb26-111"><a href="#cb26-111" aria-hidden="true" tabindex="-1"></a>for_decisiontree <span class="ot">&lt;-</span></span>
<span id="cb26-112"><a href="#cb26-112" aria-hidden="true" tabindex="-1"></a>  both_users <span class="sc">%&gt;%</span> <span class="fu">select</span>(<span class="sc">-</span><span class="dv">1</span>,<span class="sc">-</span><span class="dv">2</span>,<span class="sc">-</span><span class="dv">3</span>,<span class="sc">-</span><span class="dv">4</span>)</span>
<span id="cb26-113"><a href="#cb26-113" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb26-114"><a href="#cb26-114" aria-hidden="true" tabindex="-1"></a>train <span class="ot">&lt;-</span> for_decisiontree[index, ]</span>
<span id="cb26-115"><a href="#cb26-115" aria-hidden="true" tabindex="-1"></a>test  <span class="ot">&lt;-</span> for_decisiontree[<span class="sc">-</span>index, ]</span>
<span id="cb26-116"><a href="#cb26-116" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb26-117"><a href="#cb26-117" aria-hidden="true" tabindex="-1"></a><span class="fu">colnames</span>(train) <span class="ot">&lt;-</span> <span class="fu">make.names</span>(<span class="fu">colnames</span>(train))</span>
<span id="cb26-118"><a href="#cb26-118" aria-hidden="true" tabindex="-1"></a><span class="fu">colnames</span>(test) <span class="ot">&lt;-</span> <span class="fu">make.names</span>(<span class="fu">colnames</span>(test))</span>
<span id="cb26-119"><a href="#cb26-119" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb26-120"><a href="#cb26-120" aria-hidden="true" tabindex="-1"></a><span class="fu">set.seed</span>(<span class="dv">123</span>)</span>
<span id="cb26-121"><a href="#cb26-121" aria-hidden="true" tabindex="-1"></a>simple_model <span class="ot">&lt;-</span> <span class="fu">rpart</span>(user <span class="sc">~</span> ., </span>
<span id="cb26-122"><a href="#cb26-122" aria-hidden="true" tabindex="-1"></a>                      <span class="at">data =</span> train, <span class="at">method =</span> <span class="st">&quot;class&quot;</span>)</span>
<span id="cb26-123"><a href="#cb26-123" aria-hidden="true" tabindex="-1"></a><span class="fu">rpart.plot</span>(simple_model, <span class="at">yesno =</span> <span class="dv">2</span>)</span></code></pre></div>
<p><img src="figure-html/unnamed-chunk-13-1.png" width="672" /></p>
<p>It seems that the most dominant predictors in the simple model were the presence (or non-presence) of Facebook???s most common words, along with tweet length and the presence of the word ???tiktok.??? I suspect this will be similar for other models, though perhaps sentiment will play a role too.</p>
<p>We produce additional models using the bagging, random forests, and gradient boosting methods.</p>
<div class="sourceCode" id="cb27"><pre class="sourceCode r"><code class="sourceCode r"><span id="cb27-1"><a href="#cb27-1" aria-hidden="true" tabindex="-1"></a><span class="fu">set.seed</span>(<span class="dv">123</span>)</span>
<span id="cb27-2"><a href="#cb27-2" aria-hidden="true" tabindex="-1"></a>bagging_model <span class="ot">&lt;-</span> <span class="fu">train</span>(</span>
<span id="cb27-3"><a href="#cb27-3" aria-hidden="true" tabindex="-1"></a>  user <span class="sc">~</span> .,</span>
<span id="cb27-4"><a href="#cb27-4" aria-hidden="true" tabindex="-1"></a>  <span class="at">data =</span> train,</span>
<span id="cb27-5"><a href="#cb27-5" aria-hidden="true" tabindex="-1"></a>  <span class="at">method =</span> <span class="st">&quot;treebag&quot;</span>,</span>
<span id="cb27-6"><a href="#cb27-6" aria-hidden="true" tabindex="-1"></a>  <span class="at">trControl =</span> <span class="fu">trainControl</span>(<span class="at">method =</span> <span class="st">&quot;oob&quot;</span>),</span>
<span id="cb27-7"><a href="#cb27-7" aria-hidden="true" tabindex="-1"></a>  <span class="at">keepX =</span> T,</span>
<span id="cb27-8"><a href="#cb27-8" aria-hidden="true" tabindex="-1"></a>  <span class="at">nbagg =</span> <span class="dv">100</span>,</span>
<span id="cb27-9"><a href="#cb27-9" aria-hidden="true" tabindex="-1"></a>  <span class="at">importance =</span> <span class="st">&quot;impurity&quot;</span>,</span>
<span id="cb27-10"><a href="#cb27-10" aria-hidden="true" tabindex="-1"></a>  <span class="at">control =</span> <span class="fu">rpart.control</span>(<span class="at">minsplit =</span> <span class="dv">2</span>, <span class="at">cp =</span> <span class="dv">0</span>)</span>
<span id="cb27-11"><a href="#cb27-11" aria-hidden="true" tabindex="-1"></a>)</span>
<span id="cb27-12"><a href="#cb27-12" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb27-13"><a href="#cb27-13" aria-hidden="true" tabindex="-1"></a>n_features <span class="ot">&lt;-</span> <span class="fu">length</span>(<span class="fu">setdiff</span>(<span class="fu">names</span>(train), <span class="st">&quot;user&quot;</span>))</span>
<span id="cb27-14"><a href="#cb27-14" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb27-15"><a href="#cb27-15" aria-hidden="true" tabindex="-1"></a>train<span class="sc">$</span>user <span class="ot">&lt;-</span> <span class="fu">as.factor</span>(train<span class="sc">$</span>user)</span>
<span id="cb27-16"><a href="#cb27-16" aria-hidden="true" tabindex="-1"></a>rf_model <span class="ot">&lt;-</span> <span class="fu">ranger</span>(</span>
<span id="cb27-17"><a href="#cb27-17" aria-hidden="true" tabindex="-1"></a>  user <span class="sc">~</span> .,</span>
<span id="cb27-18"><a href="#cb27-18" aria-hidden="true" tabindex="-1"></a>  <span class="at">data =</span> train,</span>
<span id="cb27-19"><a href="#cb27-19" aria-hidden="true" tabindex="-1"></a>  <span class="at">mtry =</span> <span class="fu">floor</span>(n_features <span class="sc">*</span> <span class="fl">0.5</span>),</span>
<span id="cb27-20"><a href="#cb27-20" aria-hidden="true" tabindex="-1"></a>  <span class="at">respect.unordered.factors =</span> <span class="st">&quot;order&quot;</span>,</span>
<span id="cb27-21"><a href="#cb27-21" aria-hidden="true" tabindex="-1"></a>  <span class="at">importance =</span> <span class="st">&quot;permutation&quot;</span>,</span>
<span id="cb27-22"><a href="#cb27-22" aria-hidden="true" tabindex="-1"></a>  <span class="at">seed =</span> <span class="dv">123</span></span>
<span id="cb27-23"><a href="#cb27-23" aria-hidden="true" tabindex="-1"></a>)</span>
<span id="cb27-24"><a href="#cb27-24" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb27-25"><a href="#cb27-25" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb27-26"><a href="#cb27-26" aria-hidden="true" tabindex="-1"></a><span class="fu">set.seed</span>(<span class="dv">123</span>)  <span class="co"># for reproducibility</span></span>
<span id="cb27-27"><a href="#cb27-27" aria-hidden="true" tabindex="-1"></a>train<span class="sc">$</span>user <span class="ot">&lt;-</span> <span class="fu">as.numeric</span>(train<span class="sc">$</span>user)<span class="sc">-</span><span class="dv">1</span></span>
<span id="cb27-28"><a href="#cb27-28" aria-hidden="true" tabindex="-1"></a>gbm_model <span class="ot">&lt;-</span> <span class="fu">gbm</span>(</span>
<span id="cb27-29"><a href="#cb27-29" aria-hidden="true" tabindex="-1"></a>  <span class="at">formula =</span> user <span class="sc">~</span> .,</span>
<span id="cb27-30"><a href="#cb27-30" aria-hidden="true" tabindex="-1"></a>  <span class="at">data =</span> train,</span>
<span id="cb27-31"><a href="#cb27-31" aria-hidden="true" tabindex="-1"></a>  <span class="at">distribution =</span> <span class="st">&quot;gaussian&quot;</span>,  <span class="co"># SSE loss function</span></span>
<span id="cb27-32"><a href="#cb27-32" aria-hidden="true" tabindex="-1"></a>  <span class="at">n.trees =</span> <span class="dv">1000</span>,</span>
<span id="cb27-33"><a href="#cb27-33" aria-hidden="true" tabindex="-1"></a>  <span class="at">shrinkage =</span> <span class="fl">0.05</span>,</span>
<span id="cb27-34"><a href="#cb27-34" aria-hidden="true" tabindex="-1"></a>  <span class="at">interaction.depth =</span> <span class="dv">5</span>,</span>
<span id="cb27-35"><a href="#cb27-35" aria-hidden="true" tabindex="-1"></a>  <span class="at">n.minobsinnode =</span> <span class="dv">4</span>,</span>
<span id="cb27-36"><a href="#cb27-36" aria-hidden="true" tabindex="-1"></a>  <span class="at">cv.folds =</span> <span class="dv">10</span></span>
<span id="cb27-37"><a href="#cb27-37" aria-hidden="true" tabindex="-1"></a>)</span></code></pre></div>
<p>We also display four variable importance plots to see which variables each model identified as significant.</p>
<div class="sourceCode" id="cb28"><pre class="sourceCode r"><code class="sourceCode r"><span id="cb28-1"><a href="#cb28-1" aria-hidden="true" tabindex="-1"></a><span class="fu">vip</span>(simple_model, <span class="at">num_features =</span> <span class="dv">25</span>) <span class="sc">+</span> </span>
<span id="cb28-2"><a href="#cb28-2" aria-hidden="true" tabindex="-1"></a>  <span class="fu">ggtitle</span>(<span class="st">&#39;Simple Decision Tree - Variable Importance Plot&#39;</span>)</span></code></pre></div>
<p><img src="figure-html/unnamed-chunk-15-1.png" width="672" /></p>
<div class="sourceCode" id="cb29"><pre class="sourceCode r"><code class="sourceCode r"><span id="cb29-1"><a href="#cb29-1" aria-hidden="true" tabindex="-1"></a><span class="fu">vip</span>(bagging_model, <span class="at">num_features =</span> <span class="dv">25</span>) <span class="sc">+</span> </span>
<span id="cb29-2"><a href="#cb29-2" aria-hidden="true" tabindex="-1"></a>  <span class="fu">ggtitle</span>(<span class="st">&#39;Bagging - Variable Importance Plot&#39;</span>)</span></code></pre></div>
<p><img src="figure-html/unnamed-chunk-15-2.png" width="672" /></p>
<div class="sourceCode" id="cb30"><pre class="sourceCode r"><code class="sourceCode r"><span id="cb30-1"><a href="#cb30-1" aria-hidden="true" tabindex="-1"></a><span class="fu">vip</span>(rf_model, <span class="at">num_features =</span> <span class="dv">25</span>) <span class="sc">+</span> </span>
<span id="cb30-2"><a href="#cb30-2" aria-hidden="true" tabindex="-1"></a>  <span class="fu">ggtitle</span>(<span class="st">&#39;Random Forests - Variable Importance Plot&#39;</span>)</span></code></pre></div>
<p><img src="figure-html/unnamed-chunk-15-3.png" width="672" /></p>
<div class="sourceCode" id="cb31"><pre class="sourceCode r"><code class="sourceCode r"><span id="cb31-1"><a href="#cb31-1" aria-hidden="true" tabindex="-1"></a><span class="fu">vip</span>(gbm_model, <span class="at">num_features =</span> <span class="dv">25</span>) <span class="sc">+</span> </span>
<span id="cb31-2"><a href="#cb31-2" aria-hidden="true" tabindex="-1"></a>  <span class="fu">ggtitle</span>(<span class="st">&#39;Gradient Boosting - Variable Importance Plot&#39;</span>)</span></code></pre></div>
<p><img src="figure-html/unnamed-chunk-15-4.png" width="672" /></p>
<p>It seems that the simple decision tree, random forests model, and gradient boosting model placed the most importance on the presence of the word ???kn??? and the other commonly used words. The bagging model, on the other hand places little importance on the presence of these words and instead privileges tweet length, AFINN score, and sentiments. All of the ensemble methods identified tweet length as strongly predictive of the user. All four heavily weighted anticipation sentiments and AFINN scores.</p>
</div>
<div id="vi.-results-and-discussion" class="section level1">
<h1>VI. Results and Discussion</h1>
<p>Now, I produce confusion matrices and show residual sum of squares for all tree-based methods???first evaluating their performance on the training set and then on the test set. Note again that a Tiktok tweet is encoded as 1, and a Facebook tweet is encoded as 0. The code is shown for the first matrix but not for subsequent ones for the sake of elegance.</p>
<div id="training-set-performance" class="section level2">
<h2>Training Set Performance</h2>
<p><strong>Simple Decision Tree - Training Set:</strong></p>
<pre><code>## [1] 1 0
## Levels: 0 1</code></pre>
<pre><code>## Confusion Matrix and Statistics
## 
##           Reference
## Prediction    0    1
##          0 2300  108
##          1  247 2459
##                                           
##                Accuracy : 0.9306          
##                  95% CI : (0.9233, 0.9374)
##     No Information Rate : 0.502           
##     P-Value [Acc &gt; NIR] : &lt; 2.2e-16       
##                                           
##                   Kappa : 0.8611          
##                                           
##  Mcnemar&#39;s Test P-Value : 2.402e-13       
##                                           
##               Precision : 0.9551          
##                  Recall : 0.9030          
##                      F1 : 0.9284          
##              Prevalence : 0.4980          
##          Detection Rate : 0.4497          
##    Detection Prevalence : 0.4709          
##       Balanced Accuracy : 0.9305          
##                                           
##        &#39;Positive&#39; Class : 0               
## </code></pre>
<p><strong>Bagging Method - Training Set:</strong></p>
<pre><code>## Confusion Matrix and Statistics
## 
##           Reference
## Prediction    0    1
##          0 2512    3
##          1   35 2564
##                                           
##                Accuracy : 0.9926          
##                  95% CI : (0.9898, 0.9947)
##     No Information Rate : 0.502           
##     P-Value [Acc &gt; NIR] : &lt; 2.2e-16       
##                                           
##                   Kappa : 0.9851          
##                                           
##  Mcnemar&#39;s Test P-Value : 4.934e-07       
##                                           
##               Precision : 0.9988          
##                  Recall : 0.9863          
##                      F1 : 0.9925          
##              Prevalence : 0.4980          
##          Detection Rate : 0.4912          
##    Detection Prevalence : 0.4918          
##       Balanced Accuracy : 0.9925          
##                                           
##        &#39;Positive&#39; Class : 0               
## </code></pre>
<p><strong>Random Forests Method - Training Set:</strong></p>
<pre><code>## Confusion Matrix and Statistics
## 
##           Reference
## Prediction    0    1
##          0 2504    3
##          1   43 2564
##                                          
##                Accuracy : 0.991          
##                  95% CI : (0.988, 0.9934)
##     No Information Rate : 0.502          
##     P-Value [Acc &gt; NIR] : &lt; 2.2e-16      
##                                          
##                   Kappa : 0.982          
##                                          
##  Mcnemar&#39;s Test P-Value : 8.912e-09      
##                                          
##               Precision : 0.9988         
##                  Recall : 0.9831         
##                      F1 : 0.9909         
##              Prevalence : 0.4980         
##          Detection Rate : 0.4896         
##    Detection Prevalence : 0.4902         
##       Balanced Accuracy : 0.9910         
##                                          
##        &#39;Positive&#39; Class : 0              
## </code></pre>
<p><strong>Gradient Boosting Method - Training Set:</strong></p>
<pre><code>## Confusion Matrix and Statistics
## 
##           Reference
## Prediction    0    1
##          0 2374   55
##          1  173 2512
##                                           
##                Accuracy : 0.9554          
##                  95% CI : (0.9494, 0.9609)
##     No Information Rate : 0.502           
##     P-Value [Acc &gt; NIR] : &lt; 2.2e-16       
##                                           
##                   Kappa : 0.9108          
##                                           
##  Mcnemar&#39;s Test P-Value : 9.297e-15       
##                                           
##               Precision : 0.9774          
##                  Recall : 0.9321          
##                      F1 : 0.9542          
##              Prevalence : 0.4980          
##          Detection Rate : 0.4642          
##    Detection Prevalence : 0.4750          
##       Balanced Accuracy : 0.9553          
##                                           
##        &#39;Positive&#39; Class : 0               
## </code></pre>
<p><strong>Performance Summary and RSS</strong></p>
<table class="table" style="margin-left: auto; margin-right: auto;">
<thead>
<tr>
<th style="text-align:left;">
type
</th>
<th style="text-align:right;">
total_errors
</th>
<th style="text-align:right;">
accuracy
</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left;">
Simple
</td>
<td style="text-align:right;">
355
</td>
<td style="text-align:right;">
0.9305827
</td>
</tr>
<tr>
<td style="text-align:left;">
Bagging
</td>
<td style="text-align:right;">
38
</td>
<td style="text-align:right;">
0.9925694
</td>
</tr>
<tr>
<td style="text-align:left;">
Random Forests
</td>
<td style="text-align:right;">
46
</td>
<td style="text-align:right;">
0.9910051
</td>
</tr>
<tr>
<td style="text-align:left;">
Gradient Boosting
</td>
<td style="text-align:right;">
228
</td>
<td style="text-align:right;">
0.9554165
</td>
</tr>
</tbody>
</table>
<p>The rankings for accuracy on the training set are as follows:</p>
<ol style="list-style-type: decimal">
<li><p>Bagging method</p></li>
<li><p>Random forests</p></li>
<li><p>Gradient boosting method</p></li>
<li><p>Simple decision tree</p></li>
</ol>
<p>The bagging and random forests methods achieved impressive accuracy on the training set, both able to correctly classify more than 99% of the tweets.</p>
<p>We show the residual sum of squares for all four models on the training set below.</p>
<div class="sourceCode" id="cb37"><pre class="sourceCode r"><code class="sourceCode r"><span id="cb37-1"><a href="#cb37-1" aria-hidden="true" tabindex="-1"></a>rss_simple_train <span class="ot">&lt;-</span> <span class="fu">sum</span>((actual_train<span class="sc">-</span>simple_pred_train)<span class="sc">^</span><span class="dv">2</span>)</span>
<span id="cb37-2"><a href="#cb37-2" aria-hidden="true" tabindex="-1"></a>rss_bagging_train <span class="ot">&lt;-</span> <span class="fu">sum</span>((actual_train<span class="sc">-</span>bagging_pred_train)<span class="sc">^</span><span class="dv">2</span>)</span>
<span id="cb37-3"><a href="#cb37-3" aria-hidden="true" tabindex="-1"></a>rss_rf_train <span class="ot">&lt;-</span> <span class="fu">sum</span>((actual_train<span class="sc">-</span>rf_pred_train)<span class="sc">^</span><span class="dv">2</span>)</span>
<span id="cb37-4"><a href="#cb37-4" aria-hidden="true" tabindex="-1"></a>rss_gb_train <span class="ot">&lt;-</span> <span class="fu">sum</span>((actual_train<span class="sc">-</span>gb_pred_train)<span class="sc">^</span><span class="dv">2</span>)</span>
<span id="cb37-5"><a href="#cb37-5" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb37-6"><a href="#cb37-6" aria-hidden="true" tabindex="-1"></a><span class="fu">cat</span>(<span class="fu">paste0</span>(<span class="st">&quot;Residual Sum of Squares on Training Set</span><span class="sc">\n</span><span class="st">&quot;</span>,</span>
<span id="cb37-7"><a href="#cb37-7" aria-hidden="true" tabindex="-1"></a>           <span class="st">&quot;</span><span class="sc">\n</span><span class="st">Simple decision tree: &quot;</span>, <span class="fu">round</span>(rss_simple_train, <span class="dv">2</span>), </span>
<span id="cb37-8"><a href="#cb37-8" aria-hidden="true" tabindex="-1"></a>           <span class="st">&quot;</span><span class="sc">\n</span><span class="st">Bagging model: &quot;</span>, <span class="fu">round</span>(rss_bagging_train, <span class="dv">2</span>), </span>
<span id="cb37-9"><a href="#cb37-9" aria-hidden="true" tabindex="-1"></a>           <span class="st">&quot;</span><span class="sc">\n</span><span class="st">Random forests model: &quot;</span>, <span class="fu">round</span>(rss_rf_train, <span class="dv">2</span>), </span>
<span id="cb37-10"><a href="#cb37-10" aria-hidden="true" tabindex="-1"></a>           <span class="st">&quot;</span><span class="sc">\n</span><span class="st">Gradient boosting model: &quot;</span>, <span class="fu">round</span>(rss_gb_train, <span class="dv">2</span>)))</span></code></pre></div>
<pre><code>## Residual Sum of Squares on Training Set
## 
## Simple decision tree: 299.52
## Bagging model: 56.46
## Random forests model: 46
## Gradient boosting model: 187.74</code></pre>
<p>The random forests method had the lowest RSS, despite the bagging method achieving higher predictive accuracy on the training set. The bagging method performed second best, followed by the gradient boosting method and simple decision tree.</p>
<p>Now, we show confusion matrices for the test set.</p>
</div>
<div id="test-set-performance" class="section level2">
<h2>Test Set Performance</h2>
<p><strong>Simple Decision Tree - Test Set:</strong></p>
<div class="sourceCode" id="cb39"><pre class="sourceCode r"><code class="sourceCode r"><span id="cb39-1"><a href="#cb39-1" aria-hidden="true" tabindex="-1"></a>actual_test <span class="ot">&lt;-</span> test<span class="sc">$</span>user</span>
<span id="cb39-2"><a href="#cb39-2" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb39-3"><a href="#cb39-3" aria-hidden="true" tabindex="-1"></a>simple_pred_test <span class="ot">&lt;-</span> </span>
<span id="cb39-4"><a href="#cb39-4" aria-hidden="true" tabindex="-1"></a>  <span class="fu">predict</span>(simple_model, <span class="at">newdata =</span> test) <span class="sc">%&gt;%</span> </span>
<span id="cb39-5"><a href="#cb39-5" aria-hidden="true" tabindex="-1"></a>  <span class="fu">as_tibble</span>() <span class="sc">%&gt;%</span> </span>
<span id="cb39-6"><a href="#cb39-6" aria-hidden="true" tabindex="-1"></a>  <span class="fu">select</span>(<span class="dv">2</span>) <span class="sc">%&gt;%</span> </span>
<span id="cb39-7"><a href="#cb39-7" aria-hidden="true" tabindex="-1"></a>  <span class="fu">unlist</span>() <span class="sc">%&gt;%</span> </span>
<span id="cb39-8"><a href="#cb39-8" aria-hidden="true" tabindex="-1"></a>  <span class="fu">as.vector</span>()</span>
<span id="cb39-9"><a href="#cb39-9" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb39-10"><a href="#cb39-10" aria-hidden="true" tabindex="-1"></a>simple_test_confusion <span class="ot">&lt;-</span> </span>
<span id="cb39-11"><a href="#cb39-11" aria-hidden="true" tabindex="-1"></a>  <span class="fu">confusionMatrix</span>(<span class="at">data =</span> <span class="fu">factor</span>(<span class="fu">round</span>(simple_pred_test)),</span>
<span id="cb39-12"><a href="#cb39-12" aria-hidden="true" tabindex="-1"></a>                  <span class="at">reference =</span> <span class="fu">factor</span>(actual_test), <span class="at">mode =</span> <span class="st">&quot;prec_recall&quot;</span>)</span>
<span id="cb39-13"><a href="#cb39-13" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb39-14"><a href="#cb39-14" aria-hidden="true" tabindex="-1"></a>simple_test_errors <span class="ot">&lt;-</span> </span>
<span id="cb39-15"><a href="#cb39-15" aria-hidden="true" tabindex="-1"></a>  simple_test_confusion<span class="sc">$</span>table[<span class="dv">2</span>] <span class="sc">+</span></span>
<span id="cb39-16"><a href="#cb39-16" aria-hidden="true" tabindex="-1"></a>  simple_test_confusion<span class="sc">$</span>table[<span class="dv">3</span>]</span>
<span id="cb39-17"><a href="#cb39-17" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb39-18"><a href="#cb39-18" aria-hidden="true" tabindex="-1"></a>simple_test_accuracy <span class="ot">&lt;-</span></span>
<span id="cb39-19"><a href="#cb39-19" aria-hidden="true" tabindex="-1"></a>  <span class="fu">as.numeric</span>(simple_test_confusion<span class="sc">$</span>overall[<span class="dv">1</span>])</span>
<span id="cb39-20"><a href="#cb39-20" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb39-21"><a href="#cb39-21" aria-hidden="true" tabindex="-1"></a>simple_test_confusion</span></code></pre></div>
<pre><code>## Confusion Matrix and Statistics
## 
##           Reference
## Prediction   0   1
##          0 583  23
##          1  68 604
##                                           
##                Accuracy : 0.9288          
##                  95% CI : (0.9133, 0.9423)
##     No Information Rate : 0.5094          
##     P-Value [Acc &gt; NIR] : &lt; 2.2e-16       
##                                           
##                   Kappa : 0.8577          
##                                           
##  Mcnemar&#39;s Test P-Value : 3.979e-06       
##                                           
##               Precision : 0.9620          
##                  Recall : 0.8955          
##                      F1 : 0.9276          
##              Prevalence : 0.5094          
##          Detection Rate : 0.4562          
##    Detection Prevalence : 0.4742          
##       Balanced Accuracy : 0.9294          
##                                           
##        &#39;Positive&#39; Class : 0               
## </code></pre>
<p><strong>Bagging Method - Test Set:</strong></p>
<pre><code>## Confusion Matrix and Statistics
## 
##           Reference
## Prediction   0   1
##          0 603  30
##          1  48 597
##                                           
##                Accuracy : 0.939           
##                  95% CI : (0.9244, 0.9515)
##     No Information Rate : 0.5094          
##     P-Value [Acc &gt; NIR] : &lt; 2e-16         
##                                           
##                   Kappa : 0.878           
##                                           
##  Mcnemar&#39;s Test P-Value : 0.05425         
##                                           
##               Precision : 0.9526          
##                  Recall : 0.9263          
##                      F1 : 0.9393          
##              Prevalence : 0.5094          
##          Detection Rate : 0.4718          
##    Detection Prevalence : 0.4953          
##       Balanced Accuracy : 0.9392          
##                                           
##        &#39;Positive&#39; Class : 0               
## </code></pre>
<p><strong>Random Forests Method - Test Set:</strong></p>
<pre><code>## Confusion Matrix and Statistics
## 
##           Reference
## Prediction   0   1
##          0 600  23
##          1  51 604
##                                           
##                Accuracy : 0.9421          
##                  95% CI : (0.9279, 0.9543)
##     No Information Rate : 0.5094          
##     P-Value [Acc &gt; NIR] : &lt; 2.2e-16       
##                                           
##                   Kappa : 0.8842          
##                                           
##  Mcnemar&#39;s Test P-Value : 0.001697        
##                                           
##               Precision : 0.9631          
##                  Recall : 0.9217          
##                      F1 : 0.9419          
##              Prevalence : 0.5094          
##          Detection Rate : 0.4695          
##    Detection Prevalence : 0.4875          
##       Balanced Accuracy : 0.9425          
##                                           
##        &#39;Positive&#39; Class : 0               
## </code></pre>
<p><strong>Gradient Boosting Method - Test Set:</strong></p>
<pre><code>## Confusion Matrix and Statistics
## 
##           Reference
## Prediction   0   1
##          0 596  22
##          1  55 605
##                                           
##                Accuracy : 0.9397          
##                  95% CI : (0.9253, 0.9522)
##     No Information Rate : 0.5094          
##     P-Value [Acc &gt; NIR] : &lt; 2.2e-16       
##                                           
##                   Kappa : 0.8796          
##                                           
##  Mcnemar&#39;s Test P-Value : 0.0002656       
##                                           
##               Precision : 0.9644          
##                  Recall : 0.9155          
##                      F1 : 0.9393          
##              Prevalence : 0.5094          
##          Detection Rate : 0.4664          
##    Detection Prevalence : 0.4836          
##       Balanced Accuracy : 0.9402          
##                                           
##        &#39;Positive&#39; Class : 0               
## </code></pre>
<p><strong>Performance Summary and RSS</strong></p>
<table class="table" style="margin-left: auto; margin-right: auto;">
<thead>
<tr>
<th style="text-align:left;">
type
</th>
<th style="text-align:right;">
total_errors
</th>
<th style="text-align:right;">
accuracy
</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left;">
Simple
</td>
<td style="text-align:right;">
91
</td>
<td style="text-align:right;">
0.9287950
</td>
</tr>
<tr>
<td style="text-align:left;">
Bagging
</td>
<td style="text-align:right;">
78
</td>
<td style="text-align:right;">
0.9389671
</td>
</tr>
<tr>
<td style="text-align:left;">
Random Forests
</td>
<td style="text-align:right;">
74
</td>
<td style="text-align:right;">
0.9420970
</td>
</tr>
<tr>
<td style="text-align:left;">
Gradient Boosting
</td>
<td style="text-align:right;">
77
</td>
<td style="text-align:right;">
0.9397496
</td>
</tr>
</tbody>
</table>
<p>The rankings for accuracy on the test set are as follows:</p>
<ol style="list-style-type: decimal">
<li><p>Gradient boosting method</p></li>
<li><p>Random forests method</p></li>
<li><p>Bagging method</p></li>
<li><p>Simple decision tree</p></li>
</ol>
<p>It is worth noting though, that the differences in accuracy between the first three is incredibly small, so perhaps the tie may be broken using RSS with respect to the test set:</p>
<div class="sourceCode" id="cb44"><pre class="sourceCode r"><code class="sourceCode r"><span id="cb44-1"><a href="#cb44-1" aria-hidden="true" tabindex="-1"></a>rss_simple_test <span class="ot">&lt;-</span> <span class="fu">sum</span>((actual_test<span class="sc">-</span>simple_pred_test)<span class="sc">^</span><span class="dv">2</span>)</span>
<span id="cb44-2"><a href="#cb44-2" aria-hidden="true" tabindex="-1"></a>rss_bagging_test <span class="ot">&lt;-</span> <span class="fu">sum</span>((actual_test<span class="sc">-</span>bagging_pred_test)<span class="sc">^</span><span class="dv">2</span>)</span>
<span id="cb44-3"><a href="#cb44-3" aria-hidden="true" tabindex="-1"></a>rss_rf_test <span class="ot">&lt;-</span> <span class="fu">sum</span>((actual_test<span class="sc">-</span>rf_pred_test)<span class="sc">^</span><span class="dv">2</span>)</span>
<span id="cb44-4"><a href="#cb44-4" aria-hidden="true" tabindex="-1"></a>rss_gb_test <span class="ot">&lt;-</span> <span class="fu">sum</span>((actual_test<span class="sc">-</span>gb_pred_test)<span class="sc">^</span><span class="dv">2</span>)</span>
<span id="cb44-5"><a href="#cb44-5" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb44-6"><a href="#cb44-6" aria-hidden="true" tabindex="-1"></a><span class="fu">cat</span>(<span class="fu">paste0</span>(<span class="st">&quot;Residual Sum of Squares on Test Set</span><span class="sc">\n</span><span class="st">&quot;</span>,</span>
<span id="cb44-7"><a href="#cb44-7" aria-hidden="true" tabindex="-1"></a>           <span class="st">&quot;</span><span class="sc">\n</span><span class="st">Simple decision tree: &quot;</span>, <span class="fu">round</span>(rss_simple_test, <span class="dv">2</span>), </span>
<span id="cb44-8"><a href="#cb44-8" aria-hidden="true" tabindex="-1"></a>           <span class="st">&quot;</span><span class="sc">\n</span><span class="st">Bagging model: &quot;</span>, <span class="fu">round</span>(rss_bagging_test, <span class="dv">2</span>), </span>
<span id="cb44-9"><a href="#cb44-9" aria-hidden="true" tabindex="-1"></a>           <span class="st">&quot;</span><span class="sc">\n</span><span class="st">Random forests model: &quot;</span>, <span class="fu">round</span>(rss_rf_test, <span class="dv">2</span>), </span>
<span id="cb44-10"><a href="#cb44-10" aria-hidden="true" tabindex="-1"></a>           <span class="st">&quot;</span><span class="sc">\n</span><span class="st">Gradient boosting model: &quot;</span>, <span class="fu">round</span>(rss_gb_test, <span class="dv">2</span>)))</span></code></pre></div>
<pre><code>## Residual Sum of Squares on Test Set
## 
## Simple decision tree: 77.23
## Bagging model: 58.6
## Random forests model: 74
## Gradient boosting model: 60.05</code></pre>
<p>The bagging model had the lowest RSS on the test set even though it was only second best for the training set. The gradient boosting model had the second lowest RSS, followed by random forests and the simple decision tree.</p>
<p>In sum, it seems that the best model would be either the bagging model or the gradient boosting model, but this is nitpicking because all of the ensemble methods performed very well, with accuracy scores above 93%.</p>
</div>
</div>
<div id="vii.-conclusion" class="section level1">
<h1>VII. Conclusion</h1>
<p>Looking at the analyses, it seems that the Facebook and TikTok accounts have systematically different Twitter presences. Facebook seems to respond more frequently to user fears, which are associated with words such as ???secure??? and ???trust.??? Whereas, TikTok focuses on generating excitement and offer prize giveaways, which is associated with ???anticipation??? words such as ???winning??? and ???tomorrow.??? Differences in tweet length also possibly reflect on the preferences of the target audience; TikTok users are younger and less likely to consume written information (it is a video platform, after all), and the opposite is true for Facebook. In sum, our predictive endeavor was successful, and we unveiled a number of useful insights from it.</p>
</div>
<div id="viii.-contributions" class="section level1">
<h1>VIII. Contributions</h1>
<p>As the authorship indicates, four teammates contributed to this analysis: Elaina Lin, Kim Nguyen, Meghan Aines, and Ryan Karbowicz.</p>





</div>

<script>

// add bootstrap table styles to pandoc tables
function bootstrapStylePandocTables() {
  $('tr.odd').parent('tbody').parent('table').addClass('table table-condensed');
}
$(document).ready(function () {
  bootstrapStylePandocTables();
});


</script>

<!-- tabsets -->

<script>
$(document).ready(function () {
  window.buildTabsets("TOC");
});

$(document).ready(function () {
  $('.tabset-dropdown > .nav-tabs > li').click(function () {
    $(this).parent().toggleClass('nav-tabs-open');
  });
});
</script>

<!-- code folding -->


<!-- dynamically load mathjax for compatibility with self-contained -->
<script>
  (function () {
    var script = document.createElement("script");
    script.type = "text/javascript";
    script.src  = "https://mathjax.rstudio.com/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML";
    document.getElementsByTagName("head")[0].appendChild(script);
  })();
</script>


