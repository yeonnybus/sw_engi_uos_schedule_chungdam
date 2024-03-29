# 소프트웨어공학 Mobile Robot Controller Project

------------------
지도는 재난 지역을 추상화한 모델이다. 지도는 2차원 좌표공간(단, x, y 좌표는 각각 0 또는 자연 수 값만 가질 수 있다.)으로 구성되며 각 좌표를 지점(spot)이라고 칭한다. 지도상의 한 지점에 위 험물이 존재하면 그 지점은 위험 지점이라고 부르고, Color blob이 발견되면 그 지점은 중요 지점 이라고 부른다. 지도는 불완전하다. 즉 지도상의 한 지점에 위험 지점이라는 표시가 없더라도 실 제로는 위험 지점일 가능성이 있다. ADD-ON은 오퍼레이터로부터 지도를 얻는다.
hazard sensor는 로봇의 전방 1칸 앞이 위험 지점인지를 판별하는 센서이다.
color blob sensor는 로봇의 전후 좌우 1칸이 각각 중요 지점인지를 판별하는 센서이다. positioning sensor는 로봇의 지도상 좌표 위치를 나타내주는 센서이다.
ADD-ON은 SIM으로의 호출을 통해서 센서들의 값을 얻을 수 있다고 가정한다.


요구사항은 다음과 같다.
> 1. 입력형식:
  Map: (4 5) // 지도 크기
  Start: (1 2) // 시작 위치
  Spot: ((4 2)(1 5)) // 탐색 위치
  Hazard: ((1 0)(3 2)) // 위험 지점
 
> - 프로그램 실행 도중에 일시 정지하고 음성인식으로 중요(color blob)/위험(hazard) 지점 생성

> 2. 출력 결과
 지도를 표시하고 로봇과 미리 정해진 탐색위치, 위험지점 표시
 탐색 위치를 향해 로봇이 이동하는 모습을 표시하고 도중에 중요/위험 지점을 생성하고 발견하여 다시 경로 계산하여 이동
 최종적으로 모든 탐색 위치를 방문

------------------
