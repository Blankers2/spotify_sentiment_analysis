# 개요
- AI 허브
    - https://aihub.or.kr/aihubdata/data/view.do?dataSetSn=271

    - 감정의 종류
        - 행복/중립/슬픔/공포/혐오/분노/놀람

    - 일반적 추천시스템
        - 초기 서비스
            - 랜덤 추천
        - 서비스가 데이터가 구축이 되가면
            - 회원들의 행동 데이터 저장 -> 군집 진행 -> 회원의 유형 -> 유형에서 자주 재생/판매 제품을 정리
            - 회원가입 -> 분석에 필요한 최소 정보 획득 -> 특정 군집 그릅에 배치 -> 추천 서비스 진행
            - 회원의 이용 데이터 + 군집그룹 -> 맞춤형으로 추천 서비스 제공
        - 추천 서비스
            - 사이트/서비스에 오래 머물면서 이용 -> 광고/구매 등등 행동이 이어진다 -> 매출극대화

    - 본 노트에서는 감정 분석 결과를 구축한 음원 데이터에 대비
        - 감정선에 적절한 음원을 제공하는 방식 연결
        - 감정과 음원을 연결하는 부분은 노트의 핵심은 아님

# 스포티파이
- 음원 스트리밍 서비스 회사
- 음악서비스
    - 앨범-유통
    - 음원-유통
- 음원 데이터및 음원 자체 정보 이용
    - https://developer.spotify.com/
        - 로그인 - 회원가입 - 로그인 진입가능
        - 계정 - 클릭 - 대시보드 - 클릭
        - 약관동의 및 이메일 인증 관련 버튼
            - 체크, 버튼 클릭 -> 가입한 이메일로 인증 메일 제공
            - 메일 체크 - 인증 -> 본화면에서 새로고침 -  "create app 버튼 활성화됨"
    - create app
        - 정보입력
        - save 버튼 클릭 -> 최초 계정은 5분 정도 텀이 생길수 있음
     

![image](https://github.com/user-attachments/assets/6337f7b0-e6c0-4f37-ba1a-dac9a8e77de1)
- 레이더 차트를 통해서 BTS 곡 이 비슷한 양상을 보였다
    - 샘플 2개 기준, 데이터가 많으면 달라질수 있음
    - 인감의 감정
        - 7단계 정리
            - 연속적이 값으로 표현 가능한가?
                - 인사이트부족
            - 연속적이라는 가정 진행
                - 공포 < 혐오 < 분노 < 슬픔 < 중립 < 놀람 < 행복
        - 음원의 valence
            - (우울)0 ~ 1(행복)
