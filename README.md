# 세력봉 매매기법을 활용한 주식자동매매 프로그램입니다.

**세력봉이란?**</br>
세력이 관여했다는 증거

**매수 전략**</br>
전일 종가대비 당일 15%이상</br>
당일 시가대비 10%이상</br>

**매도 전략**
당일 장 마감전 일괄 판매

**필수 요소**
1. python 32bit 필요. (버젼 상관없음)
2. python, pythonw 속성 - [호환성] - 관리자 권한으로 실행 체크
3. 크레온plus
4. 대신증권 계좌 개설
5. Slack
5. Slack OAuth code

*크레온 plus 사용 및 python 설치 참고 영상*</br>
https://www.youtube.com/watch?v=4DzGOpsT3bw

*Slack 알림 봇 만들기 참고 영상*</br>
https://www.youtube.com/watch?v=s24dxIp-Cp0

**필요 모듈 설치**</br>
cmd창 실행</br>
pip install pywinauto</br>
pip install pandas</br>
pip install pywin32</br>
pip install slacker</br>
(pip upgrade 경고가 뜰 시 python -m pip install --upgrade pip)</br>

**사용 방법**
1. AutoConnect.py - line 12
app.start('C:\CREON\STARTER\coStarter.exe /prj:cp /id:*** /pwd:*** /pwdcert:*** /autostart')
*** -> 자신의 id, pw, 인증서로 교체

2. ETFAlgoTrader.py - line 11
slack = Slacker('자신의 Slack OAuth Code')
맨 앞에 # 제거후  자신의 Slack OAuth Code를 입력합니다.

3. ETFAlgoTrader.py - line 18
slack.chat.post_message('#stock', strbuf)
#stock 부분을 자신의 slack 채널로 교체합니다.

4. ETFAlgoTrader.py - line 269
종목명이 담긴 symbol_list를 자신이 투자하길 원하는 종목으로 교체합니다.