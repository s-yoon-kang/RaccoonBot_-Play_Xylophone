# Play_Xylophone

해당 코드는 RaccoonBot이 악보에 맞춰 실로폰을 연주하는 예제입니다.

![라쿤 실로폰]()

예제는 **악보**, **시작 위치 이동**, **건반 타격**, **음 각도 이동** 기능으로 동작합니다.
<br>

아래 버튼을 눌러 Block Composer 코드를 다운로드 받아 RaccoonBot의 동작을 확인해보세요.

<br><br><br>

#### [Raccoon_Play_Xylophone.block 다운로드]()
#### [시작하기에 앞서]()
#### [블록컴포저 환경 설정 가이드](https://github.com/RoboidStudioLAB/Wiki_Image/wiki/%EB%B8%94%EB%A1%9D%EC%BB%B4%ED%8F%AC%EC%A0%80-%ED%99%98%EA%B2%BD-%EC%84%A4%EC%A0%95-%EA%B0%80%EC%9D%B4%EB%93%9C)
#### [하드웨어 설명](https://github.com/RoboidStudioLAB/Wiki_Image/wiki/%EB%9D%BC%EC%BF%A4-%ED%95%98%EB%93%9C%EC%9B%A8%EC%96%B4-%EC%84%A4%EB%AA%85)



<br>

---

<br><br><br><br>


# 예제 설명
- 사용자가 코드를 실행해 **미리 작성된 악보** 또는 **새롭게 작성한 악보**를 선택합니다.

  <img width="569" height="165" alt="Image" src="https://github.com/user-attachments/assets/78056e0e-83d0-4392-a9c0-40b78b0fce89" />


<br><br>

- RaccoonBot이 악보에 맞춰 이동하여 **건반을 타격**하며 실로폰을 연주합니다.

  <img width="715" height="166" alt="Image" src="https://github.com/user-attachments/assets/237277ba-68a3-42e8-8a9b-6d395765a971" />


<br><br>

---

<br><br><br><br>


# 준비물 및 방법

### 준비물
- RaccoonBot
- 실로폰용 말단 장치, 실로폰
- PC (Windows 권장)
- Block Composer, Raccoon_Play_Xylophone.block 파일

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
