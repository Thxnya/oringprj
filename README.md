# 컴퓨터 비전 AI 기반 오링 불량 판정 모델 개발

https://github.com/Thxnya/oringprj<br>



📰 프로젝트 개요<br/>
---
이번 프로젝트의 목적은 두가지입니다. <br>
이미지 분류 딥러닝 알고리즘을 앙상블 형태로 활용하여 불량 판정 정확도를 높이고, <br>
사용자가 실시간으로 간편하게 불량을 판정할 수 있는 어플리케이션을 개발해보려고 합니다.<br>
<br>
오링은 부속과 부속 사이에 틈을 막아주는 역할을 합니다.<br>
목적에 맞게 재질과 규격을 면밀하게 설계하여 사용해야하는 부속입니다.<br>
지금 산업에서 AI를 활용하여 불량을 판정하더라도 완벽하지 않고 잘못 판정하는 경우가 있습니다. <br>
그렇기 때문에 사람이 한번 더 확인해야하는 번거로움이 있으며,<br>
사람이 직접 확인해도 구별하기 힘든 불량이 존재합니다.<br>
이런 불편함을 개선할 수 있는 솔루션을 개발하고자 합니다.<br>



💬 프로젝트 1차 결론<br/>
---
처리시간의 경우엔 YOLOv5가 Mask R-CNN의 1/5정도로 매우 빠른 것으로 나타났지만 <br/>
Mask R-CNN이 정확도가 더 높게 나타날 것이라고 예상한 것과는 달리 두 알고리즘 모두 성능이 우수한 모델이며 <br/>
YOLOv5의 경우 정확도가 조금 더 높은 것으로 나타났습니다.<br/>
<br/>
YOLOv5의 경우 정상과 불량의 판정 정확도가 높으면서 처리속도가 빠르고, <br/>
Mask R-CNN의 경우 객체 사이의 경계를 분할해주는 성능이 높다는 각 알고리즘의 장점을 활용하여,<br/>
YOLOv5는 정상과 불량 두가지 클래스로만 나눠서 실시간으로 판정하도록 하고 <br/>
Mask R-CNN의 경우 불량인 영역만 학습하여 YOLOv5가 불량으로 판정한 데이터에 대해서만 오링의 불량 카테고리를 판정하는데 사용합니다. <br/>
<br/>
발생하는 불량의 카테고리마다 원인이 조금씩 다를 것이라고 생각합니다.<br/>
판정 모델을 통해서 데이터가 수집되고 추세가 나타나면 <br/>
오링을 생산하는데 어떤 문제가 생겼는지 그리고 미래에 어떤 문제가 생길지도 알 수 있을 것이라고 생각합니다.<br/>



⚡ 발표 자료<br/>
---
