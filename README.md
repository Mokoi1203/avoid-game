# Survivor

아이디어 노트

-> 장르 : 쿼터뷰 시점의 피하기 게임

-> 게임의 진행 방식 : 게임이 시작되면 플레이어를 향해 동서남북 + 4가지 대각선 방향에서 총알이 날아오게 되는데, 
   방향키로 플레이어를 조작해 사방에서 날아오는 총알을 피해가며 플레이어를 가능한 한 오래 동안 생존시키고,
   플레이어가 탄알에 맞아 왼쪽 하단에 배치되어있는 플레이어의 HP가 전부 달면 게임이 끝나는 방식이다.
   (발사기의 경우 실제 게임에서는 몬스터 프리팹을 발사기로 사용해서 몬스터가 탄알을 발사하도록 설정하였다)
   
-> 플레이어의 애니메이션 : Walk, Idle

-> 플레이어에 대한 설명 : 게임을 시작했을 경우 조작하게 되는 플레이어블 캐릭터.
   WASD로 상하좌우 이동을 할 수 있으며, 이 오브젝트에 탄알이 적중할 경우 플레이어가 10 데미지를 받는다.
   플레이어의 최대 HP는 100으로 설정되어 있음.

-> 스테이지에 대한 설명 : 스테이지(게임 시작 시 플레이어가 보이게 되는 화면)은 원형 판으로 이루어져 있으며,
   게임을 플레이하는 사람이 게임에 재미를 느끼고 게임을 플레이하는데에 있어 긴장감을 심어주기 위해서 일정한 속도로 바닥이 회전하도록 되어있다.
   
-> 생존 시간에 대한 설명 : 현재 플레이어가 생존한 시간은 게임 화면 맨위에 표시되며, 현재 최장 생존 시간을 표시하고
   만약 게임을 한번도 플레이하지 않았다면 0으로 표시된다. (1이라면 1초 생존이라는 개념)
   또한 플레이어가 오랫동안 생존을 하면 할수록 그에 반영하여 실시간으로 생존 시간이 갱신된다.
   
-> 탄알에 대한 설명 : 발사기에서부터 생성되어 플레이어를 표적으로 노려서 날아온다.
   게임 내 시간으로 약 10초가 지나거나, 플레이어에게 적중했을 경우 사라지며 탄알 하나당의 데미지는 10으로 설정되어 있음.
   
-> 발사기에 대한 설명 : 플레이어를 향해 탄알을 발사하는 발사기. 보라색 몬스터의 프리팹을 사용했으며 바닥의 회전에 연동되어 있기에
   바닥과 함께 돌아간다. 탄알을 생성하는 방식은 탄알의 최근 생성 시점에서부터 누적된 시간이 생성 주기보다 크거나 같다면 
   누적된 시간을 리셋 후 생성-> 발사하는 방식이며, 탄알의 생성 주기는 약 3~4초 정도. 
   탄알이 자연적으로 사라지는 데는 게임 시간으로 약 10초가 걸린다.
