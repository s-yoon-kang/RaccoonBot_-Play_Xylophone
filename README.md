# [Play Xylophone]

**해당 문서는 Raccoon의 테스트 예제 설명 문서입니다.**


***

#### [하드웨어 설명](https://github.com/RoboidStudioLAB/Wiki_Image/wiki/%EB%9D%BC%EC%BF%A4-%ED%95%98%EB%93%9C%EC%9B%A8%EC%96%B4-%EC%84%A4%EB%AA%85)

#### [블록 컴포저 바로가기](https://rbmate.com/BlockComposer/)
  
#### [로보메이션 깃허브 바로가기](https://github.com/RobomationLAB)

#### [초보자를 위한 블록컴포저 환경설정 가이드](https://github.com/RoboidStudioLAB/Wiki_Image/wiki/%EB%B8%94%EB%A1%9D%EC%BB%B4%ED%8F%AC%EC%A0%80-%ED%99%98%EA%B2%BD-%EC%84%A4%EC%A0%95-%EA%B0%80%EC%9D%B4%EB%93%9C)

***


Raccoon이 악보에 맞춰 실로폰을 연주하는 예제입니다.
<br>
예제는 **악보**, **시작 위치 이동**, **건반 타격**, **음 각도 이동** 기능으로 동작합니다.
<br>

  ![Image](https://github.com/user-attachments/assets/aaa006e5-696c-4288-a1c9-60a6f7f0ba4b) ![Image](https://github.com/user-attachments/assets/aaa006e5-696c-4288-a1c9-60a6f7f0ba4b) ![Image](https://github.com/user-attachments/assets/aaa006e5-696c-4288-a1c9-60a6f7f0ba4b)

 
<br><br>


---


## 1. 준비물

[*예제 파일 다운로드*](https://www.dropbox.com/scl/fi/dem00dxin36kr2swu5nua/Raccoon_Play_Xylophone.block?rlkey=x1cep88nr1uao4uf5201evc5i&st=5wkuhvfn&dl=0)

| 제품명(수량) | 이미지 | 제품명(수량) | 이미지 |
| :---: | :---: | :---: | :---: |
| Raccoon<br> (1개) | <img width="200" alt="Image" src="https://github.com/user-attachments/assets/6aed75da-3092-4295-9ef7-e8956efa5bae" /> | 실로폰용 말단 장치<br> (1개) | <img width="200" alt="Image" src="https://github.com/user-attachments/assets/f94e3aae-e7ef-447d-921e-71b026d86c87" /> |
| 실로폰<br> (1개) | <img width="200" alt="Image" src="https://github.com/user-attachments/assets/dba46449-236b-4273-bb72-1256359cb4c0" /> | Block Composer | <img width="200" alt="Image" src="https://github.com/user-attachments/assets/f06909aa-91f6-4f47-8c4d-2a0044d99c49" /> |

<br><br>


---


## 2. 초기 환경 구성
- Raccoon의 **대시보드**를 켜 **각도 제어 모드**로 변경합니다.

  <img width="1000" alt="Image" src="https://github.com/user-attachments/assets/df8ecab3-8739-4bff-9cb5-9d45cdd1442d" />

<br>

  <img width="1000" alt="Image" src="https://github.com/user-attachments/assets/8b0bb1a2-43db-44fe-95b2-7d1e80c83565" />


<br><br>

- RaccoonBot의 각도를 위에서부터 **21, -65, -52, 0**으로 설정하여 **실로폰 연주 준비 자세**로 이동합니다.

  <img width="1000" alt="Image" src="https://github.com/user-attachments/assets/91f98b82-1757-4f7c-b0d1-4b24a3577e6a" />

<br>

  <img width="500" alt="Image" src="https://github.com/user-attachments/assets/628d7508-d10e-4e88-a380-71196ccd79e4" />


<br><br>

- RaccoonBot의 **실로폰 연주 준비 자세**에 맞춰 **말단 장치 끝** 부분이 실로폰의 **가운데 건반 바깥쪽**에 오도록 배치합니다.
  
  <img width="500" alt="Image" src="https://github.com/user-attachments/assets/f03301e8-6af5-42c8-a1f1-5427d3efa00b" />


<br><br>

- 이후 RaccoonBot의 **말단 장치 끝** 부분을 건반마다 위치시키고 **Joint 1번의 각도**를 확인하고 기록합니다.

  ![image](https://github.com/user-attachments/assets/7c0af05e-3e12-4c50-9b51-6e42bec4b83a)

<br>

  <img width="1000" alt="Image" src="https://github.com/user-attachments/assets/16d1d24a-2812-4023-bd61-98b164ef8a3c" />


<br><br>

- 기록한 **Joint 1번의 각도**를 음에 맞춰 **각도값**을 수정합니다.

  <img width="400" alt="Image" src="https://github.com/user-attachments/assets/50ffca25-58e8-4798-9315-8fd4f1973e63" />


<br><br>

### 악보 작성 방법

- **시작하기():** 의 아래 **if문** 하나를 복사하여 아래 붙여넣습니다.

  <img width="400" alt="Image" src="https://github.com/user-attachments/assets/d9966f64-3c63-4340-bbac-873243735cf7" />


<br><br>

- **song = "노래제목"** 을 수정하고 아래 축소된 블록을 **확장**하여 악보를 작성합니다.

  <img width="400" alt="Image" src="https://github.com/user-attachments/assets/7f5683d2-3afd-40a4-9aa1-29092f3e7801" /> <img width="400" alt="Image" src="https://github.com/user-attachments/assets/2f8c9861-eac3-4434-82b7-9a8248786fdd" />


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


## 3. 작동하기
- 오른쪽 위 **실행 버튼**을 클릭합니다.

  <img width="1000" alt="Image" src="https://github.com/user-attachments/assets/e29aa02b-faec-418b-9f47-a35e5e69cdf1" />


<br><br>

- 사용자가 코드를 실행해 **미리 작성된 악보** 또는 **새롭게 작성한 악보**를 선택합니다.

  <img width="1000" alt="Image" src="https://github.com/user-attachments/assets/27057df5-add4-470b-b4bb-6389b5673905" />


<br><br>

- RaccoonBot이 악보에 맞춰 이동하여 **건반을 타격**하며 실로폰을 연주합니다.

  ![Image](https://github.com/user-attachments/assets/aaa006e5-696c-4288-a1c9-60a6f7f0ba4b)


<br><br>


---


## ~~4. 오류 발생시 해결 방법~~
- ~~발생 가능한 오류에 대해서 적어두는 란 입니다.~~

<br><br>


---


## 5. 작동 알고리즘
- 사용자에게 **노래 제목**을 입력 받아 **악보**를 설정합니다.

  ![Image](https://github.com/user-attachments/assets/6ed30607-a020-4848-8e18-5a507c430fd7)


<br><br>

- **'start', 'swing' 변수**에 따라 Raccoon의 **속도 설정**을 **무한 반복**합니다.

  ![Image](https://github.com/user-attachments/assets/a08506e5-b031-474d-a718-198b887dc7d9)


<br><br>

- **연주 시작 함수**를 통해 **시작 위치 이동** -> **건반 타격(위치 이동, 타격)** 을 **악보 길이만큼 반복**합니다.

  ![Image](https://github.com/user-attachments/assets/64b43523-0029-4f8f-884a-7ff68d8158fa)


<br><br>

- 연주가 완료되면 **'start' 변수**를 **0**으로 설정해 정지합니다.

  ![Image](https://github.com/user-attachments/assets/9fbf6fa9-cc88-44ee-9685-33c0c4a606e1)


<br><br>

---


## 6. 코드 설명
<details>
<summary><b>시작하기():</b></summary>
    
- 사용자에게 원하는 노래의 **제목**을 입력 받아 **'song' 변수**에 저장합니다.

  ![Image](https://github.com/user-attachments/assets/22d36f5c-1804-4f3a-8aa3-68dde65b7538)


<br><br>

- Raccoon의 **초기 설정**을 수행합니다.

  ![Image](https://github.com/user-attachments/assets/8d61e54b-9fa4-4e86-931e-04e1f3655415)


<br><br>

- **각도 제어 모드**로 Raccoon을 **초기 연주 자세**로 설정하고, **속도 제어 모드**로 변경합니다.

  ![Image](https://github.com/user-attachments/assets/4c66aa43-bd05-4378-a6ab-da03fd9c42b3)


<br><br>

- 사용자가 입력한 노래 제목 **'song'** 의 값에 따라 **악보(sheet)** 를 설정합니다.

  ![Image](https://github.com/user-attachments/assets/7de7d121-4d54-4e06-9b05-894baaaea6f2)


<br><br>

- **'연주 시작'** 함수를 통해 실로폰을 연주하고 끝나면 **'start' 변수**를 0으로 설정하여 Raccoon을 정지합니다.

  ![Image](https://github.com/user-attachments/assets/9553d7ce-b44f-4a5c-b15f-c042f9ea9f2b)

<br><br>


</details>


<br>


---


<details>
<summary><b>무한 반복하기():</b></summary>
    
    
- 만약 **'start' 변수**가 **1**이라면 **연주**를 아니라면 **정지**합니다.

  ![Image](https://github.com/user-attachments/assets/86e4d71b-2178-4006-840a-7f71d45ece59)


<br><br>

- 만약 **'swing' 변수**가 **0**이라면 **관절 3**의 **속도**를 **각도 -65(제자리로)** 까지 가도록, **1**이라면 **-75의 속도(건반 타격)** 로 설정합니다.

  ![Image](https://github.com/user-attachments/assets/28df798b-1f14-44c2-8228-bfc76fb801f6)


<br><br>

- **악보**에 따라 **코드에 저장**된 **관절 1**의 **각도**로 빠르게 이동합니다. 

  ![Image](https://github.com/user-attachments/assets/45f6c28d-b382-4b27-bbb2-f538cf65f152)


<br><br>


</details>


<br>


---


<details>
<summary><b>함수</b></summary>

<br>

<details>
<summary><i>연주 시작</i></summary>

<br>

- **'length' 변수**를 **악보(sheet)** 의 **총 문자 개수**로 설정합니다.

  ![Image](https://github.com/user-attachments/assets/2fdc464b-2123-4bbe-951e-5c0e70d7ae35)


<br><br>

- **악보(sheet)** 의 **첫 시작 음**을 **함수 '시작 위치'** 에 넣습니다.

  ![Image](https://github.com/user-attachments/assets/4eb1d061-773b-4977-a582-d7c5fc9beb55)


<br><br>

- **'length' 변수**의 길이만큼 **함수 '건반 타격'** 에 음을 순차적으로 넣고 **'i' 변수**를 **1**만큼 바꿉니다.

  ![Image](https://github.com/user-attachments/assets/4e31de7d-7847-45fa-a936-d1bb2224d771)


<br><br>

</details>

<br>

<details>
<summary><i>각도값</i></summary>

<br>

- 실로폰 계이름에 따른 **관절 1**의 **각도값**을 설정합니다.

  ![Image](https://github.com/user-attachments/assets/6d8d06ce-0e8a-4e41-9183-297cc04eabf1)


<br><br>

</details>

<br>

<details>
<summary><i>시작 위치</i></summary>

<br>

- 안정적인 시작을 위해 **악보**의 **첫 계이름 위치**로 이동 후 **1초** 기다립니다.

  ![Image](https://github.com/user-attachments/assets/5c44c5ad-e8a7-46fc-ad20-65fed12512f9)


<br><br>


</details>

<br>

<details>
<summary><i>건반 타격</i></summary>

<br>

- **'note' 변수**를 **'음' 변수(sheet의 순차적 문자)** 로 설정합니다.

  ![Image](https://github.com/user-attachments/assets/abf7c424-9c90-449a-890f-076e67d7c57b)


<br><br>

- **'note' 변수**에 따라 **기다리거나** 혹은 **건반을 타격**합니다.

  ![Image](https://github.com/user-attachments/assets/2f294ec7-5496-46b9-9830-1f01965e0c72)


<br><br>

</details>

</details>

<br>


---


## 7. 관련 내용

[P 제어 이론](https://github.com/RoboidStudioLAB/Wiki_Image/wiki/P-%EC%A0%9C%EC%96%B4-%EC%9D%B4%EB%A1%A0)

<br>

<img width="10000000" alt="Image" src="https://github.com/user-attachments/assets/aa6d40b2-2d90-4a5e-90b4-1e3049b714db" />

<br><br>
