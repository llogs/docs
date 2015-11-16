### Powerline theme 구조 정리
---

#### 참고 문서
* http://powerline.readthedocs.org/en/latest/configuration.html

#### 설정 파일의 구조

Powerline 의 설정을 제대로 완료 했다면, 보통 아래의 디렉토리에 관련 설정파일이 존재한다.
```
cd ~/.config/Powerline
```

해당 디렉토리를 살펴보면 다음과 같이 2개의 파일과 2개의 디렉토리가 있음을 확인할 수 있다.

* _colors.json_
    - 색상 이름을 위한 숫자값들이 정의 되어 있다.
    - 어떠한 이름으로 어떠한 색상이 지정되어 있는지를 확인할 수 있다.
    - 혹은 새로운 색상을 추가할 수 있다.
* _colorscheme_ (Directory)
    - Powerline 을 사용할 수 있는 모든 어플리케이션을 위한 서로 다른 컬러 스키마를 가지고 있다.
    - shell 을 위한 컬러 스키마는 colorscheme/sheel/ 아래에 있다.
* _config.json_
    - Powerline 을 위한 메인 설정파일이다.
    - Powerline 설정정보를 보기 위한 첫번째 장소라고 생각하면 된다.
    - 이 설정파일을 통해 Powerline 이 어떤 색상 테마와 테마를 각각의 어플리케이션을 위해 사용하는지 확인할 수 있다.
* _themes_ (Directory)
    - themes 는 status line 내의 정보 구조를 나타낸다. 색상을 적용하는 설정과는 전혀 상관없다.
    - Powerline 을 사용할 수 있는 모든 어플리케이션을 위한 테마를 가지고 있다.
    - shell 을 위한 테마는 themes/shell/ 아래에 있다.

#### Powerline configuration 파일 수정하기

vi ~/.config/powerline/config.json

     19         "shell": {
     20             "colorscheme": "default",
     21             "theme": "default_leftonly",
     22             "local_themes": {
     23                 "continuation": "continuation",
     24                 "select": "select"
     25             }
     26         }

나의 경우 위와 같다. 기본적으로 colorscheme 와 theme 는 모두 default 지만 git branch 출력을 위해 임시적으로 default_leftonly 로 변경한 상태다. 이 상태에서 색상을 바꾸고 싶다면 colorscheme 를 ~/.config/powerline/colorscheme/ 내의 .json 파일 중 하나로 변경하면 된다. 기본적으론 default.json 과 solarized.json 두 가지가 있다.
적용 후 별도의 과정이 필요 없이 바로 변경이 된다. solarized.json 으로 변경해 봤지만 색상이 너무 밝아 별로 마음에 들지 않아 default.json 을 변경하여 쓰기로 결정했다.

Powerline 은 아래와 같은 기본 설정 파일들을 가지고 있다.

* Main configuration
    - powerline/config.json
* Colorschemes
    - powerline/colorschemes/name.json
    - powerline/colorschemes/extension/\_\_main\_\_.json
    - powerline/colorschemes/extension/name.json
* Themes
    - powerline/themes/top_theme.json
    - powerline/themes/extension/\_\_main\_\_.json
    - powerline/themes/extension/default.json

##### Colorscheme 파일의 구조

Colorschemes 파일들은 아래의 위치에 있다.

* powerline/colorscheme/_name_.json
* powerline/colorscheme/\_\_main\_\_.json
* powerline/colorscheme/_extension/name_.json

vi ~/.config/powerline/colorscheme/default.json

```
  1 {
  2     "name": "Default",
  3     "groups": {
  4         "information:additional":    { "fg": "gray9", "bg": "gray4", "attrs": [] },
  5         "information:regular":       { "fg": "gray10", "bg": "gray4", "attrs": ["bold"] },
  6         "information:highlighted":   { "fg": "white", "bg": "gray4", "attrs": [] },
  7         "information:priority":      { "fg": "brightyellow", "bg": "mediumorange", "attrs": [] },
  8         "warning:regular":           { "fg": "white", "bg": "brightred", "attrs": ["bold"] },
  9         "critical:failure":          { "fg": "white", "bg": "darkestred", "attrs": [] },
 10         "critical:success":          { "fg": "white", "bg": "darkestgreen", "attrs": [] },
 11         "background":                { "fg": "white", "bg": "gray0", "attrs": [] },
 12         "background:divider":        { "fg": "gray5", "bg": "gray0", "attrs": [] },
 13         "session":                   { "fg": "black", "bg": "gray10", "attrs": ["bold"] },
 14         "date":                      { "fg": "gray8", "bg": "gray2", "attrs": [] },
 15         "time":                      { "fg": "gray10", "bg": "gray2", "attrs": ["bold"] },
 16         "time:divider":              { "fg": "gray5", "bg": "gray2", "attrs": [] },
 17         "email_alert":               "warning:regular",
 18         "email_alert_gradient":      { "fg": "white", "bg": "yellow_orange_red", "attrs": ["bold"] },
 19         "hostname":                  { "fg": "black", "bg": "gray10", "attrs": ["bold"] },
 20         "weather":                   { "fg": "gray8", "bg": "gray0", "attrs": [] },
 21         "weather_temp_gradient":     { "fg": "blue_red", "bg": "gray0", "attrs": [] },
 22         "weather_condition_hot":     { "fg": "khaki1", "bg": "gray0", "attrs": [] },
 23         "weather_condition_snowy":   { "fg": "skyblue1", "bg": "gray0", "attrs": [] },
 24         "weather_condition_rainy":   { "fg": "skyblue1", "bg": "gray0", "attrs": [] },
 25         "uptime":                    { "fg": "gray8", "bg": "gray0", "attrs": [] },
 26         "external_ip":               { "fg": "gray8", "bg": "gray0", "attrs": [] },
 27         "internal_ip":               { "fg": "gray8", "bg": "gray0", "attrs": [] },
 28         "network_load":              { "fg": "gray8", "bg": "gray0", "attrs": [] },
 29         "network_load_gradient":     { "fg": "green_yellow_orange_red", "bg": "gray0", "attrs": [] },
 30         "network_load:divider":      "background:divider",
 31         "system_load":               { "fg": "gray8", "bg": "gray0", "attrs": [] },
 32         "system_load_gradient":      { "fg": "green_yellow_orange_red", "bg": "gray0", "attrs": [] },
 33         "environment":               { "fg": "gray8", "bg": "gray0", "attrs": [] },
 34         "cpu_load_percent":          { "fg": "gray8", "bg": "gray0", "attrs": [] },
 35         "cpu_load_percent_gradient": { "fg": "green_yellow_orange_red", "bg": "gray0", "attrs": [] },
 36         "battery":                   { "fg": "gray8", "bg": "gray0", "attrs": [] },
 37         "battery_gradient":          { "fg": "white_red", "bg": "gray0", "attrs": [] },
 38         "battery_full":              { "fg": "red", "bg": "gray0", "attrs": [] },
 39         "battery_empty":             { "fg": "white", "bg": "gray0", "attrs": [] },
 40         "player":                    { "fg": "gray10", "bg": "black", "attrs": [] },
 41         "user":                      { "fg": "white", "bg": "darkblue", "attrs": ["bold"] },
 42         "branch":                    { "fg": "gray9", "bg": "gray2", "attrs": [] },
 43         "branch_dirty":              { "fg": "brightyellow", "bg": "gray2", "attrs": [] },
 44         "branch_clean":              { "fg": "gray9", "bg": "gray2", "attrs": [] },
 45         "branch:divider":            { "fg": "gray7", "bg": "gray2", "attrs": [] },
 46         "cwd":                       "information:additional",
 47         "cwd:current_folder":        "information:regular",
 48         "cwd:divider":               { "fg": "gray7", "bg": "gray4", "attrs": [] },
 49         "virtualenv":                { "fg": "white", "bg": "darkcyan", "attrs": [] },
 50         "attached_clients":          { "fg": "gray8", "bg": "gray0", "attrs": [] }
 51     }
 52 }
 ```


Color Scheme 구조 살펴보기


md 테스트
~~취소선~~


