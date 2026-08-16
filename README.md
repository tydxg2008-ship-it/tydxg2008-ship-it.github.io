# tydxg2008-ship-it.github.io
<!DOCTYPE html>﻿
<html lang="zh-CN">﻿
<head>﻿
<meta charset="UTF-8">﻿
<meta name="viewport" content="width=device-width, initial-scale=1.0">﻿
<title>🎒女生开学智能物品清单</title>﻿
<style>﻿
*{margin:0;padding:0;box-sizing:border-box;font-family:system-ui,-apple-system,sans-serif;}﻿
body{background:#f4f7fb;max-width:760px;margin:0 auto;padding:0 14px 72px;color:#222;}﻿
h1{text-align:center;margin:16px 0;font-size:21px;color:#1e293b;}﻿
h2{font-size:17px;margin-bottom:12px;color:#2d3748;display:flex;align-items:center;gap:6px;}﻿

/*底部导航*/﻿
.bottom-nav{﻿
    position:fixed;﻿
    left:0;right:0;bottom:0;﻿
    background:#ffffff;﻿
    display:flex;﻿
    box-shadow:0 -1px 6px rgba(0,0,0,0.08);﻿
    z-index:99;﻿
}﻿
.nav-item{﻿
    flex:1;﻿
    text-align:center;﻿
    padding:11px 0;﻿
    font-size:14px;﻿
    color:#64748b;﻿
    cursor:pointer;﻿
}﻿
.nav-item.active{﻿
    color:#2563eb;﻿
    font-weight:600;﻿
}﻿

.page{display:none;}﻿
.page.active{display:block;}﻿

/*首页分组：网格多行布局*/﻿
.home-group-grid{﻿
    background:#ffffff;﻿
    border-radius:14px;﻿
    padding:14px;﻿
    margin:14px 0;﻿
    display:grid;﻿
    grid-template-columns:repeat(3,1fr);﻿
    gap:10px;﻿
}﻿
.home-grid-btn{﻿
    text-align:center;﻿
    padding:10px 6px;﻿
    background:#edf2fb;﻿
    border-radius:10px;﻿
    font-size:13px;﻿
    cursor:pointer;﻿
}﻿
.home-grid-btn:active{background:#d7e3fc;}﻿

.group-quick-bar{﻿
    background:#fff;﻿
    border-radius:12px;﻿
    padding:10px;﻿
    margin-bottom:14px;﻿
    display:flex;﻿
    flex-wrap:wrap;﻿
    gap:7px;﻿
}﻿
.group-quick-btn{﻿
    padding:5px 9px;﻿
    background:#edf2fb;﻿
    border-radius:8px;﻿
    font-size:12px;﻿
    cursor:pointer;﻿
}﻿
.group-quick-btn:active{background:#d7e3fc;}﻿

.group-block{﻿
    background:#ffffff;﻿
    border-radius:16px;﻿
    padding:18px;﻿
    margin-bottom:16px;﻿
    box-shadow:0 2px 8px rgba(0,0,0,0.06);﻿
}﻿

.item-card{﻿
    border:1px solid #e8edf4;﻿
    border-radius:12px;﻿
    padding:14px;﻿
    margin-bottom:12px;﻿
    background:#fff;﻿
}﻿
.item-name{﻿
    font-size:15px;﻿
    margin-bottom:10px;﻿
}﻿
.status-row{﻿
    display:flex;﻿
    flex-wrap:wrap;﻿
    gap:14px;﻿
    align-items:center;﻿
    margin-bottom:8px;﻿
}﻿
.cost-row{﻿
    display:flex;﻿
    gap:6px;﻿
    align-items:center;﻿
}﻿
.cost-row label{﻿
    font-size:13px;﻿
    color:#444;﻿
}﻿
.cost-row input{﻿
    width:90px;﻿
    padding:4px 6px;﻿
    border:1px solid #d1d9e6;﻿
    border-radius:6px;﻿
    font-size:13px;﻿
}﻿
.status-option{﻿
    display:flex;﻿
    align-items:center;﻿
    gap:5px;﻿
    cursor:pointer;﻿
    font-size:13px;﻿
}﻿
.circle{﻿
    width:18px;height:18px;﻿
    border:2px solid #b8c2d1;﻿
    border-radius:50%;﻿
    flex-shrink:0;﻿
}﻿
.circle.active{﻿
    background-color:#22c55e;﻿
    border-color:#22c55e;﻿
}﻿
.item-del{﻿
    margin-left:auto;﻿
    color:#ef4444;﻿
    font-size:13px;﻿
    cursor:pointer;﻿
}﻿

.total-box{﻿
    background:#fffbeb;﻿
    border-radius:14px;﻿
    padding:13px 16px;﻿
    margin-bottom:16px;﻿
}﻿
.filter-box{﻿
    background:#fff;﻿
    border-radius:16px;﻿
    padding:16px;﻿
    margin-bottom:16px;﻿
    box-shadow:0 2px 8px rgba(0,0,0,0.06);﻿
}﻿
.filter-row{﻿
    display:flex;﻿
    flex-wrap:wrap;﻿
    gap:12px;﻿
    margin-bottom:12px;﻿
    align-items:center;﻿
}﻿
label{font-size:14px;color:#334155;}﻿
select,input[type="text"],input[type="number"]{﻿
    padding:8px 10px;﻿
    border:1px solid #d1d9e6;﻿
    border-radius:8px;﻿
    font-size:14px;﻿
}﻿
.tip-text{font-size:12px;color:#64748b;margin-top:6px;}﻿

.medicine-block{﻿
    margin-top:16px;﻿
    padding-top:16px;﻿
    border-top:1px solid #e2e8f0;﻿
}﻿
.med-item{﻿
    display:flex;﻿
    align-items:center;﻿
    justify-content:space-between;﻿
    padding:7px 0;﻿
    border-bottom:1px solid #f1f5f9;﻿
}﻿
.med-del{﻿
    color:#dc2626;﻿
    cursor:pointer;﻿
    font-size:13px;﻿
}﻿
.med-input-row{﻿
    display:flex;﻿
    gap:8px;﻿
    margin:10px 0;﻿
}﻿
.med-input-row input{flex:1;}﻿
.btn-small{﻿
    padding:7px 12px;﻿
    border-radius:8px;﻿
    border:none;﻿
    cursor:pointer;﻿
    font-size:13px;﻿
}﻿
.btn-blue{background:#2563eb;color:#ffffff;}﻿
.btn-confirm{background:#16a34a;color:#fff;margin-top:8px;width:100%;padding:10px;font-weight:500;}﻿

.desc-card{﻿
    background:#fff;border-radius:16px;padding:18px;margin:14px 0;﻿
    box-shadow:0 2px 8px rgba(0,0,0,0.06);﻿
}﻿
.desc-card h3{margin-bottom:10px;color:#1e293b;}﻿
.desc-card p{font-size:14px;line-height:1.6;color:#475569;}﻿

.add-new-item-area{﻿
    margin-top:14px;﻿
    display:flex;﻿
    gap:8px;﻿
    flex-wrap:wrap;﻿
}﻿
.add-new-item-area input{flex:minmax(120px,1fr);}﻿

/*校园地图画布区域*/﻿
.map-wrap{﻿
    position:relative;﻿
    width:100%;﻿
    background:#eef2f7;﻿
    border-radius:14px;﻿
    overflow:hidden;﻿
    margin:12px 0;﻿
}﻿
#mapCanvas{﻿
    width:100%;﻿
    display:block;﻿
}﻿
.map-input-row{﻿
    display:flex;﻿
    gap:8px;﻿
    flex-wrap:wrap;﻿
    margin:10px 0;﻿
}﻿
.map-input-row input{flex:1;}﻿
</style>﻿
</head>﻿
<body>﻿

<div id="page-home" class="page active">﻿
    <h1>🎒女生开学智能清单</h1>﻿
    <div class="desc-card">﻿
        <h3>📌使用说明</h3>﻿
        <p>1、前往【匹配设置】填写信息，点【确定】自动删减不需要物品<br>﻿
2、首页网格按钮跳转清单分组；每件物品独立卡片，点圆圈切换状态，下方输入框填写单品花费<br>﻿
3、地图页：上传学校地图，填校门、宿舍楼，自动绘制虚线箭头路线<br>﻿
4、全部本地存档，清除缓存数据丢失</p>﻿
    </div>﻿
    <div class="home-group-grid">﻿
        <div class="home-grid-btn" data-target="g1">📑证件资料</div>﻿
        <div class="home-grid-btn" data-target="g2">📱数码电子</div>﻿
        <div class="home-grid-btn" data-target="g3">🛏床上用品</div>﻿
        <div class="home-grid-btn" data-target="g4">🧴洗护女生</div>﻿
        <div class="home-grid-btn" data-target="g5">👔衣物穿搭</div>﻿
        <div class="home-grid-btn" data-target="g6">📖学习文具</div>﻿
        <div class="home-grid-btn" data-target="g7">🏠宿舍日用</div>﻿
        <div class="home-grid-btn" data-target="g8">💊医药防护</div>﻿
        <div class="home-grid-btn" data-target="g9">☀️军训物资</div>﻿
        <div class="home-grid-btn" data-target="g10">✨其他零碎</div>﻿
    </div>﻿
</div>﻿

<!--匹配设置页面-->﻿
<div id="page-setting" class="page">﻿
    <h1>⚙️个人情况匹配</h1>﻿
    <div class="filter-box">﻿
        <div class="filter-row">﻿
            <label>就读地域：</label>﻿
            <select id="area">﻿
                <option value="in">省内（少带行李）</option>﻿
                <option value="out">省外（全套自备）</option>﻿
            </select>﻿
            <label>学历层次：</label>﻿
            <select id="degree">﻿
                <option value="college">专科</option>﻿
                <option value="under">本科</option>﻿
                <option value="post">研究生/博士</option>﻿
            </select>﻿
        </div>﻿
        <div class="filter-row">﻿
            <label>是否军训：</label>﻿
            <select id="military">﻿
                <option value="no">不需要军训</option>﻿
                <option value="yes">需要军训</option>﻿
            </select>﻿
            <label>是否团员：</label>﻿
            <select id="isLeague">﻿
                <option value="yes">是团员</option>﻿
                <option value="no">不是团员</option>﻿
            </select>﻿
        </div>﻿
        <button id="applySettingBtn" class="btn-small btn-confirm">✅确定，自动整理清单（删除不需要物品）</button>﻿

        <div class="medicine-block">﻿
            <label>你的身体情况/病症：</label>﻿
            <div class="med-input-row">﻿
                <input id="illnessInput" placeholder="输入病症，例如：偏头痛、鼻炎">﻿
                <button class="btn-small btn-blue" id="genMedBtn">生成对应药品</button>﻿
            </div>﻿
            <div class="med-input-row">﻿
                <input id="customMedInput" placeholder="手动新增药品">﻿
                <button class="btn-small btn-blue" id="addMedBtn">添加</button>﻿
            </div>﻿
            <div style="margin-top:10px;">﻿
                <p style="font-size:13px;color:#444;margin-bottom:6px;">待加入药物分组列表：</p>﻿
                <div id="medListWrap"></div>﻿
            </div>﻿
            <div class="med-input-row">﻿
                <button class="btn-small btn-blue" id="confirmMedBtn">✅确认全部加入医药分组</button>﻿
            </div>﻿
            <p class="tip-text">⚠️仅作为开学清单参考，不能替代医嘱，用药请遵医嘱</p>﻿
        </div>﻿
    </div>﻿
</div>﻿

<!--校园地图路线页面-->﻿
<div id="page-map" class="page">﻿
    <h1>🗺学校入校路线图</h1>﻿
    <div class="desc-card">﻿
        <p>1.上传学校地图图片<br>﻿
2.输入进门位置、宿舍楼栋位置，画布点击两点<br>﻿
3.自动绘制<strong>虚线+箭头</strong>入校路线</p>﻿
    </div>﻿
    <input type="file" id="mapFileInput" accept="image/*">﻿
    <div class="map-wrap">﻿
        <canvas id="mapCanvas"></canvas>﻿
    </div>﻿
    <div class="map-input-row">﻿
        <input id="gateName" placeholder="从哪个门进入，例：南门">﻿
        <input id="dormName" placeholder="你的宿舍楼，例：3栋">﻿
    </div>﻿
    <p class="tip-text">点击画布：第1次=校门点；第2次=宿舍楼点，自动生成虚线箭头路线</p>﻿
    <button id="clearMapBtn" class="btn-small btn-blue">清除路线重画</button>﻿
</div>﻿

<div id="page-list" class="page">﻿
    <h1>📋完整物品清单</h1>﻿
    <div class="total-box">﻿
        <div>预估总花费：<span id="totalMoney">0.00</span> 元</div>﻿
        <div style="font-size:13px;color:#666;margin-top:4px;">状态圆圈点击切换：未买｜已买｜已寄到校｜已收拾行李箱，物品下方填写单品价格</div>﻿
    </div>﻿
    <div class="group-quick-bar">﻿
        <div class="group-quick-btn" data-target="g1">📑证件</div>﻿
        <div class="group-quick-btn" data-target="g2">📱数码</div>﻿
        <div class="group-quick-btn" data-target="g3">🛏床品</div>﻿
        <div class="group-quick-btn" data-target="g4">🧴洗护</div>﻿
        <div class="group-quick-btn" data-target="g5">👔衣物</div>﻿
        <div class="group-quick-btn" data-target="g6">📖文具</div>﻿
        <div class="group-quick-btn" data-target="g7">🏠日用</div>﻿
        <div class="group-quick-btn" data-target="g8">💊医药</div>﻿
        <div class="group-quick-btn" data-target="g9">☀️军训</div>﻿
        <div class="group-quick-btn" data-target="g10">✨零碎</div>﻿
    </div>﻿

    <div id="g1" class="group-block">﻿
        <h2>📑证件资料</h2>﻿
        <div id="sc1"></div>﻿
    </div>﻿
    <div id="g2" class="group-block">﻿
        <h2>📱数码电子</h2>﻿
        <div id="sc2"></div>﻿
    </div>﻿
    <div id="g3" class="group-block">﻿
        <h2>🛏床上用品</h2>﻿
        <div id="sc3"></div>﻿
    </div>﻿
    <div id="g4" class="group-block">﻿
        <h2>🧴洗护&女生专属</h2>﻿
        <div id="sc4"></div>﻿
    </div>﻿
    <div id="g5" class="group-block">﻿
        <h2>👔衣物穿搭</h2>﻿
        <div id="sc5"></div>﻿
    </div>﻿
    <div id="g6" class="group-block">﻿
        <h2>📖学习文具</h2>﻿
        <div id="sc6"></div>﻿
    </div>﻿
    <div id="g7" class="group-block">﻿
        <h2>🏠宿舍日用小物</h2>﻿
        <div id="sc7"></div>﻿
    </div>﻿
    <div id="g8" class="group-block">﻿
        <h2>💊医药防护</h2>﻿
        <div id="sc8"></div>﻿
    </div>﻿
    <div id="g9" class="group-block">﻿
        <h2>☀️军训专属物资</h2>﻿
        <div id="sc9"></div>﻿
    </div>﻿
    <div id="g10" class="group-block">﻿
        <h2>✨其他零碎</h2>﻿
        <div class="add-new-item-area">﻿
            <input id="addInput" placeholder="新增物品">﻿
            <input id="priceInput" placeholder="单价" type="number" step="0.01">﻿
            <button id="addBtn" class="btn-small btn-blue">新增</button>﻿
        </div>﻿
        <div id="sc10" style="margin-top:14px;"></div>﻿
    </div>﻿
</div>﻿

<div id="page-mine" class="page">﻿
    <h1>👤我的</h1>﻿
    <div class="desc-card">﻿
        <h3>数据管理</h3>﻿
        <p>清单+设置全部保存在浏览器本地<br>清除浏览器缓存会丢失全部数据，请留意备份</p>﻿
        <button id="resetAll" style="margin-top:12px;padding:8px 12px;border-radius:6px;border:1px solid #f87171;background:#fff;color:#dc2626;cursor:pointer;">重置全部数据</button>﻿
    </div>﻿
</div>﻿

<div class="bottom-nav">﻿
    <div class="nav-item" data-page="page-home">首页</div>﻿
    <div class="nav-item" data-page="page-setting">匹配设置</div>﻿
    <div class="nav-item" data-page="page-map">校园地图</div>﻿
    <div class="nav-item" data-page="page-list">清单</div>﻿
    <div class="nav-item" data-page="page-mine">我的</div>﻿
</div>﻿

<script>﻿
const key = "smart_girl_dorm_list_v7";﻿
const settingKey = "smart_girl_dorm_setting_v7";﻿

//状态：0未买，1已买，2已寄到校，3已收拾进行李箱﻿
const statusList = [﻿
    {val:0,text:"未买"},﻿
    {val:1,text:"已买"},﻿
    {val:2,text:"已寄到校"},﻿
    {val:3,text:"已收拾行李箱"}﻿
];﻿

const medMap = {﻿
    "感冒":["复方氨酚烷胺片","感冒灵颗粒","退烧药","布洛芬缓释胶囊"],﻿
    "风寒感冒":["风寒感冒颗粒","生姜红糖"],﻿
    "风热感冒":["连花清瘟胶囊","清热解毒口服液"],﻿
    "流感":["奥司他韦(遵医嘱)","退烧止痛片"],﻿
    "发烧":["对乙酰氨基酚","布洛芬"],﻿
    "咳嗽":["川贝枇杷膏","右美沙芬","急支糖浆"],﻿
    "干咳":["右美沙芬片","雪梨膏"],﻿
    "痰多咳嗽":["氨溴索口服溶液","乙酰半胱氨酸"],﻿
    "支气管炎":["止咳化痰药","消炎含片"],﻿
    "扁桃体炎":["蒲地蓝消炎片","润喉含片"],﻿
    "咽喉炎":["西瓜霜含片","咽炎片","金嗓子"],﻿
    "咽喉肿痛":["牛黄解毒片","复方草珊瑚含片"],﻿
    "口腔溃疡":["西瓜霜喷剂","口腔溃疡贴","维生素B2"],﻿
    "口角炎":["维生素B2","红霉素软膏"],﻿
    "牙痛":["布洛芬","甲硝唑(遵医嘱)","牙痛水"],﻿
    "牙龈炎":["甲硝唑含漱液","牛黄解毒片"],﻿
    "鼻炎":["生理盐水洗鼻剂","糠酸莫米松鼻喷雾","氯雷他定"],﻿
    "过敏性鼻炎":["氯雷他定片","西替利嗪","鼻炎喷雾"],﻿
    "鼻窦炎":["鼻渊通窍颗粒","洗鼻盐"],﻿
    "中耳炎":["氧氟沙星滴耳液","消炎止痛药"],﻿
    "耳鸣":["甲钴胺片"],﻿
    "结膜炎":["左氧氟沙星滴眼液","人工泪液"],﻿
    "干眼症":["玻璃酸钠滴眼液","人工泪液"],﻿
    "偏头痛":["布洛芬","对乙酰氨基酚","西比灵"],﻿
    "肠胃炎":["奥美拉唑","蒙脱石散","益生菌"],﻿
    "痛经":["布洛芬缓释胶囊","暖宝宝","痛经贴"]﻿
};﻿

//初始物品﻿
const initData = {﻿
    c1:[﻿
        {name:"身份证原件",tags:"all",status:0,money:0},﻿
        {name:"身份证复印件4份",tags:"all",status:0,money:0},﻿
        {name:"录取通知书",tags:"all",status:0,money:0},﻿
        {name:"一寸证件照纸质版",tags:"all",status:0,money:0},﻿
        {name:"二寸证件照纸质版",tags:"all",status:0,money:0},﻿
        {name:"证件照电子版备份",tags:"all",status:0,money:0},﻿
        {name:"团员档案袋",tags:"league‑yes",status:0,money:0},﻿
        {name:"团关系转接材料",tags:"league‑yes",status:0,money:0},﻿
        {name:"银行卡",tags:"all",status:0,money:0},﻿
        {name:"少量现金",tags:"all",status:0,money:0},﻿
        {name:"成绩单",tags:"post",status:0,money:0},﻿
        {name:"学历证明",tags:"post",status:0,money:0}﻿
    ],﻿
    c2:[﻿
        {name:"手机",tags:"all",status:0,money:0},﻿
        {name:"手机充电器",tags:"all",status:0,money:0},﻿
        {name:"数据线",tags:"all",status:0,money:0},﻿
        {name:"充电宝",tags:"all",status:0,money:0},﻿
        {name:"耳机",tags:"all",status:0,money:0},﻿
        {name:"合规插排",tags:"all",status:0,money:0},﻿
        {name:"宿舍台灯",tags:"all",status:0,money:0},﻿
        {name:"笔记本电脑",tags:"under,post",status:0,money:0},﻿
        {name:"U盘",tags:"post",status:0,money:0},﻿
        {name:"移动硬盘",tags:"post",status:0,money:0}﻿
    ],﻿
    c3:[﻿
        {name:"床垫",tags:"area‑out",status:0,money:0},﻿
        {name:"床帘",tags:"area‑out",status:0,money:0},﻿
        {name:"蚊帐",tags:"area‑out",status:0,money:0},﻿
        {name:"被套",tags:"area‑out",status:0,money:0},﻿
        {name:"床单",tags:"area‑out",status:0,money:0},﻿
        {name:"枕套",tags:"area‑out",status:0,money:0},﻿
        {name:"四季被子",tags:"area‑out",status:0,money:0},﻿
        {name:"枕头",tags:"area‑out",status:0,money:0},﻿
        {name:"薄被",tags:"area‑in",status:0,money:0}﻿
    ],﻿
    c4:[﻿
        {name:"牙刷",tags:"all",status:0,money:0},﻿
        {name:"牙膏",tags:"all",status:0,money:0},﻿
        {name:"漱口杯",tags:"all",status:0,money:0},﻿
        {name:"洗面奶",tags:"all,girl",status:0,money:0},﻿
        {name:"爽肤水",tags:"all,girl",status:0,money:0},﻿
        {name:"乳液面霜",tags:"all,girl",status:0,money:0},﻿
        {name:"洗发水",tags:"all,girl",status:0,money:0},﻿
        {name:"护发素",tags:"all,girl",status:0,money:0},﻿
        {name:"沐浴露",tags:"all,girl",status:0,money:0},﻿
        {name:"身体乳",tags:"all,girl",status:0,money:0},﻿
        {name:"洗脸毛巾",tags:"all,girl",status:0,money:0},﻿
        {name:"洗澡毛巾",tags:"all,girl",status:0,money:0},﻿
        {name:"干发帽",tags:"all,girl",status:0,money:0},﻿
        {name:"洗衣液",tags:"all",status:0,money:0},﻿
        {name:"化妆品全套",tags:"girl",status:0,money:0},﻿
        {name:"卸妆油",tags:"girl",status:0,money:0},﻿
        {name:"化妆棉",tags:"girl",status:0,money:0},﻿
        {name:"棉签",tags:"girl",status:0,money:0},﻿
        {name:"梳子",tags:"girl",status:0,money:0},﻿
        {name:"发圈",tags:"girl",status:0,money:0},﻿
        {name:"发夹",tags:"girl",status:0,money:0},﻿
        {name:"卫生巾",tags:"girl",status:0,money:0},﻿
        {name:"护垫",tags:"girl",status:0,money:0},﻿
        {name:"安睡裤",tags:"girl",status:0,money:0}﻿
    ],﻿
    c5:[﻿
        {name:"秋季上衣",tags:"area‑out",status:0,money:0},﻿
        {name:"冬季厚外套",tags:"area‑out",status:0,money:0},﻿
        {name:"当季上衣",tags:"area‑in",status:0,money:0},﻿
        {name:"当季裤子",tags:"area‑in",status:0,money:0},﻿
        {name:"内衣",tags:"all",status:0,money:0},﻿
        {name:"袜子",tags:"all",status:0,money:0},﻿
        {name:"睡衣一套",tags:"all",status:0,money:0},﻿
        {name:"居家拖鞋",tags:"all",status:0,money:0},﻿
        {name:"洗澡拖鞋",tags:"all",status:0,money:0},﻿
        {name:"衣架",tags:"all,girl",status:0,money:0},﻿
        {name:"脏衣袋",tags:"all",status:0,money:0}﻿
    ],﻿
    c6:[﻿
        {name:"中性笔",tags:"all",status:0,money:0},﻿
        {name:"笔记本",tags:"all",status:0,money:0},﻿
        {name:"文件袋",tags:"all",status:0,money:0}﻿
    ],﻿
    c7:[﻿
        {name:"抽纸",tags:"all",status:0,money:0},﻿
        {name:"湿巾",tags:"all",status:0,money:0},﻿
        {name:"垃圾袋",tags:"all",status:0,money:0},﻿
        {name:"柜子小锁",tags:"all",status:0,money:0},﻿
        {name:"粘钩",tags:"all",status:0,money:0},﻿
        {name:"剪刀",tags:"all",status:0,money:0},﻿
        {name:"水杯",tags:"all",status:0,money:0}﻿
    ],﻿
    c8:[﻿
        {name:"创可贴",tags:"all",status:0,money:0},﻿
        {name:"碘伏棉签",tags:"all",status:0,money:0},﻿
        {name:"普通感冒药",tags:"all",status:0,money:0},﻿
        {name:"肠胃药",tags:"all",status:0,money:0},﻿
        {name:"驱蚊花露水",tags:"all",status:0,money:0},﻿
        {name:"痛经药",tags:"girl",status:0,money:0},﻿
        {name:"暖宝宝",tags:"girl",status:0,money:0}﻿
    ],﻿
    c9:[﻿
        {name:"SPF50+防晒霜",tags:"military",status:0,money:0},﻿
        {name:"军训加厚鞋垫",tags:"military",status:0,money:0},﻿
        {name:"大容量水杯",tags:"military",status:0,money:0},﻿
        {name:"冰凉贴",tags:"military",status:0,money:0}﻿
    ],﻿
    c10:[﻿
        {name:"雨伞",tags:"all",status:0,money:0},﻿
        {name:"随身小背包",tags:"all",status:0,money:0}﻿
    ]﻿
};﻿

const defaultSetting = {﻿
    area:"in",﻿
    degree:"college",﻿
    military:"no",﻿
    isLeague:"yes"﻿
};﻿

let tempMedList = [];﻿

function loadData(){﻿
    const s = localStorage.getItem(key);﻿
    return s ? JSON.parse(s) : JSON.parse(JSON.stringify(initData));﻿
}﻿
let data = loadData();﻿

function loadSetting(){﻿
    const s = localStorage.getItem(settingKey);﻿
    return s ? JSON.parse(s) : {...defaultSetting};﻿
}﻿
let appSetting = loadSetting();﻿

function saveData(){localStorage.setItem(key,JSON.stringify(data));}﻿
function saveSetting(){localStorage.setItem(settingKey,JSON.stringify(appSetting));}﻿

const domArea = document.getElementById("area");﻿
const domDegree = document.getElementById("degree");﻿
const domMilitary = document.getElementById("military");﻿
const domIsLeague = document.getElementById("isLeague");﻿

function fillSettingUI(){﻿
    domArea.value = appSetting.area;﻿
    domDegree.value = appSetting.degree;﻿
    domMilitary.value = appSetting.military;﻿
    domIsLeague.value = appSetting.isLeague;﻿
}﻿

//【确定按钮逻辑】点击才执行过滤，删除不需要的物品﻿
document.getElementById("applySettingBtn").onclick = function(){﻿
    appSetting.area = domArea.value;﻿
    appSetting.degree = domDegree.value;﻿
    appSetting.military = domMilitary.value;﻿
    appSetting.isLeague = domIsLeague.value;﻿
    saveSetting();﻿

    const raw = JSON.parse(JSON.stringify(initData));﻿
    for(let groupKey in raw){﻿
        const keepList = [];﻿
        raw[groupKey].forEach(item=>{﻿
            const tags = item.tags.split(",");﻿
            let keep = false;﻿
            if(tags.includes("all")) keep=true;﻿
            if(tags.includes("area‑in")&&appSetting.area==="in") keep=true;﻿
            if(tags.includes("area‑out")&&appSetting.area==="out") keep=true;﻿
            if(tags.includes(appSetting.degree)) keep=true;﻿
            if(tags.includes("military")&&appSetting.military==="yes") keep=true;﻿
            if(tags.includes("league‑yes")&&appSetting.isLeague==="yes") keep=true;﻿
            if(tags.includes("girl")) keep=true;﻿
            if(keep) keepList.push(item);﻿
        })﻿
        raw[groupKey] = keepList;﻿
    }﻿
    data = raw;﻿
    saveData();﻿
    renderAll();﻿
    alert("✅清单已自动整理，不需要物品已移除！");﻿
}﻿

function renderMedList(){﻿
    const wrap = document.getElementById("medListWrap");﻿
    wrap.innerHTML="";﻿
    tempMedList.forEach((medName,idx)=>{﻿
        const div = document.createElement("div");﻿
        div.className="med-item";﻿
        div.innerHTML = `<span>${medName}</span><span class="med-del">删除</span>`;﻿
        wrap.appendChild(div);﻿
        div.querySelector(".med-del").onclick=()=>{﻿
            tempMedList.splice(idx,1);﻿
            renderMedList();﻿
        }﻿
    })﻿
}﻿

document.getElementById("genMedBtn").onclick=function(){﻿
    const inputText = document.getElementById("illnessInput").value.trim();﻿
    if(!inputText)return;﻿
    let added = new Set(tempMedList);﻿
    for(let keyword in medMap){﻿
        if(inputText.includes(keyword)){﻿
            medMap[keyword].forEach(medName=>{﻿
                if(!added.has(medName)){﻿
                    tempMedList.push(medName);﻿
                    added.add(medName);﻿
                }﻿
            })﻿
        }﻿
    }﻿
    renderMedList();﻿
}﻿

document.getElementById("addMedBtn").onclick=function(){﻿
    const medName = document.getElementById("customMedInput").value.trim();﻿
    if(!medName)return;﻿
    if(!tempMedList.includes(medName)) tempMedList.push(medName);﻿
    document.getElementById("customMedInput").value="";﻿
    renderMedList();﻿
}﻿

document.getElementById("confirmMedBtn").onclick = function(){﻿
    tempMedList.forEach(name=>{﻿
        const exist = data.c8.some(x=>x.name === name);﻿
        if(!exist){﻿
            data.c8.push({name:name,tags:"customMed",status:0,money:0});﻿
        }﻿
    });﻿
    tempMedList.length = 0;﻿
    saveData();﻿
    renderMedList();﻿
    renderMedList();﻿
}﻿

//底部导航切换﻿
const navItems = document.querySelectorAll(".nav-item");﻿
const pages = document.querySelectorAll(".page");﻿
navItems.forEach(item=>{﻿
    item.onclick = function(){﻿
        const targetId = this.dataset.page;﻿
        navItems.forEach(n=>n.classList.remove("active"));﻿
        this.classList.add("active");﻿
        pages.forEach(p=>p.classList.remove("active"));﻿
        document.getElementById(targetId).classList.add("active");﻿
        if(targetId==="page-setting"){﻿
            fillSettingUI();﻿
            renderMedList();﻿
        }﻿
    }﻿
})﻿

document.querySelectorAll(".home-grid-btn").forEach(btn=>{﻿
    btn.onclick=function(){﻿
        const targetId = this.dataset.target;﻿
        navItems.forEach(n=>n.classList.remove("active"));﻿
        document.querySelector('[data-page="page-list"]').classList.add("active");﻿
        pages.forEach(p=>p.classList.remove("active"));﻿
        document.getElementById("page-list").classList.add("active");﻿
        setTimeout(()=>{﻿
            const el = document.getElementById(targetId);﻿
            if(el) el.scrollIntoView({behavior:"smooth",block:"start"});﻿
        },80);﻿
    }﻿
})﻿

document.querySelectorAll(".group-quick-btn").forEach(btn=>{﻿
    btn.onclick=function(){﻿
        const targetId = this.dataset.target;﻿
        const el = document.getElementById(targetId);﻿
        if(el) el.scrollIntoView({behavior:"smooth",block:"start"});﻿
    }﻿
})﻿

document.getElementById("resetAll").onclick = function(){﻿
    if(confirm("确定重置全部清单与设置？不可恢复！")){﻿
        localStorage.removeItem(key);﻿
        localStorage.removeItem(settingKey);﻿
        data = JSON.parse(JSON.stringify(initData));﻿
        appSetting = {...defaultSetting};﻿
        tempMedList.length=0;﻿
        saveData();saveSetting();﻿
        fillSettingUI();﻿
        renderAll();﻿
        renderMedList();﻿
    }﻿
}﻿

function calcTotal(){﻿
    let sum=0;﻿
    for(let k in data){﻿
        data[k].forEach(it=>sum += Number(it.money||0));﻿
    }﻿
    document.getElementById("totalMoney").innerText = sum.toFixed(2);﻿
}﻿

function renderItem(containerId,arrKey){﻿
    const dom = document.getElementById(containerId);﻿
    dom.innerHTML = "";﻿
    data[arrKey].forEach((item,index)=>{﻿
        const card = document.createElement("div");﻿
        card.className = "item-card";﻿
        let htmlStatus = "";﻿
        statusList.forEach(s=>{﻿
            htmlStatus += `﻿
            <div class="status-option" data-val="${s.val}">﻿
                <div class="circle ${item.status===s.val?'active':''}"></div>﻿
                <span>${s.text}</span>﻿
            </div>﻿
            `﻿
        })﻿
        card.innerHTML = `﻿
            <div style="display:flex;justify-content:space-between;align-items:flex-start;">﻿
                <div class="item-name">${item.name}</div>﻿
                <div class="item-del">删除</div>﻿
            </div>﻿
            <div class="status-row">${htmlStatus}</div>﻿
            <div class="cost-row">﻿
                <label>单价：</label>﻿
                <input type="number" step="0.01" class="cost-input" value="${Number(item.money).toFixed(2)}">﻿
                <span>元</span>﻿
            </div>﻿
        `;﻿
        dom.appendChild(card);﻿

        //状态切换﻿
        card.querySelectorAll(".status-option").forEach(opt=>{﻿
            opt.onclick = function(){﻿
                item.status = Number(this.dataset.val);﻿
                saveData();﻿
                renderAll();﻿
            }﻿
        })﻿

        //花费输入框，回车、失焦保存﻿
        const costInput = card.querySelector(".cost-input");﻿
        const saveCost = ()=>{﻿
            const val = parseFloat(costInput.value)||0;﻿
            item.money = val;﻿
            saveData();﻿
            calcTotal();﻿
        };﻿
        costInput.addEventListener("blur", saveCost);﻿
        costInput.addEventListener("keydown",e=>{﻿
            if(e.key === "Enter"){﻿
                saveCost();﻿
                costInput.blur();﻿
            }﻿
        });﻿

        //删除物品﻿
        card.querySelector(".item-del").onclick = function(){﻿
            data[arrKey].splice(index,1);﻿
            saveData();﻿
            renderAll();﻿
        }﻿
    })﻿
}﻿

function renderAll(){﻿
    renderItem("sc1","c1");﻿
    renderItem("sc2","c2");﻿
    renderItem("sc3","c3");﻿
    renderItem("sc4","c4");﻿
    renderItem("sc5","c5");﻿
    renderItem("sc6","c6");﻿
    renderItem("sc7","c7");﻿
    renderItem("sc8","c8");﻿
    renderItem("sc9","c9");﻿
    renderItem("sc10","c10");﻿
    calcTotal();﻿
}﻿

const inputName = document.getElementById("addInput");﻿
const inputPrice = document.getElementById("priceInput");﻿
const btnAdd = document.getElementById("addBtn");﻿
function addNew(){﻿
    const name = inputName.value.trim();﻿
    const price = parseFloat(inputPrice.value)||0;﻿
    if(!name)return;﻿
    data.c10.push({name:name,tags:"all,girl",status:0,money:price});﻿
    inputName.value="";inputPrice.value="";﻿
    saveData();renderAll();﻿
}﻿
btnAdd.onclick = addNew;﻿
[inputName,inputPrice].forEach(el=>el.addEventListener("keydown",e=>e.key==="Enter"&&addNew()));﻿

// ========== 校园地图画布逻辑 虚线+箭头路线 ==========﻿
const canvas = document.getElementById("mapCanvas");﻿
const ctx = canvas.getContext("2d");﻿
let mapImage = null;﻿
let clickPoints = [];﻿

function resizeCanvas(){﻿
    const wrap = document.querySelector(".map-wrap");﻿
    canvas.width = wrap.clientWidth;﻿
    if(mapImage){﻿
        const imgW = mapImage.width;﻿
        const imgH = mapImage.height;﻿
        const scale = canvas.width / imgW;﻿
        canvas.height = imgH * scale;﻿
    }else{﻿
        canvas.height = 260;﻿
    }﻿
    redrawMap();﻿
}﻿

function redrawMap(){﻿
    ctx.clearRect(0,0,canvas.width,canvas.height);﻿
    if(mapImage){﻿
        const scale = canvas.width / mapImage.width;﻿
        ctx.drawImage(mapImage,0,0,mapImage.width*scale,mapImage.height*scale);﻿
    }﻿
    if(clickPoints.length>=1){﻿
        ctx.fillStyle="#2563eb";﻿
        ctx.beginPath();﻿
        ctx.arc(clickPoints[0].x, clickPoints[0].y,6,0,Math.PI*2);﻿
        ctx.fill();﻿
        ctx.fillText(document.getElementById("gateName").value||"校门",clickPoints[0].x+8,clickPoints[0].y);﻿
    }﻿
    if(clickPoints.length>=2){﻿
        ctx.fillStyle="#dc2626";﻿
        ctx.beginPath();﻿
        ctx.arc(clickPoints[1].x, clickPoints[1].y,6,0,Math.PI*2);﻿
        ctx.fill();﻿
        ctx.fillText(document.getElementById("dormName").value||"宿舍楼",clickPoints[1].x+8,clickPoints[1].y);﻿
        //绘制虚线﻿
        ctx.strokeStyle="#222";﻿
        ctx.setLineDash([8,4]);﻿
        ctx.lineWidth=2;﻿
        ctx.beginPath();﻿
        ctx.moveTo(clickPoints[0].x,clickPoints[0].y);﻿
        ctx.lineTo(clickPoints[1].x,clickPoints[1].y);﻿
        ctx.stroke();﻿
        ctx.setLineDash([]);﻿
        //绘制箭头﻿
        drawArrowHead(clickPoints[0].x,clickPoints[0].y,clickPoints[1].x,clickPoints[1].y);﻿
    }﻿
}﻿

function drawArrowHead(x1,y1,x2,y2){﻿
    const headLen =12;﻿
    const angle = Math.atan2(y2-y1,x2-x1);﻿
    ctx.beginPath();﻿
    ctx.moveTo(x2,y2);﻿
    ctx.lineTo(x2-headLen*Math.cos(angle-Math.PI/6), y2-headLen*Math.sin(angle-Math.PI/6));﻿
    ctx.moveTo(x2,y2);﻿
    ctx.lineTo(x2-headLen*Math.cos(angle+Math.PI/6), y2-headLen*Math.sin(angle+Math.PI/6));﻿
    ctx.lineWidth=2;﻿
    ctx.stroke();﻿
}﻿

//上传地图图片﻿
document.getElementById("mapFileInput").onchange = function(e){﻿
    const file = e.target.files[0];﻿
    if(!file) return;﻿
    const reader = new FileReader();﻿
    reader.onload = function(ev){﻿
        const img = new Image();﻿
        img.onload = function(){﻿
            mapImage = img;﻿
            clickPoints = [];﻿
            resizeCanvas();﻿
        }﻿
        img.src = ev.target.result;﻿
    }﻿
    reader.readAsDataURL(file);﻿
}﻿

//画布点击取点﻿
canvas.onclick = function(e){﻿
    const rect = canvas.getBoundingClientRect();﻿
    const x = e.clientX - rect.left;﻿
    const y = e.clientY - rect.top;﻿
    if(clickPoints.length<2){﻿
        clickPoints.push({x,y});﻿
    }else{﻿
        clickPoints = [{x,y}];﻿
    }﻿
    redrawMap();﻿
}﻿

document.getElementById("clearMapBtn").onclick = function(){﻿
    clickPoints = [];﻿
    redrawMap();﻿
}﻿

window.addEventListener("resize",resizeCanvas);﻿

fillSettingUI();﻿
renderAll();﻿
renderMedList();﻿
resizeCanvas();﻿
</script>﻿
</body>﻿
</html>