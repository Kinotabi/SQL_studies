# SQL_studies
SQL 연습을 위한 repository

기초적인 SQL 문법부터 반복해서 배우고 실험해보기

※ SQLite 기반
* 각각의 예시 데이터세트
* 1. PISA 데이터세트
    - output_cluster : 국제학업성취도 자료인 PISA를 가공하여 학생들을 ICT 사용 수준과 ICT 사용 환경이 좋은 정도로 두 축을 구성해
                       만든 예제 테이블
                       
                       CNTRYID : 국가 고유 번호, VARCHAR FK
                       CNT	: 국가 이니셜 3글자, VARCHAR FK
                       CNTSCHID	: 학교 고유 번호, VARCHAR FK
                       CNTSTUID	: 학생 고유 번호, VARCHAR PK
                       ICTENV	: 학생의 ICT 사용 수준. 값이 클수록 사용을 많이 함. INT
                       ICTUSE	: 학생이 속한 환경 내에서 ICT 기술 사용이 자유로운 정도 (예: 컴퓨터가 많은가? 태블릿을 갖고 있는가?), INT
                       cluster : 클러스터링된 결과. 0과 1로 나뉘어 있음. VARCHAR
                       
    - ict_test_countries : 위 데이터세트에서 일부 국가들만 선정하여 ICT와 관련된 변수들을 선별한 테이블
 
                           CNTRYID : 국가 고유 번호, VARCHAR FK
                           CNT	: 국가 이니셜 3글자, VARCHAR FK
                           CNTSCHID	: 학교 고유 번호, VARCHAR FK
                           CNTSTUID	: 학생 고유 번호, VARCHAR PK
                           OECD	: OECD 국가 여부, 0은 아니오, 1은 예, VARCHAR
                           ENTUSE	: 엔터테인먼트 목적의 ICT 사용 수준. 값이 높을 수록 높음. INT
                           HOMESCH : 집 안에서의 ICT 사용 수준. 갚이 높을 수록 높음. INT
                           USESCH   : 학교 내에서의 ICT 사용 수준. 값이 높을 수록 높음. INT
                           INTICT	: ICT에 대한 학생의 흥미 수준. 값이 높을 수록 높음. INT
                           COMPICT : ICT에 대한 학생의 역량 수준. 값이 높을 수록 높음. INT
                           AUTICT	: 응답자 본인이 생각하기에 ICT를 얼마나 다룰 수 있는지. 값이 높을 수록 높음. INT
                           SOIAICT : 사교적 상황에서 ICT를 언급하는 정도. 값이 높을 수록 높음. INT
                           ICTCLASS	: 학교 교실 안에서 수업 중에 ICT를 활용하는 정도. 값이 높을 수록 높음. INT
                           ICTOUTSIDE : 학교 교실 바깥에서 교과목 공부를 위해 ICT를 활용하는 정도. 값이 높을 수록 높음. INT
                           
* 2. Boston University COVID-19 Sleep 데이터세트 : Boston University에서 COVID-19 시기의 수면의 질을 연구하기 위하여
                                                구축한 데이터세트. 매일, 혹은 하루에 수 회 측정된 자료로 구성되어 있다.
                                                고유 응답 ID, 조사 시간, 우울감, 심리적 요인 등을 폭넗게 조사된 DB이다.

    - daily_survey : 설문 데이터 테이블
    - demographic_survey : 참여자의 인구통계학적 변인 테이블
                                                
