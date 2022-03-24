<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
    <title>网络地址管理</title>
    <style type="text/css">
        h1 { margin: 5px 10px 15px; border-bottom: 1px dashed #ecede8; font-size: 16px; color: #333; font-weight: normal; height: 30px; line-height: 30px; position: relative; clear: both; }
        body { margin: 0; font-family: "Microsoft Yahei","Tahoma",Arial; font-size: 14px; color: #333; background-color: #fff; }
        ul { list-style-type: none; margin: 0; padding: 0; }
        pre { margin: 0; }
        .head_box { position: relative; background-color: #f3f3f3; box-shadow: 0 2px 4px rgba(0,0,0,0.15),inset 0 -1px 0 0 #fcfcfc; -moz-box-shadow: 0 2px 4px rgba (0,0,0,0.15),inset 0 -1px 0 0 #fcfcfc; -webkit-box-shadow: 0 2px 4px rgba(0,0,0,0.15),inset 0 -1px 0 0 #fcfcfc; border-top: 1px solid #bdbdbd; border-bottom: 1px solid #bdbdbd; }
            .head_box .inner.wrp { width: auto; margin-left: auto; margin-right: auto; }
        .logo { padding-top: 1px; padding-bottom: 1px; font-size: 18px; }
            .logo a { display: block; height: 40px; overflow: hidden; text-decoration: none; }
                .logo a * { float: left; border: none; }
                .logo a span { color: #656565; margin-top: 7px; }
        .body { width: auto; margin-left: auto; margin-right: auto; padding: 1px 0 5px; }
        .main_content { border: 1px solid #bdbdbd; }
        .title { height: 45px; line-height: 45px; padding-left: 10px; background: #F4F5F9; font-size: 16px; }
        .content { display: -webkit-box; min-height: 420px; padding-bottom: 0px; background-color: snow; }
        .left { width: 100px; line-height: 40px; min-height: 200px; border-right: 1px solid #bdbdbd; }
            .left li { padding-left: 10px; cursor: pointer; display: block; }
                .left li:hover { background: cornsilk; }
        .right { -webkit-box-flex: 1; padding: 30px; }
        .footer { text-align: center; color: #516e81; margin: 25px auto 10px; font-size: 12px; height: 30px; line-height: 20px; text-shadow: 0 1px 0 #fff; }
            .footer ul { text-align: center; list-style: none; margin: 0; padding: 0; }
            .footer li { display: inline; }
            .footer a { color: #3a8dc9; margin: 0 5px; text-decoration: none; }
        td, th { padding-left: 20px; }
        td { width: 160px; }
        .markdown-body table { width: auto; margin-left: 0px; margin-right: 0px !important; }
        .markdown-body tbody { border-top: 0px solid #d5dfeb; border-bottom: 0px solid #d5dfeb; background-color: snow; }
        .markdown-body td:first-child, .markdown-body th:first-child { width: 20%; padding-left: 20px; }
        .markdown-body ul, .markdown-body ol { padding-left: 0px; }
        .markdown-body td { border-right: 0px solid #d5dfeb; border-bottom: 0px solid #d5dfeb; padding: 5px; }
        .markdown-body li, .markdown-body li p, .markdown-body dd, .markdown-body dd p { margin-bottom: 0px; }
        #main .download-bar { display: none; }
        footer .owner, .creds { display: none !important; }
    </style>
</head>
<body>
    <div class="head" id="header" style="overflow: hidden;">
        <div class="head_box" style="overflow: hidden;">
            <div class="inner wrp" style="overflow: hidden;">
                <h1 class="logo">
                    <a href="javascript:void(0)" title="网络地址管理">
                        <span style="display: none;" id="systemName"></span><span>网络地址管理&nbsp;|&nbsp;快捷入口</span>
                    </a>
                </h1>
            </div>
        </div>
    </div>
    <div class="body">
        <div class="main_content">
            <div class="title">地址分类</div>
            <div class="content">
                <ul class="left" id="left">
                    <li id="0" onclick="openHtml(0,this)">常用地址</li>
                    <li id="1" onclick="openHtml(1,this)">公司地址</li>
                    <li id="2" onclick="openHtml(2,this)">学习地址</li>
                    <li id="3" onclick="openHtml(3,this)">资料地址</li>
                    <li id="4" onclick="openHtml(4,this)">博客地址</li>
                    <li id="5" onclick="openHtml(5,this)">工作地址</li>
                    <li id="6" onclick="openHtml(6,this)">其他地址</li>
                    <li id="7" onclick="openHtml(7,this)">临时地址</li>
                </ul>
                <table id="showReport" class="right">
                </table>
            </div>
        </div>
    </div>
    <div class="footer">
        <ul class="footer-places">
            <li class="footer-about">
                <a target="_blank" href="http://www.baidu.com/">百度一下</a>
                &nbsp;|&nbsp;
            </li>
            <li class="footer-contactus">
                <a target="_blank" href="http://home.baidu.com/">关于百度</a>
            </li>
        </ul>
        <div style="clear: both"></div>
    </div>
     <script type="text/javascript">
        function openHtml(type, obj) {

            var myul = document.getElementById('left');
            var mylis = myul.getElementsByTagName('li');
            for (var index = 0; index < mylis.length; index++) {
                if (mylis[index].id == obj.id) {
                    mylis[index].style.background = 'cornsilk';
                    mylis[index].onmouseover = null;
                    mylis[index].onmouseout = null;
                }
                else {
                    mylis[index].style.background = 'snow';
                    mylis[index].onmouseover = function () {
                        this.style.background = 'cornsilk';
                    }
                    mylis[index].onmouseout = function () {
                        this.style.background = 'snow';
                    }
                }
            }

            var showReport = "";
            /// 常用地址
            if (type == 0) {
                showReport += getTrHead();
                showReport += getTdHtml('https://www.baidu.com/', '百度搜索');
                showReport += getTdHtml('https://fanyi.baidu.com/translate', '百度翻译');
                showReport += getTdHtml('https://translate.google.cn/', 'Google翻译');
                showReport += getTdHtml('https://pan.baidu.com/', '百度pan');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('https://www.entts.com/', '英语朗读');
                showReport += getTdHtml('http://www.bejson.com/', 'BEJSON');
                showReport += getTdHtml('https://www.json.cn/', 'JSON解析');
                showReport += getTdHtml('http://tool.oschina.net/', '在线工具');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('https://app.xunjiepdf.com/', '迅捷PDF转换');
                showReport += getTdHtml('http://www.wzsky.net/wz/peisefangan.html', '配色宝典');
                showReport += getTdHtml('https://www.iamwawa.cn/', '哇哇工具');
                showReport += getTdHtml('https://www.jq22.com/textDifference', '在线文本对比');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('https://www.chashebao.com/info/chongqing.html', '社保查询(旧)');
                showReport += getTdHtml('http://ggfwpz.ylbzj.cq.gov.cn/hallEnter/#/personLogin', '社保查询');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTrTail();
            }
            /// 公司地址
            else if (type == 1) {
                showReport += getTrHead();
                showReport += getTdHtml('https://wsoa.wicresoft.com/', 'WSOA');
                showReport += getTdHtml('https://dashboard.juhe.cn/home/', '聚合数据');
                showReport += getTdHtml('https://laiye.com', '来也');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTrTail();
            }
            /// 学习地址
            else if (type == 2) {
                showReport += getTrHead();
                showReport += getTdHtml('http://bootstrap-table.wenzhixin.net.cn/zh-cn/documentation/', 'Bootstrap');
                showReport += getTdHtml('http://edu.51cto.com/center/course/lesson/index?id=2376', 'JavaScript');
                showReport += getTdHtml('http://www.runoob.com/angularjs/angularjs-tutorial.html', 'AngularJS');
                showReport += getTdHtml('https://less.bootcss.com/', 'Less');

                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('https://www.runoob.com/', 'runoob');
                showReport += getTdHtml('http://www.runoob.com/html/html-media.html', 'HTML');
                showReport += getTdHtml('https://www.yiibai.com/javafx', 'JavaFX教程™');
                showReport += getTdHtml('https://code.makery.ch/', 'code.makery');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('https://www.layui.com/', 'Layui框架');
                showReport += getTdHtml('https://www.5axxw.com/', '爱学');
                showReport += getTdHtml('https://www.cnblogs.com/zenronphy/p/12387461.html', 'C#高级11版');
                showReport += getTdHtml('http://c.biancheng.net/', 'C语言中文网');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('http://v.dxsbb.com/ruanjian/coreldraw/186/', 'CorelDRAW');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTrTail();
            }
            /// 资料地址
            else if (type == 3) {
                showReport += getTrHead();

                showReport += getTdHtml('http://www.fontawesome.com.cn/faicons/', '图标库Font Awesome');
                showReport += getTdHtml('https://fontawesome.dashgame.com/', 'Font Awesome');
                showReport += getTdHtml('https://www.iconfinder.com/', 'icon图标库');
                showReport += getTdHtml('http://www.iconfont.cn/home/index', 'iconfont');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('https://echarts.apache.org/examples/zh/index.html', 'ECharts Example');
                showReport += getTdHtml('https://my.vmware.com/cn/web/vmware/home', 'VMware');
                showReport += getTdHtml('https://mvnrepository.com/artifact/org.controlsfx/controlsfx', '中央仓库[依赖包]');
                showReport += getTdHtml('https://jingyan.baidu.com/article/0a52e3f4e53ca1bf63ed725c.html', 'lombok插件安装');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('http://www.cssmoban.com/wpthemes/', 'Wordpress主题');
                showReport += getTdHtml('https://www.17sucai.com/', '17素材');
                showReport += getTdHtml('https://www.8a.hk/', '八艾云');
                showReport += getTdHtml('https://www.juzhenyun.org/', '矩阵云');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('https://quizlet.com/zh-cn', 'Quizlet');
                showReport += getTdHtml('http://timor.tech/api/holiday', '免费节假日API');
                showReport += getTdHtml('https://www.liaoxuefeng.com/wiki/896043488029600', 'Git教程');
                showReport += getTdHtml('https://github.com/tiimgreen/github-cheat-sheet/blob/master/README.zh-cn.md', 'GitHub秘籍');

                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('https://docs.microsoft.com/zh-cn/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver15', 'Microsoft(SSMS)');
                showReport += getTdHtml('https://www.jetbrains.com/idea/download/other.html', 'IntelliJ IDEA<br/>Other Versions');
                showReport += getTdHtml('https://passport.csdn.net/loginv3', 'CSDN');
                showReport += getTdHtml('https://blog.csdn.net/u011714378', 'CSDN(U)');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('http://ahkcn.sourceforge.net/docs/AutoHotkey.htm', 'AutoHotkey');
                showReport += getTdHtml('https://www.jq22.com/jquery-info18727', 'gTree部门组织选择插件');
                showReport += getTdHtml('https://ip.ihuan.me/', 'HTTP代理');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTrTail();
            }
            /// 博客地址
            else if (type == 4) {
                showReport += getTrHead();
                showReport += getTdHtml('https://www.cnblogs.com/SanNiuSignal/', 'SanNiuSignal博客园');
                showReport += getTdHtml('https://www.cnblogs.com/superstar/', 'superstar博客园');
                showReport += getTdHtml('https://www.cnblogs.com/lcawen/', 'lcawen博客园');
                showReport += getTdHtml('https://www.imzcy.cn/', 'imzcy博客园');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('https://www.cnblogs.com/xuliangxing/', 'xuliangxing博客园');
                showReport += getTdHtml('https://www.cnblogs.com/zeroone/', 'zeroone博客园');
                showReport += getTdHtml('https://www.cnblogs.com/xiezunxu/', 'xiezunxu博客园');
                showReport += getTdHtml('http://yelog.org/', '叶落阁博客园');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('https://www.cnblogs.com/lcawen/articles/7040005.html', 'OCR识别中文');
                showReport += getTdHtml('https://www.cnblogs.com/zeroone/archive/2013/09/06/3306179.html', '打印机列表');
                showReport += getTdHtml('https://www.cnblogs.com/xiezunxu/articles/8965848.html', 'WPF动画');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('https://www.cnblogs.com/golden83/', 'Golden博客园');
                showReport += getTdHtml('https://golden83.gitee.io/', 'Golden主页');
                showReport += getTrTail();
            }
            /// 工作地址
            else if (type == 5) {
                showReport += getTrHead();
                showReport += getTdHtml('https://www.51job.com/', '前程无忧');
                showReport += getTdHtml('https://www.zhaopin.com/', '智联招聘');
                showReport += getTdHtml('http://zhaopin.baidu.com/jianzhi?', '兼职招聘');
                showReport += getTdHtml('http://cq.ganji.com/qjzwenjuandiaocha/', '重庆赶集');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTrTail();
            }
            /// 其他地址
            else if (type == 6) {
                showReport += getTrHead();
                showReport += getTdHtml('http://www.96096kp.com/ecsite/control/main', '愉客行');
                showReport += getTdHtml('http://www.12306.cn/mormhweb/', '中国铁路');
                showReport += getTdHtml('edge://history/all', 'EDGE历史');
                showReport += getTdHtml('chrome://history/', '谷歌历史');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTrTail();
            }
            /// 临时地址
            else if (type == 7) {
                showReport += getTrHead();
                showReport += getTdHtml('http://10.173.0.136:81/index.php', '禅道');   /// xuweilin/Abc.1234567890
                showReport += getTdHtml('https://mars.deloitte.com.cn/mars-work-space/index', '工作台');
                showReport += getTdHtml('https://appcenterweb.deloitteresources.com/www/index.html#login?isError=true', 'APPCenter');

                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('https://workflowapidev.deloitte.com.cn:4999', 'WeLearn3:4999');   /// /swagger/ui/index
                showReport += getTdHtml('http://10.173.0.139:1111/', 'workflow测试');
                showReport += getTdHtml('http://10.173.0.179:6060/', '勤学测试');   ///  /swagger/ui/index
                showReport += getTdHtml('https://workflowapidev.deloitte.com.cn:9110/user/login', '勤聚测试');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('https://workflowapidev.deloitte.com.cn:5999', 'WeLearn3:5999');
                showReport += getTdHtml('http://10.173.0.139:2222/', 'workflowUAT');
                showReport += getTdHtml('https://deloitteacademydev.deloitte.cn/', '勤学UAT');
                showReport += getTdHtml('', '勤聚UAT(未知)');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('https://welearn2dev.deloitte.com.cn:9200/user/login', 'WeLearn3:9200');
                showReport += getTdHtml('https://workflow.deloitte.com.cn/ ', 'workflow正式');
                showReport += getTdHtml('https://deloitteacademy.deloitte.cn/', '勤学正式');
                showReport += getTdHtml('', '勤聚正式(未知)');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('http://10.173.0.179:8088/welearnadmin/#id=mug919&p=activity_log&g=1', 'WeLearn3.0原型(Admin)');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('https://www.pgyer.com/PbVo ', '勤学ios');
                showReport += getTdHtml('http://10.173.0.179:8088/da/#g=1&p=%E4%BF%AE%E6%94%B9%E8%AE%B0%E5%BD%95', '原型设计');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('http://10.173.0.179:8088/w3/#id=snq2f2&p=home&g=1', 'WeLearn3.0原型(User)');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('https://www.pgyer.com/yLfp ', '勤学android');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTrTail();
            }
            /// 其他
            else {
                showReport += getTrHead();
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTrTail();

                showReport += getTrHead();
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTdHtml('', '&ensp; ');
                showReport += getTrTail();
            }
            document.getElementById('showReport').innerHTML = showReport;
        }

        function getTrHead() {
            return "<tr>";
        }

        function getTrTail() {
            return "</tr>";
        }

        function getTrHtml(url, name) {
            return "<tr><td><a target=\"_blank\" href=\"" + url + "\" title=\"" + name + "\">" + name + "</a></td></tr>";
        }

        function getTdHtml(url, name) {
            return "<td><a target=\"_blank\" href=\"" + url + "\" title=\"" + name + "\">" + name + "</a></td>";
        }
    </script>
</body>
</html>
