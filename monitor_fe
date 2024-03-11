<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Мониторинг</title>
<script src="https://cdn.anychart.com/releases/8.11.1/js/anychart-core.min.js"></script>
    <script src="https://cdn.anychart.com/releases/8.11.1/js/anychart-pie.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
</head>

<body>
<style>
<style>
<style>

	.main-container {
		width: 1176px;
	}
	
	.main-container, .main-nav {
		margin: 15px 0;
		color: #525456;
		font-size: 16px;
		background: white;
		padding: 30px;
	}

	.main-nav {
		overflow: hidden;
		padding-bottom: 7px;
	}

	.tab {
		display: inline-block;
		padding: 15px 25px 10px;
		font-size: 18px;
		font-weight: 500;
		position: relative;
		cursor: pointer;
	}

	.main-nav .tab:before {
		content: '';
		position: absolute;
		left: 0;
		bottom: -7px;
		width: 100vw;
		border-bottom: 1px solid #9dd2f1;
	}

	.nav-filters th span:after {
		content: "\21c5";
		font-size: 15px;
	}

	td, th {
		padding: 0px;
	}
	
	th {
		cursor: pointer;
	}

	td:nth-child(1),
	td:nth-child(2) {
		text-align: center;
	}

	.main-nav .active.tab {
		color: #007ac2;
		border-bottom: 5px solid #007ac2;
	}
.log-container {
    margin: 20px;
}

.log-item {
    padding: 10px;
    margin-bottom: 10px;
    border-left: 5px solid transparent;
}

.log-item.info {
    border-left-color: #3498db;
}

.log-item.error {
    border-left-color: #e74c3c;
}

.log-item.warning {
    border-left-color: #f39c12;
}

</style>
<h1>Мониторинг работы HCM Websoft</h1>
<div style="background-color: #f2f2f2; padding: 24px; border-radius: 25px; box-shadow: 0 2px 18px rgba(0,0,0,0.1);">
<h2>UPTIME системы</h2>
    <div class="log-container">
        <div class="log-item info">[2022-01-01 12:00:00] Система успешно запущена</div>
        <div class="log-item error">[2022-01-02 08:30:00] Не удалось подключиться к базе данных</div>
        <div class="log-item warning">[2022-01-03 15:45:00] Низкий уровень свободного места на диске</div>
    </div>
</div><br><br>

</body>
</html>
<script language="javascript">
    <!--
    // initialize a variable to test for javascript 1.1.
    // which is necessary for the window.location.replace method
    var javascriptVersion1_1 = false;
    // -->
</script>

<script language="javascript1.1">
<!--
javascriptVersion1_1 = true;
// -->
</script>

<script language="javascript">

    // initialize global variables
    var detectableWithVB = false;
    var pluginFound = false;
    var check = '<img src="check.png">';
    var x = '<img src="x.png">';

    function goURL(daURL) {
// if the browser can do it, use replace to preserve back button
        if(javascriptVersion1_1) {
            window.location.replace(daURL);
        } else {
            window.location = daURL;
        }
        return;
    }

    function redirectcheck(pluginFound, redirectURL, redirectIfFound) {
// check for redirection
        if( redirectURL && ((pluginFound && redirectIfFound) || (!pluginFound &&!redirectIfFound)) )
        {
// go away
            goURL(redirectURL);
            return pluginFound;
        }
        else
        {
// stay here and return result of plugin detection
            return pluginFound;
        }
    }

    function canDetectplugins()
    {
        if( detectableWithVB || (navigator.plugins && navigator.plugins.length > 0) ) {
            return true;
        } else {
            return false;
        }
    }

    function detectFlash(redirectURL, redirectIfFound) {
        pluginFound = detectplugin('Shockwave','Flash');
// if not found, try to detect with VisualBasic
        if(!pluginFound && detectableWithVB) {
            pluginFound = detectActiveXControl('ShockwaveFlash.ShockwaveFlash.1');
        }
// check for redirection
        return redirectcheck(pluginFound, redirectURL, redirectIfFound);
    }

    function detectDirector(redirectURL, redirectIfFound) {
        pluginFound = detectplugin('Shockwave','Director');
// if not found, try to detect with VisualBasic
        if(!pluginFound && detectableWithVB) {
            pluginFound = detectActiveXControl('SWCtl.SWCtl.1');
        }
// check for redirection
        return redirectcheck(pluginFound, redirectURL, redirectIfFound);
    }

    function detectQuickTime(redirectURL, redirectIfFound) {
        pluginFound = detectplugin('QuickTime');
// if not found, try to detect with VisualBasic
        if(!pluginFound && detectableWithVB) {
            pluginFound = detectQuickTimeActiveXControl();
        }
        return redirectcheck(pluginFound, redirectURL, redirectIfFound);
    }

    function detectReal(redirectURL, redirectIfFound) {
        pluginFound = detectplugin('RealPlayer');
// if not found, try to detect with VisualBasic
        if(!pluginFound && detectableWithVB) {
            pluginFound = (detectActiveXControl('rmocx.RealPlayer G2 Control') ||
            detectActiveXControl('RealPlayer.RealPlayer(tm) ActiveX Control (32-bit)') ||
            detectActiveXControl('RealVideo.RealVideo(tm) ActiveX Control (32-bit)'));
        }
        return redirectcheck(pluginFound, redirectURL, redirectIfFound);
    }

    function detectWindowsMedia(redirectURL, redirectIfFound) {
        pluginFound = detectplugin('Windows Media');
// if not found, try to detect with VisualBasic
        if(!pluginFound && detectableWithVB) {
            pluginFound = detectActiveXControl('MediaPlayer.MediaPlayer.1');
        }
        return redirectcheck(pluginFound, redirectURL, redirectIfFound);
    }

    function detectplugin() {
// allow for multiple checks in a single pass
        var daplugins = detectplugin.arguments;
// consider pluginFound to be false until proven true
        var pluginFound = false;
// if plugins array is there and not fake
        if (navigator.plugins && navigator.plugins.length > 0) {
            var pluginsArrayLength = navigator.plugins.length;
// for each plugin...
            for (pluginsArrayCounter=0; pluginsArrayCounter < pluginsArrayLength; pluginsArrayCounter++ ) {
// loop through all desired names and check each against the current plugin name
                var numFound = 0;
                for(namesCounter=0; namesCounter < daplugins.length; namesCounter++) {
// if desired plugin name is found in either plugin name or description
                    if( (navigator.plugins[pluginsArrayCounter].name.indexOf(daplugins[namesCounter]) >= 0) ||
                            (navigator.plugins[pluginsArrayCounter].description.indexOf(daplugins[namesCounter]) >= 0) ) {
// this name was found
                        numFound++;
                    }
                }
// now that we have checked all the required names against this one plugin,
// if the number we found matches the total number provided then we were successful
                if(numFound == daplugins.length) {
                    pluginFound = true;
// if we've found the plugin, we can stop looking through at the rest of the plugins
                    break;
                }
            }
        }
        return pluginFound;
    } // detectplugin

    // Here we write out the VBScript block for MSIE Windows
    if ((navigator.userAgent.indexOf('MSIE')!= -1) && (navigator.userAgent.indexOf('Win')!= -1)) {
        document.writeln('<script language="VBscript">');

        document.writeln('\'do a one-time test for a version of VBScript that can handle this code');
        document.writeln('detectableWithVB = False');
        document.writeln('If ScriptEngineMajorVersion >= 2 then');
        document.writeln(' detectableWithVB = True');
        document.writeln('End If');

        document.writeln('\'this next function will detect most plugins');
        document.writeln('Function detectActiveXControl(activeXControlName)');
        document.writeln(' on error resume next');
        document.writeln(' detectActiveXControl = False');
        document.writeln(' If detectableWithVB Then');
        document.writeln(' detectActiveXControl = IsObject(CreateObject(activeXControlName))');
        document.writeln(' End If');
        document.writeln('End Function');

        document.writeln('\'and the following function handles QuickTime');
        document.writeln('Function detectQuickTimeActiveXControl()');
        document.writeln(' on error resume next');
        document.writeln(' detectQuickTimeActiveXControl = False');
        document.writeln(' If detectableWithVB Then');
        document.writeln(' detectQuickTimeActiveXControl = False');
        document.writeln(' hasQuickTimechecker = false');
        document.writeln(' Set hasQuickTimechecker = CreateObject("QuickTimecheckObject.QuickTimecheck.1")');
        document.writeln(' If IsObject(hasQuickTimechecker) Then');
        document.writeln(' If hasQuickTimechecker.IsQuickTimeAvailable(0) Then ');
        document.writeln(' detectQuickTimeActiveXControl = True');
        document.writeln(' End If');
        document.writeln(' End If');
        document.writeln(' End If');
        document.writeln('End Function');

        document.writeln('</scr' + 'ipt>');
    }

    function detectBrowser()
    {
        var sReturn = "";
        if(document.documentMode) {
            sReturn += document.documentMode + '.x'
            return sReturn;
        }
        /*
        if (/MSIE (\d+\.\d+);/.test(navigator.userAgent))
        { //test for MSIE x.x;
            sReturn = "Microsoft Internet Explorer "
            var ieversion=new Number(RegExp.$1) // capture x.x portion and store as a number
            if (ieversion>=8)
            {
                sReturn += "8.x";
            }
            else
            {
                if (ieversion>=7)
                {
                    sReturn += "7.x";
                }
                else
                {
                    if (ieversion>=6)
                    {
                        sReturn += "6.x";
                    }
                    else
                    {
                        if (ieversion>=5)
                        {
                            sReturn += "5.x";
                        }
                        else
                        {
                            sReturn += "?";
                        }
                    }
                }
            }
            return sReturn;
        }
        */
        if (/Firefox[\/\s](\d+\.\d+)/.test(navigator.userAgent))
        { //test for Firefox/x.x or Firefox x.x (ignoring remaining digits);
            sReturn = "Firefox "
            var ffversion=new Number(RegExp.$1) // capture x.x portion and store as a number
            if (ffversion>=3)
            {
                sReturn += "3.x";
            }
            else
            {
                if (ffversion>=2)
                {
                    sReturn += "2.x";
                }
                else
                {
                    if (ffversion>=1)
                    {
                        sReturn += "1.x";
                    }
                    else
                    {
                        sReturn += "?";
                    }
                }
            }
            return sReturn;
        }
        if (/Opera[\/\s](\d+\.\d+)/.test(navigator.userAgent))
        { //test for Opera/x.x or Opera x.x (ignoring remaining decimal places);
            sReturn = "Opera ";
            var oprversion=new Number(RegExp.$1) // capture x.x portion and store as a number
            if (oprversion>=10)
            {
                sReturn += "10.x";
            }
            else
            {
                if (oprversion>=9)
                {
                    sReturn += "9.x";
                }
                else
                {
                    if (oprversion>=8)
                    {
                        sReturn += "8.x";
                    }
                    else
                    {
                        if (oprversion>=7)
                        {
                            sReturn += "7.x";
                        }
                        else
                        {
                            sReturn += "?";
                        }
                    }
                }
            }
            return sReturn;
        }
        if (/Chrome[\/\s](\d+\.\d+)/.test(navigator.userAgent))
        { //test for Chrome (ignoring remaining decimal places);
            sReturn = "Chrome ";
            var oprversion=new Number(RegExp.$1) // capture x.x portion and store as a number
            if (oprversion>=3)
            {
                sReturn += "3.x";
            }
            else
            {
                if (oprversion>=2)
                {
                    sReturn += "2.x";
                }
                else
                {
                    if (oprversion>=1)
                    {
                        sReturn += "1.x";
                    }
                    else
                    {
                        sReturn += "?";
                    }
                }
            }
            return sReturn;
        }
        if (/Safari[\/\s](\d+\.\d+)/.test(navigator.userAgent))
        { //test for Chrome (ignoring remaining decimal places);
            sReturn = "Safari ";
            var oprversion=new Number(RegExp.$1) // capture x.x portion and store as a number
            if (oprversion>=4)
            {
                sReturn += "4.x";
            }
            else
            {
                if (oprversion>=3)
                {
                    sReturn += "3.x";
                }
                else
                {
                    if (oprversion>=2)
                    {
                        sReturn += "2.x";
                    }
                    else
                    {
                        sReturn += "?";
                    }
                }
            }
            return sReturn;
        }
    }

    function detectOS()
    {
        var OSName="Unknown OS";
        var OS = navigator.userAgent;
        if (OS.indexOf("Win")!=-1)
        {
            if ((OS.indexOf("Windows NT 5.1")!=-1) || (OS.indexOf("Windows XP")!=-1))
            {
                OSName="Windows XP";
            }
            else
            {
                if ((OS.indexOf("Windows NT 7.0")!=-1) || (OS.indexOf("Windows NT 6.1")!=-1))
                {
                    OSName="Windows 7";
                }
                else
                {
                    if ((OS.indexOf("Windows NT 6.0")!=-1))
                    {
                        OSName="Windows Vista/Server 2008";
                    }
                    else
                    {
                        if (OS.indexOf("Windows ME")!=-1)
                        {
                            OSName="Windows ME";
                        }
                        else
                        {
                            if ((OS.indexOf("Windows NT 4.0")!=-1) || (OS.indexOf("WinNT4.0")!=-1) || (OS.indexOf("WinNT")!=-1))
                            {
                                OSName="Windows NT";
                            }
                            else
                            {
                                if ((OS.indexOf("Windows NT 5.2")!=-1))
                                {
                                    OSName="Windows Server 2003";
                                }
                                else
                                {
                                    if ((OS.indexOf("Windows NT 5.0")!=-1) || (OS.indexOf("Windows 2000")!=-1))
                                    {
                                        OSName="Windows 2000";
                                    }
                                    else
                                    {
                                        if ((OS.indexOf("Windows 98")!=-1) || (OS.indexOf("Win98")!=-1))
                                        {
                                            OSName="Windows 98";
                                        }
                                        else
                                        {
                                            if ((OS.indexOf("Windows 95")!=-1) || (OS.indexOf("Win95")!=-1) || (OS.indexOf("Windows_95")!=-1))
                                            {
                                                OSName="Windows 95";
                                            }
                                            else
                                            {
                                                if((OS.indexOf("Win16")!=-1))
                                                {
                                                    OSName="Windows 3.1";
                                                }
                                                else
                                                {
                                                    OSName="Windows Ver. Unknown";
                                                }
                                            }
                                        }
                                    }
                                }
                            }
                        }
                    }
                }
            }
            if ((OS.indexOf("WOW64")!=-1) || (OS.indexOf("x64")!=-1) || (OS.indexOf("Win64")!=-1) || (OS.indexOf("IA64")!=-1))
            {
                OSName += " (x64)";
            }
            else
            {
                OSName += " (x32)";
            }
        }
        else
        {
            if (OS.indexOf("Mac")!=-1)
            {
                OSName="MacOS";
            }
            else
            {
                if (OS.indexOf("X11")!=-1)
                {
                    OSName="UNIX";
                }
                else
                {
                    if (OS.indexOf("Linux")!=-1)
                    {
                        OSName="Linux";
                    }
                }
            }
        }
        return OSName;
    }
</script>

<meta http-equiv="Content-Type" content="text/html; charset=utf-8">
<style type="text/css">
    <!--
    body {

    }
    .style1 {color: #990000}
    -->
</style></head>

<body>
<div style="background-color: #f2f2f2; padding: 24px; border-radius: 25px; box-shadow: 0 2px 18px rgba(0,0,0,0.1);">
<h2>Информация о пользователе</h2>
<script language="javascript">
    document.write('<b>Ваша операционная система:</b> ' + detectOS());
    document.write('<br><b>Ваш браузер:</b> ' + detectBrowser());
    document.write('<br><b>Javascript разрешен:</b> ' + canDetectplugins() + '<br/>');

    if(canDetectplugins()) {
        document.write('<b>Shockwave установлен:</b> ' + detectDirector() + '<br/>' +
        '<b>Flash установлен:</b> ' + detectFlash() + '<br/>' +
        '<b>QuickTime установлен:</b> ' + detectQuickTime() + '<br/>' +
        '<b>RealPlayer установлен:</b> ' + detectReal() + '<br/>' +
        '<b>Windows Media Player установлен:</b> ' + detectWindowsMedia());
    }
</script>
</div><br><br>
<noscript class="style1">
    Ваш браузер не поддерживает JavaScript
</noscript>
<div style="background-color: #f2f2f2; padding: 24px; border-radius: 25px; box-shadow: 0 2px 18px rgba(0,0,0,0.1);">
<h2>Статистика по показателям</h2>
    <canvas id="myChart"></canvas>
</div>
<script>
const data = {
    labels: ['Сотрудники', 'Организации', 'Подразделения'],
    datasets: [{
        data: [30, 40, 10],
        backgroundColor: ['#ff0000', '#0000ff', '#ffff00']
    }]
};

const ctx = document.getElementById('myChart').getContext('2d');
const myChart = new Chart(ctx, {
    type: 'doughnut',
    data: data,
options: {
                responsive: false
            }
});
</script>
<style>
canvas {
    width: 50px;
    height: 50px;
}
</style>
<br><br>

<div style="background-color: #f2f2f2; padding: 24px; border-radius: 25px; box-shadow: 0 2px 18px rgba(0,0,0,0.1);">
<h2>Тестирование базы данных</h2>
<% 
// ВРЕМЯ РАБОТЫ БД
check_current_db = false; 

countUsers = 100; 
userDescSize = 1; 


function random_str(length) 
{ 
        var i; 

        rstr = ''; 

        for (i=1;i<=length;i++) 
        { 
                rstr = rstr + String.fromCharCode(Random(30,102)); 
        } 

        return Base64Encode(rstr); 
} 

allStart = CurDate; 

Response.Write('<p>Начало теста: ' +CurDate+'</p>'); 

userDesc = random_str(userDescSize); 

if(!check_current_db)  
{  

start = CurDate; 

for (i=0;i<countUsers;i++) 
{ 

y = OpenNewDoc('x-local://wtv/wtv_banner.xmd'); 

y.BindToDb(); 


y.TopElem.code = 'XAUTO'; 
y.TopElem.name = 'XAUTO'; 
y.TopElem.zone = userDesc; 

y.Save(); 
} 

try
{
	if ( tools.sys_db_capability & tools.UNI_CAP_SYNC_CATALOG )
		tools.sync_catalog('banners');
}
catch(e)
{

}

Response.Write('<li>Создание '+countUsers+' записей баннеров (секунд): ' +DateDiff(CurDate,start)+'</li>'); 

start = CurDate; 

idx=0; 

usersArr = ArraySelectAll(XQuery('for $i in banners where $i/code="XAUTO" return $i')); 

for(i in usersArr) 
{ 
        DeleteDoc(UrlFromDocID(i.id),true) 
        idx++; 
        //if (idx>=countUsers) 
           //     break; 
} 

try
{
	if ( tools.sys_db_capability & tools.UNI_CAP_SYNC_CATALOG )
		tools.sync_catalog('banners');
}
catch(e)
{

}

Response.Write('<li>Удаление '+idx+' записей баннеров (секунд): ' +DateDiff(CurDate,start)+'</li>'); 


start = CurDate; 

for (i=0;i<countUsers;i++) 
{ 

y = OpenNewDoc('x-local://wtv/wtv_collaborator.xmd'); 

y.BindToDb(); 


y.TopElem.firstname = 'XAUTO'; 
y.TopElem.lastname = 'XAUTO'; 
y.TopElem.login = 'XAUTO'; 
y.TopElem.desc = userDesc; 


y.Save(); 
} 

try
{
	if ( tools.sys_db_capability & tools.UNI_CAP_SYNC_CATALOG )
		tools.sync_catalog('collaborators');
}
catch(e)
{

}

Response.Write('<li>Создание '+countUsers+' записей сотрудников (секунд): ' +DateDiff(CurDate,start)+'</li>'); 

userDesc = random_str(userDescSize); 

start = CurDate; 

idx=0; 

usersArr = ArraySelectAll(XQuery('for $i in collaborators where $i/login="XAUTO" and $i/fullname="XAUTO XAUTO" return $i')); 

for(i in usersArr) 
{ 
        doc = OpenDoc(UrlFromDocID(i.id)); 

        doc.TopElem.desc = userDesc; 
        doc.Save(); 
        idx++; 
        //if (idx>=countUsers) 
           //     break; 
} 

try
{
	if ( tools.sys_db_capability & tools.UNI_CAP_SYNC_CATALOG )
		tools.sync_catalog('collaborators');
}
catch(e)
{

}

Response.Write('<li>Сохранение '+idx+' записей сотрудников (секунд): ' +DateDiff(CurDate,start)+'</li>'); 


y = OpenNewDoc('x-local://wtv/wtv_course.xmd'); 

y.BindToDb(); 

y.TopElem.code = 'XXX_WT_AUTO'; 
y.TopElem.name = 'XXX_WT_AUTO'; 

y.Save(); 

idx=0; 
usersArr = ArraySelectAll(XQuery('for $i in collaborators where $i/login="XAUTO" and $i/fullname="XAUTO XAUTO" return $i')); 

for(i in usersArr) 
{ 
        tools.activate_course_to_person(i.id, y.DocID);         
        idx++; 
        //if (idx>=countUsers) 
           //     break;
} 

try
{
	if ( tools.sys_db_capability & tools.UNI_CAP_SYNC_CATALOG )
		tools.sync_catalog('active_learnings');
}
catch(e)
{

}


Response.Write('<li>Назначение '+idx+' записей сотрудников (секунд): ' +DateDiff(CurDate,start)+'</li>'); 


start = CurDate; 

idx=0; 
usersArr = ArraySelectAll(XQuery('for $i in active_learnings where $i/course_id='+y.DocID+' return $i')); 

for(i in usersArr) 
{ 
        DeleteDoc(UrlFromDocID(i.id),true) 
        idx++; 
        //if (idx>=countUsers) 
           //     break; 
} 

try
{
	if ( tools.sys_db_capability & tools.UNI_CAP_SYNC_CATALOG )
		tools.sync_catalog('active_learnings');
}
catch(e)
{

}

Response.Write('<li>Удаление '+idx+' незавершенных курсов (секунд): ' +DateDiff(CurDate,start)+'</li>'); 

DeleteDoc(UrlFromDocID(y.DocID),true) 

start = CurDate; 

idx=0; 
usersArr = ArraySelectAll(XQuery('for $i in collaborators where $i/login="XAUTO" and $i/fullname="XAUTO XAUTO" return $i')); 

for(i in usersArr) 
{ 
        DeleteDoc(UrlFromDocID(i.id),true) 
        idx++; 
        //if (idx>=countUsers) 
           //     break; 
} 

try
{
	if ( tools.sys_db_capability & tools.UNI_CAP_SYNC_CATALOG )
		tools.sync_catalog('collaborators');
}
catch(e)
{

}

Response.Write('<li>Удаление '+idx+' записей сотрудников (секунд): ' +DateDiff(CurDate,start)+'</li>'); 

} 

if(check_current_db) 
{ 
        start = CurDate; 

        for(i in collaborators) 
        { 
                doc = OpenDoc(UrlFromDocID(i.id)).TopElem; 
        } 

        Response.Write('<li>Полный просмотр таблицы пользователей ['+ArrayCount(collaborators)+' записей] (секунд): ' +DateDiff(CurDate,start)+'</li>'); 

        start = CurDate; 

        for(i in collaborators) 
        { 
                a = i.fullname; 
        } 

        Response.Write('<li>Полный просмотр записей пользователей ['+ArrayCount(collaborators)+' записей] (секунд): ' +DateDiff(CurDate,start)+'</li>'); 

        start = CurDate; 

        for(i in learnings) 
        { 
                doc = OpenDoc(UrlFromDocID(i.id)).TopElem; 
        } 

        Response.Write('<li>Полный просмотр записей завершенных курсов ['+ArrayCount(learnings)+' записей] (секунд): ' +DateDiff(CurDate,start)+'</li>'); 


        start = CurDate; 

        for(i in groups) 
        { 
                doc = OpenDoc(UrlFromDocID(i.id)).TopElem; 
        } 

        Response.Write('<li>Полный просмотр записей групп ['+ArrayCount(groups)+' записей] (секунд): ' +DateDiff(CurDate,start)+'</li>'); 
} 

Response.Write('<li>Всего на тест (секунд): ' +DateDiff(CurDate,allStart)+'</li>'); 


Response.Write('<p>Конец теста: ' +CurDate+'</p>'); 

%>
<input id="clickMe" type="button" value="Протестировать" onclick="" />

</div>
