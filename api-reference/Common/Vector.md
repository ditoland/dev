# **Vector**

## **생성자**

| **Vector.new(number X, number Y, number Z)** |
| :--- |
| **Vector를 X, Y, Z 좌표를 세팅해서 생성한다.** |

| **Vector.new(number Value)** |
| :--- |
| **Vector를 X, Y, Z 좌표를 Value로 생성한다.** |

| **Vector.new()** |
| :--- |
| **Vector를 X, Y, Z 좌표를 0으로 생성한다.** |

## **속성**

| **Vector.X** |
| :--- |
| **X 좌표** |

| **Vector.Y** |
| :--- |
| **Y 좌표** |

| **Vector.Z** |
| :--- |
| **| **Z 좌표** |

## **함수**

| **void Normalize()** |
| :--- |
| **단위를 1로 정규화 시킨다.** |

## **연산자**

| **Vector Vector + Vector** |
| :--- |
| **두 벡터 값을 더해서 그 값을 리턴한다.** |

| **Vector Vector - Vector** |
| :--- |
| **앞에 벡터에서 뒤의 벡터를 뺀 값을 리턴한다.** |

| **Vector Vector * Vector** |
| :--- |
| **두 벡터 값을 곱해서 그 값을 리턴한다.** |

## **예제**

```lua
a = Vector.new(1, 2, 3)
b = Vector.new(3)

c = a + b		--> c.X = 4, c.Y = 5, c.Z = 6

d = Vector.new()
d.X = 10

d.Normalize()   --> d.X = 1, d.Y = 0, d.Z = 0
```