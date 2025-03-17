# Why make this project

SLAM으로 2D Occupaied Map을 만드는 건 귀찮고 시간이 꽤나 걸리는 일이다. 맵의 크기에 따라 다른데 5분도 넘게 걸린 적이 있다. (1분 이상 ~~ )

그러나 우리의 목표는 SLAM 알고리즘의 검증이 아니라 다양한 환경에서 로봇 서비스를 제공하는 것이기 때문에 맵의 구조를 자주 변경해야 한다.

그 때마다 SLAM으로 지도를 만드는 건 너무 귀찮고 시간도 많이 걸린다.

그래서 시뮬레이션 환경이니 마치 SLAM으로 2D Occupied Map을 만든 것처럼 코드 몇줄로 동일한 결과를 만들 수 있지 않을까 하고 만들게 되었다.

(nvidia의 issac sim은 기본적으로 시뮬레이션 상에서 2D occupied map을 만드는 기능을 제공하는데 유니티는 없는 것 같음)

# How to use

1. Assets/OccupiedMapMaker 아래에 있는 OccupancyMapRangeVisualizer prefab을 씬에 배치
2. 만들고 싶은 맵의 크기 만큼 OccupancyMapRangeVisualizer의 transform의 scale 조정, 위치 조정(x,z) 라이다의 높이만큼 y 조정
3. startX, startY 조정 (마치 SLAM으로 맵 만들 때의 로봇의 시작 위치)
4. OccupancyMapRangeVisualizer에 붙어있는 OccupiedMapMaker 스크립트의 Path, filename 수정
5. 씬에서 OccupancyMapRangeVisualizer 선택 후 메뉴 탭의 OccupiedMapMaker -> MakeOccupiedMap 클릭

<p align="center">
  <img src="https://github.com/ko-ko-song/OccupiedMapMaker/assets/48386420/8c28f089-aaeb-4b9b-84f2-65bd7182934a">
</p>

## Output

- map.pgm

- map.yaml

![Image](https://github.com/user-attachments/assets/f546eb9e-1d92-4714-ba13-db39ab9098eb)

<br>

## Unity 초보자를 위한 package Export,Import 방법

OccupancyMapRangeVisualizer.prefab 우클릭

Export Packages... 클릭

![Image](https://github.com/user-attachments/assets/278a2222-9081-4767-8a32-f0c5b855bddd)

Include dependenciese 체크

Export...클릭

![Image](https://github.com/user-attachments/assets/c7980271-569a-4392-b35f-85b58b489bc3)

다른 프로젝트에서 Asset 빈 공간 우클릭

Import Packages -> Custom Package ...

저장한 package 불러오기

![Image](https://github.com/user-attachments/assets/7af2cad8-6d7c-4360-83dd-55aa99b4d293)
