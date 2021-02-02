
게임에 참여한 플레이어 객체에요. 이 기능들은 서버에서만 사용 가능해요. 
## **함수**

| **RModeServerCharacter GetCharacter()** |
| :--- |

플레이어의 캐릭터를 얻을 수 있어요. 
| **string GetPlayerName()** |
| :--- |

플레이어의 이름을 얻을 수 있어요. 
| **string GetTeamName()** |
| :--- |

플레이어가 속해있는 팀 이름을 얻을 수 있어요. 
| **int GetLifeCount()** |
| :--- |

플레이어의 남은 목숨 개수를 얻을 수 있어요. 
| **KillCharacter()** |
| :--- |

플레이어 캐릭터를 죽게 하는 함수에요. 
| **RespawnCharacter()** |
| :--- |

플레이어 캐릭터를 리스폰 시키는 함수에요. 
| **SetCheckPoint(RSpawnPoint SpawnPointObject)** |
| :--- |

플레이어의 체크 포인트를 설정할 수 있어요 (설정할 스폰 포인트 오브젝트) 
| **SetCheckPoint(RWorldObject WorldObject)** |
| :--- |

플레이어의 체크 포인트를 설정할 수 있어요 (설정할 월드 오브젝트) 
| **SetFreeCamMode(bool bFreeCam)** |
| :--- |

플레이어의 프리캠 모드 사용여부를 설정할 수 있어요. (프리캠 사용 여부) 
| **RequestFreeCam(float WaitTime)** |
| :--- |

지정된 시간이 지난 후에 플레이어의 프리캠 모드를 요청해요. (대기 시간) 
| **int GiveItem(ModeItemServer Item, int Count)** |
| :--- |

플레이어에게 아이템을 줄 수 있어요. (줄 아이템, 개수) return 인벤토리 인텍스 
| **int GiveItem(ModeItemServer Item)** |
| :--- |

플레이어에게 아이템을 줄 수 있어요. (줄 아이템) return 인벤토리 인텍스 
| **int GetInventorySize()** |
| :--- |

플레이어의 인벤토리 사이즈를 얻을 수 있어요. 
| **ClearItem()** |
| :--- |

플레이어의 아이템을 모두 제거해요. 
| **EquipInventoryItem(int InventoryIndex)** |
| :--- |

플레이어 캐릭터에 아이템을 장착시킬 수 있어요. (장착 할 인벤토리 칸) 
| **SetEnableCollisionBetweenCharacters(bool Enable)** |
| :--- |

플레이어간의 충돌 여부를 설정할 수 있어요. (충돌 여부) 
| **SetUserCollisionTypeResponse(string UserCollisionType, CollisionResponse Response)** |
| :--- |

유저가 충돌 시 발생 타입을 설정할 수 있어요. (충돌 타입 이름 설정, [Enum.CollisionResponse.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/collisionresponse)) 
| **bool HaveInventorySaveData()** |
| :--- |

저장소에 인번토리에 대한 데이터가 저장되어 있는지 확인할 수 있어요. 
| **RModeHitResult LineTrace(Vector Start, Vector Dir, float Distance)** |
| :--- |

설정된 시작 지점에서 원하는 방향으로 지정된 거리 만큼 충돌이 있는지 체크할 수 있어요. (시작 지점 Vector, 목표 지점 Vector, 거리 값) 
| **ModeItemServer GetInventoryItem(int InventoryIndex)** |
| :--- |

지정된 칸의 인벤토리 아이템을 얻을 수 있어요. (인벤토리 칸) 
| **ModeItemServer GetEquipItem(String EquipSlot)** |
| :--- |

플레이어 캐릭터가 착용중인 아이템을 얻을 수 있어요. (장착 중인 아이템 슬롯) 
# **상속받아 사용 가능한 기능들**

## **속성**

| **Parent** |
| :--- |

부모 객체를 얻을 수 있어요. 
## **이벤트**

| **ConnectChangeEventFunction(string ValueName, function FunctionName)** |
| :--- |

추가된 값이 변경 될 때 호출되는 이벤트에요. (Value 이름, 연결 함수) 

샘플 

```lua

local function ChangeCurBullet(value) 

Logger:Log(“Hello”) 

end 

 

-- Object의 "CurBullet" 라는 Value가 변경되면 ChangeCurBullet 함수에 연결 

Object:ConnectChangeEventFunction("CurBullet", LuaScriptFunction ChangeCurBullet)   

``` 
| **AddTimeEvent(String EventName, float Time, LuaScriptFunction EventFuunction)** |
| :--- |

일정 시간뒤에 연결 함수가 호출되는 이벤트를 추가해요. (추가할 이벤트 이름, 시간, 연결 함수) 
| **DeleteTimeEvent(String EventName)** |
| :--- |

등록된 시간 이벤트를 삭제해요. (삭제할 이벤트 이름) 
## **함수**

| **string GetName()** |
| :--- |

객체의 이름을 얻을 수 있어요. 
| **RModeObject GetParent(string ParentName)** |
| :--- |

이름으로 부모 객체를 얻을 수 있어요. (찾고싶은 부모 객체 이름) 
| **RModeObject GetChild(string ChildName)** |
| :--- |

이름으로 자식 객체를 얻을 수 있어요. (찾고싶은 자식 객체 이름) 
| **RModeObject GetGetSibling(string Name)** |
| :--- |

이름으로 형제 객체를 얻을 수 있어요. (찾고싶은 형제 객체 이름) 
| **List<RScriptObject> GetChildList()** |
| :--- |

자식 객체의 리스트를 얻을 수 있어요. 
| **bool IsCharacter()** |
| :--- |

캐릭터인지 확인할 수 있어요. 
| **bool IsStaticMesh()** |
| :--- |

스테틱 메시인지 확인할 수 있어요. 
| **bool IsFX()** |
| :--- |

FX인지 확인할 수 있어요. 
| **bool IsSound()** |
| :--- |

Sound인지 확인할 수 있어요. 
| **bool IsPointLight()** |
| :--- |

포인트 라이트인지 확인할 수 있어요. 
| **bool IsSpotLight()** |
| :--- |

스포트 라이트인지 확인할 수 있어요. 
| **bool IsSurfaceUI()** |
| :--- |

서피스 UI인지 확인할 수 있어요. 
| **bool IsScreenUI()** |
| :--- |

스크린 UI인지 확인할 수 있어요. 
| **bool IsItem()** |
| :--- |

아이템인지 확인할 수 있어요. 
| **bool IsNPC()** |
| :--- |

NPC인지 확인할 수 있어요. 
| **bool IsFolder()** |
| :--- |

폴더인지 확인할 수 있어요. 
| **bool IsScript()** |
| :--- |

스트립트인지 확인할 수 있어요. 
| **bool IsCollider()** |
| :--- |

Collider인지 확인할 수 있어요. 
| **bool IsWidget()** |
| :--- |

Widget인지 확인할 수 있어요. 
| **bool IsCamera()** |
| :--- |

Widget인지 확인할 수 있어요. 
| **bool IsValid()** |
| :--- |

해당 오브젝트가 유효한지 확인 할 수있어요. 
| **AddReplicateValue(string ValueName, Vector Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화가 가능한 벡터를 추가해요. (추가할 Value 이름, Vector 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
| **AddReplicateValue(string ValueName, float Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화가 가능한 실수를 추가해요. (추가할 Value 이름, float 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
| **AddReplicateValue(string ValueName, bool Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화가 가능한 bool를 추가해요. (추가할 Value 이름, bool 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
| **AddReplicateValue(string ValueName, string Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화가 가능한 문자열을 추가해요. (추가할 Value 이름, string 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
| **AddReplicateValue(string ValueName, Color Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화가 가능한 컬러를 추가해요. (추가할 Value 이름, Color 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
| **AddSaveValue(string ValueName, Vector Data)** |
| :--- |

해당 객체 저장소에 벡터를 추가해요. (Value 이름, Vector 데이터) 
| **AddSaveValue(string ValueName, float Data)** |
| :--- |

해당 객체 저장소에 실수를 추가해요. (Value 이름, float 데이터) 
| **AddSaveValue(string ValueName, bool Data)** |
| :--- |

해당 객체 저장소에 bool을 추가해요. (Value 이름, bool 데이터) 
| **AddSaveValue(string ValueName, string Data)** |
| :--- |

해당 객체 저장소에 문자열을 추가해요. (Value 이름, string 데이터) 
| **AddSaveValue(string ValueName, Color Data)** |
| :--- |

해당 객체 저장소에 칼라를 추가해요. (Value 이름, Color 데이터) 