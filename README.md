# rescueRCCAR

![image](https://user-images.githubusercontent.com/62790857/147813726-d319e615-44d9-4e52-b3b4-ec74aead9a94.png)
1. 차에 전원을 인가하면 자동으로 통신을 시작한다. 데이터 수신용 모듈에도 전원 인가 시 양 측에 연결한 nRF24l01 모듈을 통하여 LoRa 방식으로 통신한다.


![image](https://user-images.githubusercontent.com/62790857/147813739-0f23ad43-49ea-420c-a849-ddddc0667a56.png)
2. GPS 신호가 감지되면 다음과 같이 GPS 데이터를 수신하고 그 값을 nRF24l01 모듈이 받아와 출력한다. 기본 코드에서 추가 수정을 하여, 인지하기 쉽고 지도와 연계하기 쉽게 위도, 경도만
나오게 코드를 수정하였습니다.

![image](https://user-images.githubusercontent.com/62790857/147813749-a42e02f9-3af8-4a95-a837-108477011995.png)


3. 원격 모듈이 무선 LAN 네트워크 망에 연결되었다면 ov2640 카메라가 촬영한 영상을 원격으로 출력한다. 현재는 카메라가 사람을 찍고있는 모습입니다.


![image](https://user-images.githubusercontent.com/62790857/147813757-dd4e377a-d966-46eb-8ed9-8bb7a1a0f934.png)


4. 영상과 더불어 위도,경도 값을 통해 GPS 모듈에서 받아온 정보를 토대로 모듈의 위치가 구체적으로 어디 있는지 특정할 수 있다.


![image](https://user-images.githubusercontent.com/62790857/147813761-f398ced8-b305-4376-8d72-be8122d52509.png)


5. 만약 조도센서의 값이 일정이하로 떨어지게 된다면, 카메라 식별이 불가하므로 인체감지센서를 이용해 식별을 하게 됩니다.  



GPS의 값을 그냥 받게되면,


![image](https://user-images.githubusercontent.com/62790857/147813803-12f54059-4b9e-4fe5-b9b5-69801565506b.png)



위와 같은 표처럼 필요하지 않은 값들이 함께 출력되므로, 첫 번째 코드를 이용해 위도, 경도 값만 나오게 코딩하였습니다.



![image](https://user-images.githubusercontent.com/62790857/147813810-e5f4916f-100a-40fc-8fce-afc55b4ec06a.png)
