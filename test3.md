```uml
@startuml
start
:変数weather=天気情報;
if(wearther=0)then(yes)
:快晴です;
else if(weather=1)then(yes)
:曇りです;
else if(weather=2)then(yes)
:雨です;
else(その他)
:不明です;
endif
end
@enduml
```
