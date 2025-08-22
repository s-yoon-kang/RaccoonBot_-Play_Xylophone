# Play_Xylophone

해당 코드는 RaccoonBot이 악보에 맞춰 실로폰을 연주하는 예제입니다.

![라쿤 키보드]()

예제에는 **잘못된 입력 감지**, **대/소문자 감지**, **키 입력 감지/재시도** 기능이 있습니다.
<br>

아래 버튼을 눌러 파이썬 코드를 다운로드 받아 RaccoonBot의 동작을 확인해보세요.

<br><br><br>

#### [Raccoon_keyboard_Typing.py 다운로드]()
#### [시작하기에 앞서]()
#### [초보자를 위한 파이썬 설치 가이드](https://github.com/RobomationLAB/Hamster-S_API_KR/wiki/%EC%B4%88%EB%B3%B4%EC%9E%90%EB%A5%BC-%EC%9C%84%ED%95%9C-%ED%8C%8C%EC%9D%B4%EC%8D%AC-%EC%84%A4%EC%B9%98-%EA%B0%80%EC%9D%B4%EB%93%9C)
#### [하드웨어 설명](https://github.com/RoboidStudioLAB/Wiki_Image/wiki/%EB%9D%BC%EC%BF%A4-%ED%95%98%EB%93%9C%EC%9B%A8%EC%96%B4-%EC%84%A4%EB%AA%85)



<br>

---

<br><br><br><br>


# 예제 설명
- 사용자가 코드에 반복 타이핑할 문장을 **영어**로 **["문장"]** 과 같이 입력합니다. 

  <img width="569" height="165" alt="Image" src="https://github.com/user-attachments/assets/78056e0e-83d0-4392-a9c0-40b78b0fce89" />


<br><br>

- 여러 문장의 경우 다음과 같이 **["문장 1", "문장 2"]** 로 나눠서 작성합니다.

  <img width="715" height="166" alt="Image" src="https://github.com/user-attachments/assets/237277ba-68a3-42e8-8a9b-6d395765a971" />


<br><br>

- 코드를 실행하면 라쿤이 타이핑 자세로 준비한 후 로그 출력과 함께 타이핑을 시작합니다.

  <img width="534" height="127" alt="Image" src="https://github.com/user-attachments/assets/34250add-1295-4f03-a9b1-9cd1ad9e8a80" />


<br><br>

- 대/소문자는 **Caps Lock 토글**로 제어하여 입력합니다.

  <img width="602" height="150" alt="Image" src="https://github.com/user-attachments/assets/73b41e4c-7390-4573-9e8a-c1aa441eb596" />


<br><br>

- 잘못된 키 입력을 실시간으로 감지하며 **오동작 시 해당 단어를 건너뛰고 Enter 후 다음 단어로 진행**합니다.

  <img width="668" height="76" alt="Image" src="https://github.com/user-attachments/assets/589bf472-e314-411e-bfb2-37913c58b777" />


<br><br>

동작에 따른 소리는 다음과 같습니다.

<br>

- 타이핑을 할 준비가 되었다면 **BEEP** 소리
- 잘못된 키 입력시 **ENGINE** 소리
- 타이핑을 완료하면 **GOOD JOB** 소리



<br>

---

<br><br><br><br>


# 준비물 및 방법
### 준비물
- RaccoonBot
- 키보드용 말단 장치
- PC (Windows 권장)
- 키보드 (Coms 블루투스 키보드(미니) V3.0 또는 RaccoonBot이 모두 상호작용 가능한 크기)
- Python 3.9+
- 패키지: `roboid`, `threading`, `keyboard`, `ctypes`, `time`

<br><br>
### 세팅
- RaccoonBot과 키보드를 **5cm** 간격을 두고 **마주보게** 배치해주세요.

  <img width="500" height="400" alt="Image" src="https://github.com/user-attachments/assets/6e493534-edd2-477e-9397-18614ac4790a" />


<br><br>

- **Joint 4**가 **수직**으로 키의 정중앙을 누를 수 있게 위치를 조절하며 **key_mapping** 함수를 수정합니다.

  <img width="500" height="400" alt="Image" src="https://github.com/user-attachments/assets/73220c2d-ced2-4b4c-8178-90f19193a4b0" />


<br><br>

- **key_mapping** 함수와 **RaccoonBot**의 **XYZ 좌표계**는 다음과 같습니다. (단위: cm)

  <img width="500" height="500" alt="Image" src="https://github.com/user-attachments/assets/12c8777d-20ad-4e7d-983b-cd4033817549" /> <img width="472" height="219" alt="Image" src="https://github.com/user-attachments/assets/02a18a92-bdf9-423a-80f0-47903d1bed77" />


<br><br>

- **Z축**의 경우 키보드를 완전히 누르는 좌표보다 **0.2cm 더 낮게** 설정합니다.

  <img width="764" height="218" alt="Image" src="https://github.com/user-attachments/assets/8f6145cb-52f2-431c-8cac-0dfb8f1fadff" />

<br><br>

- **1 ~ 0** | **a ~ z** | **,** | **.** | **Caps lock** | **Space** | **Enter**의 좌표를 모두 수정하고 문장 입력에 차례대로 입력하며 확인합니다.

  <img width="1520" height="360" alt="Image" src="https://github.com/user-attachments/assets/3a01331f-c1b0-402b-b966-d7c0ff4fa67c" />

<br>

---

<br><br><br><br>


# 코드 설명
