# SNS
각 커뮤니티 별 정치인 선호도 조사

// 주피터랩 사용하기 위한 과정
주피터랩 설치 -> cmd에 "pip install jupyter lab" 사용 -> 오류 발생 long path 오류 -> 레지스트리 편집기 진입 -> HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem 경로들어가기 -> "LongPathsEnabled"을 0에서 1로 변경
시스템 속성 -> 환경 변수 -> 사용자 변수 path ->jupyter-lab 파일 존재하는 경로 설정

// 주피터랩에 존재하는 코드 사용하기 위해 준비할 것
// cmd 창을 키고 해당 코드 복사 붙여넣기 한다.
python3 -m pip install selenium
python3 -m pip install openyxl
python3 -m pip install webdriver_manager
python3 -m pip install pandas
python3 -m pip install tqdm

// 파일 사용법
Train,Test 데이터 -> 실제 Train하고 Test한 데이터가 있는 공간으로 실제는 github를 참조하여 쓰기 때문에 확인만 할 것

결과 추출 코드 -> 개별연구_trained.ipynb를 실행하면 바로 사용가능하다. 이때 결과를 보기 위해서 txt파일이 존재해야 하는데 해당 파일은 크롤링 코드를 사용하여 txt 파일을 만들고 해당 폴더로 옮기면 사용가능하다. 혹은 해당 텍스트 파일이 존재하는 경로를 지정해도 된다.

머신러닝 코드 -> 개별연구.ipnyb를 실행하면 전처리, 기계학습, 결과 분석을 모두 실행한다. 그러나 해당 코드는 사용할 때마다 시간이 오래 걸리기에 결과 추출 코드를 사용할 것

크롤링 -> 해당 코드는 위의 머신러닝을 활용하여 해당 사이트가 어느 정치인을 선호하는 가를 나타내기 위해 글을 크롤링하는 코드이다. 보배드림, 클리앙,DC, 일베, 엠팍이 있으며 해당 코드를 실행하면 analysis_사이트_정치인.txt 파일이 생성된다. 해당 폴더에서 얼만큼 크롤링을 하는지 설정하냐에 따라 Train,TEST에 데이터를 넣을 수도 있고, 마지막 결과를 위한 데이터로 사용할 수도 있다.
