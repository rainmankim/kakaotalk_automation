<img align="center" src="https://user-images.githubusercontent.com/62319355/105825928-1e9d7e00-5ffb-11eb-991a-097e7aa9130e.jpg" alt="Kakao Team">

# 파이썬으로 카카오톡 자동화시키기
:smile: :grinning: :sleepy: :relieved: :confused: :open_mouth: :astonished: :thumbsup:


```
안녕하세요 rainmankim 입니다.
자세한 사항은 ipynb 파일을 참조해주세요.
의견이나 피드백이 있으시다면 rainmankim@gmail.com 으로 메일 부탁드리겠습니다 ^^

다수의 대상에게 메세지를 보내려면 굉장히 번거롭죠?
API 를 활용할 수도 있겠지만 API를 활용하는 것은 더 복잡합니다.
이번에는 파이썬 pyautogui 를 활용해서 쉽게 카카오톡 메세지 보내기를 자동화 해보겠습니다.
```


## 이번 강의에서는 총 여섯가지의 function을 이용하여서 자동화해보겠습니다.
```
kill_kakao()  # 카카오톡 종료
open_kakao()  # 카카오톡 실행
login_kakao() # 카카오톡 로그인
find_fren(fren) # 카카오톡 친구(들) 찾기
send_message(message) # 메세지 보내기
auto_send(target, message) # 그리고 최종 메인 function입니다.
```

## 강의에 앞서서 자동화 원리를 설명해드리겠습니다.
```
Pyautogui 와 opencv 를 위주로 자동화가 되는데요.
여러분의 눈이 카카오톡 UI를 보고 클릭하듯이
아래 코드는 0.9의 정확도로 login_password 이미지와 매칭하는 픽셀위치를 찾습니다.

button_location = pyautogui.locateOnScreen('images/login_login.png', confidence=0.9)  

if button_location is None and button_location_2 is None:
    print("패스워드 버튼 찾기 실패 ㅠㅠ")
elif button_location is not None:
    button_point = pyautogui.center(button_location)
    pyautogui.click(button_point.x, button_point.y)  # 그 다음은 이렇게 클릭해주고
    pyautogui.write('Hello World')  # 텍스트를 입력해주면 됩니다.

```

<img align="center" src="https://user-images.githubusercontent.com/62319355/105826059-4987d200-5ffb-11eb-8724-0eb35fb0eac9.png" alt="Kakao Login">

### 흐려서 잘 안보이지만 아래 이미지 비슷한 픽셀을 찾는 겁니다.
<img align="center" src="https://user-images.githubusercontent.com/62319355/105826183-6ae8be00-5ffb-11eb-8089-bb177772ae8e.png" alt="Login ">



## Credits
```
- 웨커 TV
```
