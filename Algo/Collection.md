# Collection 
객체들을 한 곳에 모아 놓고 편리하게 사용할 수 있는 환경을 제공한다. 

* list
* set
* map
* queue
* stack

### 정적 자료구조 
- 고정된 크기의 자료구조
- 배열이 대표적 정적 자료구조
- 선언 시 크기를 명시하면 바꿀 수 없다.

### 동적 자료구조
- 요소의 개수에 따라 자료구조의 크기가 동적으로 증가하거나 감소
- 리스트, 스택, 큐

![스크린샷 2023-12-18 오후 11 55 52](https://github.com/Youth787/SSAFY_CS_Study/assets/90955152/901c9b26-1419-415a-81d0-4bc6b34c338c)

> 자료구조들의 종류는 어떤 구조에서 얼마나 빨리 원하는 데이터를 찾는가에 따라 결정 <br>

* 순서를 유지할 것인지? <br>
* 중복을 허용할 것인지? <br>
* 다른 자료구조들에 비해서 어떤 장점과 장점을 가지고 있는지?  <br>


![스크린샷 2023-12-18 오후 11 59 29](https://github.com/Youth787/SSAFY_CS_Study/assets/90955152/1ecfb2b7-079f-4680-9221-6b4d673b07e0)

-----

# List
* Arraylist
* LinkedList

> array

- 같은 타입의 데이터를 묶어 사용하는 자료구조
- 접근 속도가 빠르다
- 크기를 변경할 수 없어 추가 데이터를 넣을때, 새로운 배열을 만들고 복사
- 데이터 삭제 시, 인덱시를 재조정하기 위해 전체 데이터를 옮겨야 한다.
- ArrayList 역시 Array를 활용하므로 이 같은 특징을 가지고 있다.

### Arraylist
자동으로 배열의 크기를 관리해준다. 

![스크린샷 2023-12-19 오전 12 31 19](https://github.com/Youth787/SSAFY_CS_Study/assets/90955152/86a6cbdb-66a1-4308-946d-59f9372fe30e) <br>

내부적으로 데이터를 배열에서 관리하며 데이터의 추가, 삭제를 위해 임시 배열을 생성해 데이터를 복사하는 방법을 사용하고 있다. </br>
대량의 자료를 추가/삭제 하는 경우에는 그만큼 데이터의 복사가 많이 일어나게 되어 성능 저하를 일으킬 수 있다.  </br>
반면 각 데이터는 인덱스를 가지고 있기 때문에 한번에 참고가 가능해 데이터의 검색에는 유리한 구현체이다.  </br>

### linkedList
- 노드와 포인터를 이용하여 만든 리스트
- 노드 클래스를 살펴보면 next와 prev로 양방향 포인터를 가진다. 
- 포인터로 각각의 노드들을 연결하고 있어서, 삽입/삭제가 빠르다는 장점이 있다. (단순히 기존 포인터를 끊고 새로운 노드에 연결하면 되기 때문)
- 특정 원소를 조회하기 위해서는 첫 노드부터 순회해야하기 때문에 Arraylsit에 비해 느리다는 단점이 있다.
- linkedlist는 조회보다 삽입/삭제가 많은 경우에 사용하는 것이 좋다. 

![스크린샷 2023-12-19 오전 11 58 15](https://github.com/Youth787/SSAFY_CS_Study/assets/90955152/a5ce8f44-0fe5-4447-82f5-dc32679b08b4)

<br>

-----

# Set

> 종류

* hashset
* treeset

> 특징

- 순서가 없고, 중복을 허용하지 않는다.
- 장점 : 빠른 속도, 효율적인 중복 데이터 제거 수단
- 단점 : 단순 집합의 개념으로 정렬하려면 별도의 처리가 필요하다.

<br>

* HashSet
  - 해시 테이블에 원소를 저장
  - 해시 알고리즘을 사용하여 검색속도가 매우 빠르다.
  - 성능면에서 우수하다고 알려져 있다.
  - 원소들의 순서가 일정하지 않다.
  - 저장 순서를 유지하려면 Linkedhashset을 이용하면 된다.


* TreeSet
  - 이진 검색 트리
  - 값에 따라서 순서가 결정된다.
  - 값을 순서대로 정렬할 필요가 있다면 고려해볼만한 선택지
  - hashset과 다르게 그 값이 정렬되어 저장되지만, 그렇기 때문에 속도가 hashset보다 느리다. 

<br>

### 해시 알고리즘 
hashset은 해시 알고리즘 기반으로 동작한다. <br>
해시 함수를 사용하여 데이터를 해시 테이블에 저장하고 그것을 다시 검색하는 알고리즘 <br>

![스크린샷 2023-12-19 오전 1 24 42](https://github.com/Youth787/SSAFY_CS_Study/assets/90955152/e0784fa7-1e88-4efc-ba58-42a9d171e4da)

* 입력된 키를 해시 코드로 변환한다.
* 해시 코드를 인덱스로 한 bucket이라는 array에 해당 인덱스를 찾아 저장한다. 

<br>

-----

# Map

> 종류

* HashMap
* HashTable
* LinkedHashMap
* TreeMap

> 특징

- key와 value로 이루어진 자료구조
- Set과 마찬가지로 순서를 가지지 않는다.
- key값은 중복될 수 있지만 value는 중복될 수 없다.
  
![스크린샷 2023-12-19 오전 11 41 21](https://github.com/Youth787/SSAFY_CS_Study/assets/90955152/e0c9b1ec-1c43-47dc-8eb2-8f68f5d52c26)

### HashMap
- 일반적으로 자주 사용되는 자료구조
```` java
void hashMapTest() {
    Map<Integer, String> hashMap = new HashMap<>();
    hashMap.put(1, "one");
    hashMap.put(2, "two");

    Iterator<Integer> it = hashMap.keySet().iterator();
    while(it.hasNext()) {
        int key = it.next();
        System.out.println("key: " + key + ", value: " + hashMap.get(key));
    }
}
````
```` java
  key: 1, value: one
  key: 2, value: two
````

### LinkedHashMap
일반적으로 Map 자료구조는 순서를 가지지 않지만, LinkedHashMap은 들어온 순서대로 순서를 가진다. <br>

### TreeMap
이진트리로 구성되어 있고, Treeset과 같이 정렬하여 데이터를 저장하고 있다. <br>
데이터를 저장할때 정렬하기 때문에 저장 시간이 다른 자료구조에 비해 오래걸린다. <br>





