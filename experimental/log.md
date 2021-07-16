#160403
在safari看會是滿版，在ipad看會歪掉
#160404
改字型 不能用ttc檔 記得回到css上層
@font-face {
  font-family: 'jasmine';
  src: url('../fonts/font.ttf');
}
#160404
用fontforge改字型成功啦
#160404
one page scroll好像不錯
http://www.thepetedesign.com/demos/onepage_scroll_demo.html
http://alvarotrigo.com/fullPage/
http://www.cssdesignawards.com/articles/15-excellent-jquery-plugins-to-spice-up-your-sites/44/
#160406
可以捲回最上方的按鈕jquery.backTop.min.js及backTop.css
#160422
放圖片 用透明背景好
把<link href="css/bootstrap.min.css" rel="stylesheet">換成<link href="css/bootstrap.css" rel="stylesheet">因為圖片無法對齊下面的問題要從bootstrap.css改，以後再重新編譯

加了pull-down js讓圖片可對齊下方==>用手機根本悲劇
<script type="text/javascript">
//for each element that is classed as 'pull-down', set its margin-top to the difference between its own height and the height of its parent
$('.pull-down').each(function() {
  var $this=$(this);
  $this.css('margin-top', $this.parent().height()-$this.height())
});</script>
</body>

#160422-2
新增
img-responsive
img-responsive-tall
img-responsive-short
讓圖片在大螢幕置底(增加上方padding)
用@media (max-width: 978px) {
    .img-responsive{
      padding:0;
      margin:0;
    }
    .img-responsive-tall {
      padding:0;
      margin:0;
    }
    .img-responsive-short {
      padding:0;
      margin:0;
    }
}讓小裝置不會有padding

#160428
新footer
<p class="copyright">版權所有 暖暖心理治療所 © 2016<span style="float:right;">網頁製作 <a href="http://www.wordpress.org/">Guppy Squad</a></span></p>
新增兩張圖片
拿掉<hr class="section-heading-spacer">比較好調整padding
調整padding
治療所介紹那邊調
<div class="col-lg-6 col-sm-6">
<div class="col-lg-5 col-lg-offset-1 col-sm-6">讓圖大一點

#160430
新增公告用alert
<div class="col-lg-12 col-sm-6">
<div class="alert alert-warning fade in">
  <a href="#" class="close" data-dismiss="alert" aria-label="close">&times;</a>
  <strong>公告：</strong> 暖暖心理治療所春節期間暫停營業。
</div>
</div>
詳細資訊可以考慮用modal或Popovers
http://www.w3schools.com/bootstrap/bootstrap_modal.asp
http://www.w3schools.com/bootstrap/bootstrap_popover.asp

/*限制寬度*/
.container{
  max-width:1080px
}

blockquote {
  padding: 0px 0px 0px 30px;
  margin: 20px 0px 20px 0px;
  border-left: 3px solid #eee; }
}

整理&刪除一些多餘css

讓list格式好一點
ul.A{
  letter-spacing: 0.3px;
  margin:10px 0px 0px 0px;
  line-height: 1.5;
  list-style-type: none;
}
ul.B{
  letter-spacing: 0.3px;
  margin:10px 0 0 5px;
  line-height: 1.6;
  list-style-type: disc;
}
自動更新年份
<script type="text/javascript">
document.write(new Date().getFullYear());
</script>

navbar提早collapse
@media (max-width: 1200px) {
    .navbar-header {
        float: none;
    }
    .navbar-left,.navbar-right {
        float: none !important;
    }
    .navbar-toggle {
        display: block;
    }
    .navbar-collapse {
        border-top: 1px solid transparent;
        box-shadow: inset 0 1px 0 rgba(255,255,255,0.1);
    }
    .navbar-fixed-top {
		top: 0;
		border-width: 0 0 1px;
	}
    .navbar-collapse.collapse {
        display: none!important;
    }
    .navbar-nav {
        float: none!important;
		margin-top: 7.5px;
	}
	.navbar-nav>li {
        float: none;
    }
    .navbar-nav>li>a {
        padding-top: 10px;
        padding-bottom: 10px;
    }
    .collapse.in{
  		display:block !important;
	}
}

#160501
降低了小裝置的navbar高度http://stackoverflow.com/questions/18599778/decreasing-height-of-bootstrap-3-0-navbar
.navbar-nav > li > a, .navbar-brand {
    padding-top:4px !important;
    padding-bottom:0 !important;
    height: 28px;
}
.navbar {min-height:28px !important;}

拿掉小裝置選單底線

把toggle鈕變小http://stackoverflow.com/questions/26831661/bootstrap-3-navbar-toggle-height

padding改成margin
#160508
小裝置圖片上緣margin++
所有圖都畫完啦
寬度限制為900

#160509-1
網域註冊好了
1. 不要用url轉（原始網址會跑出來）及遮罩轉（會嵌在iframe，bootstrap格式會跑掉）
2. 放棄http://tsaihw.github.io/web03，因為DNS只能用host name-->改成tsaihw.github.io
3. 主要的設定竟然是在Github。弄一個CNAME在master branch下 --> Confirm that you have created and committed yourCNAMEfile on GitHub.
https://help.github.com/articles/setting-up-your-pages-site-repository/
4. 改godaddy DNS的A部分https://help.github.com/articles/setting-up-an-apex-domain/#configuring-a-records-with-your-dns-provider
5. Follow your DNS provider's instructions to create two A records that point your custom domain to the following IP addresses:
		* 192.30.252.153
		* 192.30.252.154

#160509-2
告別web03，新增web09，web09的內容更新到tsaihw.github.io
刪除註解刪除多餘檔案
最後優化
文字刪減

#160512
新增問卷及modal
GH無法用php只好用google form
.ss-q-long {
	width:100%;
	height:100px;
}
#160530
    新增favicon(沙發)
#160604
    favicon=蝸牛
#160607
各種favicon
    https://realfavicongenerator.net/
#190803
    網頁改版->網頁最佳化
#191231
    網頁文字增刪+移除留言板
#200117
    新增telegram連結
#200204
    防疫公告
#200512
    改善CSS，刪除外部字型的引用(因Lighthouse SEO的performance竟然零分)
#200916
新增sitemap
#201016
1. Add `rel="noopener"` or `rel="noreferrer"` to any external links to improve performance and prevent security vulnerabilities.
2. third-party scripts-->未修改
3. Specifying a doctype prevents the browser from switching to quirks-mode.-->加入<!DOCTYPE html>
4. <meta name="description">沒寫
#201028
1. rel="noopener"的修改
2. <html lang="zh-Hant-TW">
#210214
1. 遷移到gandi
將godaddy的DNS改為gandi的，但網站就連不上..
2. SSL憑證花一晚申請成功，沒想到轉址就送一個免費的，不過似乎用轉址(forwarding)不ok，github網址會顯示在瀏覽器。
3. 嘗試改DNS record(在gandi設定)似乎便成功轉址。另外github也重新填入Custom domain為nuan-nuan.co，另外開啟了github提供的https(Enforce HTTPS選項)，網站就變成https!（SSL憑證白申請了）參考：https://docs.github.com/en/github/working-with-github-pages/managing-a-custom-domain-for-your-github-pages-site
DNS record主要是將nuan-nuan.co指向github主機的ip(需要設定在A類別)，CNAME則是讓www.nuan-nuan.co也轉到github。
@ 10800 IN A 185.199.108.153
@ 10800 IN A 185.199.109.153
@ 10800 IN A 185.199.110.153
@ 10800 IN A 185.199.111.153
www 10800 IN CNAME tsaihw.github.io.

#210711
配色改成白
刪除造成圖片排板問題的<!DOCTYPE html>

#210712 
bootstrap從3.3.6升級到3.4.1(升級到5.0太複雜，暫時擱置)
#210713
jquery 1.11.1升級到3.6.0
#210713
直接從bootstrap5模板重寫網站,使用https://startbootstrap.com/template/small-business
的startbootstrap-small-business-gh-pages模版
sublime text好用~取代brackets

#210715
As of Bootstrap 5 beta, left and right have been replaced by start and end for RTL support. Therefore the margin utilities changed for Bootstrap 5 beta:

    ml-auto => ms-auto (start)
    mr-auto => me-auto (end)

Also note, all uses of left and right have been replaced with start and end in Bootstrap 5...

    ml-* => ms-*
    pl-* => ps-*
    mr-* => me-*
    pr-* => pe-*
    text-left => text-start
    text-right=> text-end
    float-left => float-start
    float-right=> float-end
    border-left => border-start
    border-right=> border-end
    rounded-left => rounded-start
    rounded-right=> rounded-end
    dropleft => dropstart
    dropright=> dropend
    dropdown-menu--left => dropdown-menu--start
    dropdown-menu--right => dropdown-menu--end
    carousel-item-left => carousel-item-start
    carousel-item-right=> carousel-item-end

#210717
Gallery弄半天終於找到解答
https://stackoverflow.com/questions/41794746/col-xs-not-working-in-bootstrap-4
col-xs-* have been dropped in Bootstrap 4 in favor of col-*.
Replace col-xs-12 with col-12 and it will work as expected.
Also note col-xs-offset-{n} were replaced by offset-{n} in v4.


Breakpoint          Class infix     Dimensions
X-Small             None            <576px
Small               sm              ≥576px
Medium              md              ≥768px
Large               lg              ≥992px
Extra large         xl              ≥1200px
Extra extra large   xxl             ≥1400px

#210717
konami

