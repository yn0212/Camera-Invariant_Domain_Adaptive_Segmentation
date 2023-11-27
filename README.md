# Camera-Invariant_Domain_Adaptive_Segmentation
카메라 특성 변화에 강인한 Domain Adaptive Semantic Segmentation 알고리즘 개발
[배경]
자율주행은 다양한 센서들을 사용해 주변 상황을 인식하고 이를 바탕으로 차량을 제어하게 됩니다. 

카메라 센서의 경우, 장착 위치, 센서의 종류, 주행 환경 등에 따라 영상간의 격차(Domain Gap)가 발생합니다. 

그간 여러 선행 연구에서는 이미지의 광도와 질감(Photometry and Texture) 격차에 의한 인식 성능 저하를 극복하기 위해, 

Unsupervised Domain Adaptation 기술을 광범위하게 적용해왔습니다. 

하지만 대부분의 기존 연구들은 카메라의 광학적 특성, 

특히 이미지의 왜곡 특성(Geometric Distortion)에 따른 영상간의 격차는 고려하지 않고 있습니다. 

따라서 본 대회에서는 왜곡이 존재하지 않는 이미지(Source Domain)와 레이블을 활용하여, 

왜곡된 이미지(Target Domain)에 대해서도 고성능의 이미지 분할(Semantic Segmentation)을 수행하는 AI 알고리즘 개발을 제안합니다.


[주제].
카메라 특성 변화에 강인한 Domain Adaptive Semantic Segmentation 알고리즘 개발

![image](https://github.com/yn0212/Camera-Invariant_Domain_Adaptive_Segmentation/assets/105347300/ddc9fa81-57d7-4c2a-bcd8-415fdc3dc652)

[설명]
왜곡이 없는(Rectilinear Source Domain) 이미지와 대응되는 레이블 정보를 활용하여, 

레이블이 존재하지 않는 왜곡된 영상(Fisheye* Target Domain)에서도 

강인한 이미지 장면 분할(Semantic Segmentation) 인식을 수행하는 알고리즘 개발

* Fisheye: 200도의 시야각(200° F.O.V)을 가지는 어안렌즈 카메라로 촬영된 이미지
![image](https://github.com/yn0212/Camera-Invariant_Domain_Adaptive_Segmentation/assets/105347300/1d03aca5-6f93-4149-9cba-d58fdb88871d)



1.회색 블록 -_resnet50_unet_fish_eye_seg2.ipynb
![image](https://github.com/yn0212/Camera-Invariant_Domain_Adaptive_Segmentation/assets/105347300/acc273cb-c853-4662-bd36-cdf57c0bcabe)

-fish eye transform augmentation 위주 모델 최적화 알고리즘 설계 및 ensemble

2. uda 기법 공부
![image](https://github.com/yn0212/Camera-Invariant_Domain_Adaptive_Segmentation/assets/105347300/5b2adb7c-33cd-447d-9829-47989cae3b6a)

daformer참고 논문 : https://arxiv.org/abs/2111.14887
mic 참고 논문: https://arxiv.org/abs/2212.01322


결과 영상(1학년(70명),2학년,3학년 앞 발표- 이해하기 쉽게 제작)


https://github.com/yn0212/Camera-Invariant_Domain_Adaptive_Segmentation/assets/105347300/458b614b-11e3-4590-a30e-3885d9aed3bf



