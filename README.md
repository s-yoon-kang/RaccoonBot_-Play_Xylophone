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

  ![Image](https://github.com/user-attachments/assets/27057df5-add4-470b-b4bb-6389b5673905)


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
- RaccoonBot의 **대시보드**를 켜 **각도 제어 모드**로 변경합니다.
  
  ![Image](https://github.com/user-attachments/assets/df8ecab3-8739-4bff-9cb5-9d45cdd1442d)
  ![Image](https://github.com/user-attachments/assets/8b0bb1a2-43db-44fe-95b2-7d1e80c83565)


<br><br>

- RaccoonBot의 각도를 위에서부터 **21, -65, -52, 0**으로 설정하여 **실로폰 연주 준비 자세**로 이동합니다.

  ![Image](https://github.com/user-attachments/assets/91f98b82-1757-4f7c-b0d1-4b24a3577e6a)


<br><br>

- RaccoonBot의 **실로폰 연주 준비 자세**에 맞춰 **말단 장치 끝** 부분이 실로폰의 **가운데 건반 바깥쪽**에 오도록 배치합니다.
  
  <img width="500" height="500" alt="Image" src="https://github.com/user-attachments/assets/12c8777d-20ad-4e7d-983b-cd4033817549" />


<br><br>

- 이후 RaccoonBot의 **말단 장치 끝** 부분을 건반마다 위치시키고 **Joint 1번의 각도**를 확인하고 기록합니다.

  ![Image](https://github.com/user-attachments/assets/16d1d24a-2812-4023-bd61-98b164ef8a3c)


<br><br>

- 기록한 **Joint 1번의 각도**를 음에 맞춰 **각도값**을 수정합니다.

  <img width="764" height="218" alt="Image" src="https://github.com/user-attachments/assets/8f6145cb-52f2-431c-8cac-0dfb8f1fadff" />


<br><br>

## 악보 작성 방법
- **시작하기():** 의 아래 **if문** 하나를 복사하여 아래 붙여넣습니다.

  ![Image](https://github.com/user-attachments/assets/d9966f64-3c63-4340-bbac-873243735cf7)


<br><br>

- **song = "노래제목"** 을 수정하고 아래 축소된 블록을 **확장**하여 악보를 작성합니다.

  ![Image](https://github.com/user-attachments/assets/7f5683d2-3afd-40a4-9aa1-29092f3e7801)
  ![Image](https://github.com/user-attachments/assets/2f8c9861-eac3-4434-82b7-9a8248786fdd)


<br><br>

- 기능은 다음과 같습니다.
  | 표시 | 기능 |
  | --- | --- |
  | 도(C4) | **Joint 1**을 **도**에 해당하는 각도로 이동합니다. |
  | 레(D4) | **Joint 1**을 **레**에 해당하는 각도로 이동합니다. |
  | 미(E4) | **Joint 1**을 **미**에 해당하는 각도로 이동합니다. |
  | 파(F4) | **Joint 1**을 **파**에 해당하는 각도로 이동합니다. |
  | 솔(G4) | **Joint 1**을 **솔**에 해당하는 각도로 이동합니다. |
  | 라(A4) | **Joint 1**을 **라**에 해당하는 각도로 이동합니다. |
  | 시(B4) | **Joint 1**을 **시**에 해당하는 각도로 이동합니다. |
  | 또(C5) | **Joint 1**을 **또**에 해당하는 각도로 이동합니다. |
  | (띄어쓰) | **Joint 1**을 **반박자** 쉽니다. |


<br><br>

---

<br><br><br><br>


# 코드 설명
