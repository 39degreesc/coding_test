# Coding Test Guidelines

(주)삼십구도씨 개발자 채용을 위한 코딩 과제 안내입니다.

삼십구도씨에서는 지원자님의 개발 스타일을 파악하기 위한 과제를 진행합니다.

제출하신 코드의 리뷰 후 면접진행 여부가 결정됩니다.

# 요구사항

[LINK](https://drive.google.com/file/d/17CXfMH36M9Wk2ktUpvnlZzi8He67Msj3/view?usp=sharing)

- 위 영상을 참고해서 지역별 날씨를 보여주는 어플리케이션을 동일하게 구현해주세요.
- 지역 이름에 ***"se"***가 포함된 지역을 대상으로 오늘, 내일 날씨를 보여줍니다.
- 날씨 정보는 지역 이름, 날씨 아이콘, 날씨 요약, 현재 온도, 습도로 구성됩니다.

# API

- [https://www.metaweather.com/api/](https://www.metaweather.com/api/) – MetaWeather의 Open API를 사용해주세요.
    1. **Location Search** - /api/location/search/?query=(query)를 사용해서 검색어 ***"se"***로 검색되는 지역 목록을 반환받습니다.
    2. **Location** - /api/location/(woeid)/를 사용해서 각 지역별 날씨 정보를 반환받습니다.

        consolidated_weather 필드의 하위 필드를 사용해서 각 날씨를 구성해 주세요.

|name|desc|
|:--:|:--:|:--:|--:|
|weather_state_name|날씨 요약|
|weather_state_abbr|아이콘 이미지 정보|
|the_temp|현재 날씨|
|humidity|습도|

# 개발 환경

- **언어** – Java, Kotlin, Swift
- **라이브러리** – 어떤 라이브러리를 사용하셔도 무방합니다.

# 제출

- 6**일 이내 제출** – 공휴일 상관없이 월요일에 안내를 받으셨으면 그 다음주 일요일까지 제출해주세요.
- **지원자님의 Git Repository로 공유** – 과제는 지원자님의 공개 Repository에 올려서 URL을 공유해주세요. Github, Gitlab 등 어떤 공간이라도 좋습니다.
- ninyess@39degreesc.com – Repository URL을 이메일로 제출해주세요.
- 일정 내 완성하지 못하셨더라도 개발된 부분까지 제출해주세요.

# 문의

- ninyess@39degreesc.com – 과제 진행 중 궁금하신 점은 이메일로 문의해주세요.
