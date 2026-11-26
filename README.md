# RoboVisionAi
VLM 기반 배송 로봇 주변 환경 이미지 분석 웹 애플리케이션

1. 프로젝트 소개

Python과 OpenAI VLM API를 활용하여 배송 로봇 주변 환경 이미지를 분석하는 웹 애플리케이션이다.

이미지를 업로드하면 사람, 장애물, 출입문, 통로 등의 주요 요소를 식별하고 주변 상황을 한국어로 설명한다.

2. 주요 기능

* JPG, JPEG, PNG 이미지 업로드 및 미리보기
* OpenAI VLM API 기반 이미지 분석
* 사람, 장애물, 출입문, 통로 등 주요 객체 식별
* 분석 결과 한국어 설명 및 JSON 구조화
* 분석 기록 로컬 JSON 파일 저장
* API 및 이미지 처리 오류 예외 처리

3. 기술 스택

* Python
* Streamlit
* OpenAI Vision API
* Pillow
* python-dotenv
* JSON

4. 실행 방법

① GitHub 저장소 다운로드

git clone https://github.com/bradipi977-sys/RoboVisionAI.git
cd RoboVisionAI

② 라이브러리 설치

pip install -r requirements.txt

③ API 키 설정

.env.example을 참고하여 .env 파일을 생성하고 OpenAI API 키를 설정한다.

④ 애플리케이션 실행

streamlit run app.py

5. 보안 및 유의사항

* API 키는 환경변수로 관리한다.
* 이미지에 없는 객체를 임의로 생성하지 않도록 프롬프트를 설계한다.
* 객체의 존재 여부가 불확실하면 ‘확인 불가’로 표시한다.
* 본 프로젝트는 이미지 분석용 샘플이며 실제 로봇 제어 및 안전 판단에 사용하지 않는다.
* OpenAI API 사용 시 별도의 이용 요금이 발생할 수 있다.

6. 테스트

pytest

분석 결과 처리 및 데이터 구조 검증을 위한 기본 테스트를 수행한다.

7. 라이선스

MIT License
