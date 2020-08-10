<html class=" js boxshadow pointerevents placeholder"><head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>TOZ</title>
    <link rel="shortcut icon" href="/images/favicon.ico">
    <link rel="stylesheet" type="text/css" href="/css/login_style.css">
	<script type="text/javascript" async="" src="https://www.gstatic.com/recaptcha/releases/IU7gZ7o6RDdDE6U4Y1YJJWnN/recaptcha__ko.js"></script><script src="/assets/js/jquery-1.11.1.min.js"></script>
    <script src="/customForm/js/modernizr.custom.63321.js"></script>
    <!--[if lte IE 7]>
    <style>.main {display: none;}.support-note .note-ie {display: block;}</style><![endif]-->
    <style>

        body{
		background: url(/images/bg_main01.png) no-repeat;
		background-size: cover;
		}

		.video_bg{
		position: absolute;
		left: 0;
		top: -10px;
		width: 100%;
		height: 200%;
		background: #161616;
		overflow: hidden;
		opacity: 0.2;
		}

        .full_screen {
            position: fixed;
            left: 0;
            right: 0;
            top: 0;
            bottom: 0;
            width: 100%;
            height: 100%;
            -o-object-fit: cover;
            -ms-object-fit: cover;
            object-fit: cover;
            z-index: 0;
            opacity: 0.6;
        }
		
		

        .chrome-layer {
            background: rgba(42, 42, 42, 0.8);
            width: 100%;
            position: absolute;
            z-index: 998;
            left: 0;
            top: 0;
            text-align: center;
        }


    </style>
</head>

<body onload="start()" onresize="resize()" onorientationchange="resize()" onmousedown="context.fillStyle='rgba(0,0,0,'+opacity+')'" onmouseup="context.fillStyle='rgb(0,0,0)'">


<div id="login_wrap">
    <div class="cs_center">
        <em>Copyright TOZ Corp (C). All Rights Reserved.</em>
    </div>
    <form class="login_slate">

        <div class="polygon_box active">
            <div class="login_polygon1"></div>
            <div class="login_polygon2"></div>
        </div>
<script>


function run_logo()
{

  $('#glitter').fadeIn(1000);
  $('#glitter').fadeOut(1000);

}
run_logo()
setInterval(run_logo,2000);


</script>
        
            <div class="login_area">
                <div class="login_box active">
                    <h1><img src="/images/logo_login.png">
                    </h1>
					<div id="glitter" style="position: absolute; top: 67px; left: 260px; display: block; opacity: 0.0909251;">
					<img src="/images/toz_2.png">
					</div>
                    <input type="hidden" name="use_otp" id="use_otp" value="0">
                    <h4><input type="text" name="l_username" id="l_username" placeholder="아이디" maxlength="20" onkeydown="javascript:if(event.keyCode == 13) login.goLogin();"></h4>
                    <h4><input type="password" name="l_password" id="l_password" placeholder="비밀번호" maxlength="20" onkeydown="javascript:if(event.keyCode == 13) login.goLogin();"></h4>
                    <h6>
					<span class="login" onclick="javascript:login.goLogin();" style="-webkit-box-shadow: inset 0px 0px 0px 2px rgba(209,209,209,1);
-moz-box-shadow: inset 0px 0px 0px 2px rgba(209,209,209,1);
box-shadow: inset 0px 0px 0px 2px rgba(209,209,209,1);">
						<em></em>
						<code>로그인</code>
					</span>
					<br>
                        <a class="join">
						<span onclick="code_join();" class="join" style="margin-top:6px; -webkit-box-shadow: inset 0px 0px 0px 2px rgba(209,209,209,1);
-moz-box-shadow: inset 0px 0px 0px 2px rgba(209,209,209,1);
box-shadow: inset 0px 0px 0px 2px rgba(209,209,209,1);">
						<em></em>
						<code>회원가입</code>
					</span>
					</a>
                        <br><span style="position:absolute; left:28px; margin-top:10px"><img id="speaker" src="/images/cus.png" width="375px" class="speaker" onclick="fnSpeaker()"></span>
                    </h6>
                </div>
            </div>
        </form>
</div>

<form id="frm" name="myFrm" onsubmit="return login.checkCode();" class="form-2">
<div class="code_area">
    <div class="code_box" style="background:#000000c7;border-radius: 50px;">
        <h1>가입코드</h1>
        <h2>JOIN CODE</h2>
        <h4>
            <input type="text" autocomplete="off" name="joinCode" id="joinCode" class="essential code" maxlength="20" placeholder="가입코드">
        </h4>
        <h5>
				<span class="join">
				
					<em></em>
					<code><input type="submit" style="left: 0;
    position: absolute;
    background: none;
    width: 100%;
    height: 100%;
    border: none;" name="submit" value="">가입</code>
				</span>
            <span class="cancel" onclick="code_cancel();">
                <em></em>
                <code>취소</code>
            </span>
        </h5>
    </div>
</div>
</form>

<form id="frm-join" name="frm-join" method="post" onsubmit="return recaptcha_check();">
    <input type="hidden" id="g-recaptcha" name="g-recaptcha">
    <input type="hidden" id="code" name="code">
    <div class="join_area">
        <div class="join_box" style="padding-top: 35px; background: #000000c7; padding-left: 35px; padding-right: 35px;border-radius: 50px;height:670px;">
            <h1>회원가입</h1>
            <h2>CREATE ACCOUNT</h2>
            <h3>＊표시 필수 입력사항</h3>
            <h4>
                <ul class="left">
                    <li>
                        <input type="text" autocomplete="off" name="userid" id="userid" class="essential code" maxlength="20" placeholder="아이디">
                    </li>
                    <li class="gap"><span>영문/숫자 조합 4~12자 이내로 작성.</span></li>
                    <li>
                        <input type="text" autocomplete="off" name="nickname" id="nickname" class="essential code" maxlength="12" placeholder="닉네임">
                    </li>
                    <li class="gap"><span>영문/숫자 조합 4~12자 이내로 작성.</span></li>
                    <li><input type="password" name="password" id="password" class="essential" maxlength="16" placeholder="비밀번호"></li>
                    <li><input type="password" name="passwordConfirm" id="passwordConfirm" class="essential confirm" maxlength="16" placeholder="비밀번호 확인"></li>
                    <li class="gap"><span>영문 및 숫자 특수문자 조합 4자 이상으로 작성.</span></li>
                    <li>
                        <input type="text" autocomplete="off" name="phone" id="phone" class="essential code" maxlength="12" placeholder="휴대폰 번호">
                    </li>
                    <li class="gap"><span id="bul-phone"></span></li>
                </ul>

                <ul>
                    <li class="gap">
                        <select id="bank" name="bank" class="bank" required="">
                            <option value="">은행선택</option>
                            <option value="국민은행">국민은행</option>
                            <option value="우리은행">우리은행</option>
                            <option value="농협">농협</option>
                            <option value="신한은행">신한은행</option>
                            <option value="기업은행">기업은행</option>
                            <option value="KEB하나은행">KEB하나은행</option>
                            <option value="SC제일">SC제일</option>
                            <option value="씨티은행">씨티은행</option>
                            <option value="HSBC은행">HSBC은행</option>
                            <option value="우체국">우체국</option>
                            <option value="신협">신협</option>
                            <option value="수협">수협</option>
                            <option value="새마을금고">새마을금고</option>
                            <option value="부산은행">부산은행</option>
                            <option value="광주은행">광주은행</option>
                            <option value="대구은행">대구은행</option>
                            <option value="전북은행">전북은행</option>
                            <option value="제주은행">제주은행</option>
                            <option value="경남은행">경남은행</option>
                            <option value="케이뱅크">케이뱅크</option>
                            <option value="카카오뱅크">카카오뱅크</option>
                            <option value="미래에셋대우증권">미래에셋대우증권</option>
                            <option value="신한투자증권">신한투자증권</option>
                            <option value="KB증권">KB증권</option>
                        </select>
                    </li>
                    <li><input type="text" autocomplete="off" name="depositor" id="depositor" required="" maxlength="24" class="essential" placeholder="예금주"></li>
                    <li><input type="text" autocomplete="off" name="account" id="account" required="" maxlength="24" class="essential" placeholder="계좌번호"></li>
                    <li class="gap"><span id="bul-account" class="bul"></span></li>
                    <li>
                        <input type="text" autocomplete="off" name="bankPassword" id="bankPassword" class="essential code" maxlength="16" placeholder="충환전 비밀번호">
                    </li>
                    <li>
                        <input type="text" autocomplete="off" name="bankPasswordConfirm" id="bankPasswordConfirm" class="essential code" maxlength="16" placeholder="충환전 비밀번호 확인">
                    </li>
                    <li class="gap"><span>영문 및 숫자 특수문자 조합 4자 이상으로 작성.</span></li>

                    

                    <li>
                        
                    </li>

                    <li>
                        
                    </li>

                    <li>
                        
                    </li>
                </ul>
            </h4>
            <h5>
                <div class="g-recaptcha" data-sitekey="6LcFzwAVAAAAAD6kZGADUxaFiA4SQl2MFKxfRQz2"><div style="width: 304px; height: 78px;"><div><iframe src="https://www.google.com/recaptcha/api2/anchor?ar=1&amp;k=6LcFzwAVAAAAAD6kZGADUxaFiA4SQl2MFKxfRQz2&amp;co=aHR0cDovL3R6LTEwMS5jb206ODA.&amp;hl=ko&amp;v=IU7gZ7o6RDdDE6U4Y1YJJWnN&amp;size=normal&amp;cb=j9s06b8segha" width="304" height="78" role="presentation" name="a-h5zz10d1qzca" frameborder="0" scrolling="no" sandbox="allow-forms allow-popups allow-same-origin allow-scripts allow-top-navigation allow-modals allow-popups-to-escape-sandbox"></iframe></div><textarea id="g-recaptcha-response" name="g-recaptcha-response" class="g-recaptcha-response" style="width: 250px; height: 40px; border: 1px solid rgb(193, 193, 193); margin: 10px 25px; padding: 0px; resize: none; display: none;"></textarea></div><iframe style="display: none;"></iframe></div>
				<span class="join" onclick="recaptcha_check();">
					<em></em>
					<code>가입</code>
				</span>
                <span class="cancel" onclick="member_cancel();">
					<em></em>
					<code>취소</code>
				</span>
            </h5>
        </div>
    </div>
</form>

<!-- jQuery if needed -->
<script src="/assets/js/jquery-1.11.1.min.js"></script>
<script src="https://www.google.com/recaptcha/api.js" async="" defer=""></script>
<script>
    // grecaptcha.ready(function() {
    //     grecaptcha.execute('6LffnAAVAAAAAP9ljvBq1N9MQvJS0kyysmslfgNG', {action: 'login'}).then(function(token) {
    //         // 토큰을 받아다가 g-recaptcha 에다가 값을 넣어줍니다.
    //         document.getElementById('g-recaptcha').value = token;
    //     });
    // });
    //
    // function SetCaptchaToken() {
    //     grecaptcha.execute('6LffnAAVAAAAAP9ljvBq1N9MQvJS0kyysmslfgNG', {action: 'login'}).then(function (token) {
    //         // 토큰을 받아다가 g-recaptcha 에다가 값을 넣어줍니다.
    //         document.getElementById('g-recaptcha').value = token;
    //     });
    // }
    // //SetCaptchaToken();
    // setInterval(function () { SetCaptchaToken(); }, 2 * 60 * 1000);

    function recaptcha_check () {
        var v = grecaptcha.getResponse();

        if(v.length == 0) {
            alert("캡챠 버튼을 클릭하세요;");
            return false;
        } else {
            login.goJoin();
            return true;
        }
    }

    setTimeout(function(){
        $(".polygon_box").addClass("active");
        var vid = document.getElementById("video_bg");
        vid.autoplay=true;
        vid.load();
    },1000);
    setTimeout(function(){
        $(".login_box").addClass("active");
    },1500);

    function fnSpeaker(){
        var vid = document.getElementById("video_bg");
        if(vid.muted){
            vid.muted = false;
            $('#speaker').attr('src','/images/speaker.png');
        }else{
            vid.muted = true;
            $('#speaker').attr('src','/images/Mute-256.png');
        }
    }


    function code_join(){

        $(".login_box").removeClass("active");
        setTimeout(function(){
            $(".login_slate").addClass("active");
            $(".login_area").hide();
            $(".code_area").show();
        },1500);
        setTimeout(function(){
            $(".code_box").addClass("active");
            $('#joinCode').val("");
            $('#joinCode').focus();
        },1600);
    }

    function member_join(n){
        if(n==1){
            $(".login_box").removeClass("active");
            setTimeout(function(){
                $(".login_slate").addClass("active");
                $(".login_area").hide();
                $(".join_area").show();
            },1500);
            setTimeout(function(){
                $(".joiGn_box").addClass("active");
            },1600);
        }else {
            $.ajax({
                url: '/join/code',
                method: 'post',
                data: {
                    joinCode: $('#joinCode').val()
                }
            }).done(function (data) {
                console.log(data)
                if (data.success) {
                    $('#code').val($('#joinCode').val());
                    $('form')[1].reset();
                    $("#reg_check_code").val('0');
                    $("#reg_check_hp").val('0');
                    $("#reg_mb_id").removeAttr("readonly");
                    $("#reg_mb_hp").removeAttr("readonly");
                    $("#reg_mb_recommend").removeAttr("readonly");
                    $(".bet_style").removeAttr("checked");
                    $("#reg_hp_code").hide();
                    $("#btn_check_hp").show();
                    $(".code_box").removeClass("active");
                    console.log(4)

                    setTimeout(function () {
                        $(".code_slate").addClass("active");
                        $(".code_area").hide();
                        $(".join_area").show();
                    }, 1500);
                    setTimeout(function () {
                        $(".join_box").addClass("active");
                    }, 1600);
                }
            });
        }
    }

    function code_cancel(){
        $(".code_box").removeClass("active");
        setTimeout(function(){
            $(".login_slate").removeClass("active");
            $(".code_area").hide();
            $(".login_area").show();
        },100);
        setTimeout(function(){
            $(".login_line").addClass("active");
            $(".login_box").addClass("active");
        },500);
    }

    function member_cancel(){
        $(".join_box").removeClass("active");
        setTimeout(function(){
            $(".login_slate").removeClass("active");
            $(".join_area").hide();
            $(".login_area").show();
        },100);
        setTimeout(function(){
            $(".login_line").addClass("active");
            $(".login_box").addClass("active");
        },500);
    }

    function member_complete(){
        $(".join_box").removeClass("active");
        setTimeout(function(){
            $(".login_slate").removeClass("active");
            $(".join_area").hide();
            $(".complete_area").show();
        },100);
        setTimeout(function(){
            $(".complete_box").addClass("active");
        },500);
    }


    // FOCUS
    $(".input_box").focus(function(){
        $(this).prev("div").addClass("focus");
    });
    $(".input_box").focusout(function(){
        $(this).prev("div").removeClass("focus");
    });

    // CONFIRM
    $(".confirm").focusout(function(){
        $(this).next("code").addClass("confirm");
    });

    var config = {"requiredRecommend":false,"checkRecommend":false,"duplicatePhone":true,"duplicateAccount":true};
</script>

<script src="/js/common.js"></script>
<script src="/js/common.join.js?ver=1.4"></script>
<script src="/images/365_files/particles.min.js"></script>
<script src="/images/365_files/app.js"></script>

<div style="background-color: rgb(255, 255, 255); border: 1px solid rgb(204, 204, 204); box-shadow: rgba(0, 0, 0, 0.2) 2px 2px 3px; position: absolute; transition: visibility 0s linear 0.3s, opacity 0.3s linear 0s; opacity: 0; visibility: hidden; z-index: 2000000000; left: 0px; top: -10000px;"><div style="width: 100%; height: 100%; position: fixed; top: 0px; left: 0px; z-index: 2000000000; background-color: rgb(255, 255, 255); opacity: 0.05;"></div><div class="g-recaptcha-bubble-arrow" style="border: 11px solid transparent; width: 0px; height: 0px; position: absolute; pointer-events: none; margin-top: -11px; z-index: 2000000000;"></div><div class="g-recaptcha-bubble-arrow" style="border: 10px solid transparent; width: 0px; height: 0px; position: absolute; pointer-events: none; margin-top: -10px; z-index: 2000000000;"></div><div style="z-index: 2000000000; position: relative;"><iframe title="recaptcha challenge" src="https://www.google.com/recaptcha/api2/bframe?hl=ko&amp;v=IU7gZ7o6RDdDE6U4Y1YJJWnN&amp;k=6LcFzwAVAAAAAD6kZGADUxaFiA4SQl2MFKxfRQz2&amp;cb=ezypbch21rbx" name="c-h5zz10d1qzca" frameborder="0" scrolling="no" sandbox="allow-forms allow-popups allow-same-origin allow-scripts allow-top-navigation allow-modals allow-popups-to-escape-sandbox" style="width: 100%; height: 100%;"></iframe></div></div></body></html>
