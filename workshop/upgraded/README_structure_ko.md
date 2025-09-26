# upgraded 폴더 구조 설명

`upgraded` 폴더는 레거시(`legacy`) 폴더의 전체 파일과 디렉터리 구조를 그대로 복사한 폴더입니다. 각 구성 요소는 다음과 같습니다:

- `MANIFEST.in`: 패키징 시 포함할 파일 목록을 지정하는 설정 파일
- `README.rst`: 프로젝트 설명 문서
- `distribute-0.6.10.tar.gz`, `distribute_setup.py`: 레거시 Python 패키징 도구 관련 파일
- `setup.py`: 프로젝트 설치 및 배포를 위한 스크립트
- `docs/`: 프로젝트 문서화 관련 디렉터리
    - `build/`: Sphinx로 빌드된 문서 결과물
        - `doctrees/`: Sphinx 문서 빌드 중간 파일
        - `html/`: HTML 문서 결과물 및 정적 파일
    - `source/`: Sphinx 문서 소스
        - `_static/`: 사용자 정의 CSS 등 정적 파일
        - 여러 `.rst` 문서와 `conf.py` 설정 파일
- `guachi/`: 프로젝트의 주요 Python 패키지
    - `__init__.py`, `config.py`, `database.py`: 핵심 모듈
    - `tests/`: 단위 및 통합 테스트 코드
        - `test_configmapper.py`, `test_configurations.py`, `test_database.py`, `test_integration.py`
- `guachi.egg-info/`: 패키지 메타데이터 정보
    - `PKG-INFO`, `SOURCES.txt`, `dependency_links.txt`, `top_level.txt`

이 폴더는 레거시 프로젝트를 최신 Python 환경으로 업그레이드하기 위한 작업 공간으로 활용됩니다. 각 파일과 디렉터리는 기능별로 분리되어 있어, 코드 수정, 테스트, 문서화, 패키징 등 다양한 작업을 독립적으로 진행할 수 있습니다.