# 7_TIL_Private

:purple_heart: Java

:green_heart: Spring

:black_heart: 인프라

:handshake: PJT업무

:crescent_moon: 달이 조언​

:heart: 개념/용어

:blue_heart: 글/영상

:books: 책/강의

---

## 7/1(화)
:green_heart: Spring


## 7/8(화)
:green_heart: Spring

- Optional<>
    - Optional.of()
    - Optional.empty()


- 예외 일으키기
    - ``` Exception X = new Exception("의도적 예외처리"); ```
- 테스트케이스
    ```java
    @BeforeEach
    public void beforeEach() {
        memoryMemberRepository.clearStore();
    }

    @Test
    public void clearStore() {
        // given
        Member member = new Member();
        memoryMemberRepository.save(member);
        //when
        memoryMemberRepository.clearStore();
        //then
        assertThat(memoryMemberRepository.findAll().isEmpty()).isTrue();
    }
    ```
    - assertThat(T actual).someMethod();
    - assertThatThrownBy(() -> {}).isInstanceOf(Exception.class).hasMessage("~");
    ...

## 7/9(수)
:green_heart: Spring
- 테스트케이스 (Mock사용)
    ```java
    @Test
    public void 회원가입() {
        //given
        Member member = new Member();
        member.setName("nyang");

        Mockito.when(memberRepository.findByName(any()))
            .thenReturn(Optional.empty());

        Mockito.when(memberRepository.save(any()))
            .thenAnswer((it)-> {
                Member param = it.getArgument(0,Member.class);
                param.setId(1L);
                return param;
            });
        //when
        Long joinID = memberService.join(member);

        //then
        assertThat(joinID).isEqualTo(1L);

        Mockito.verify(memberRepository).findByName("nyang");
        Mockito.verify(memberRepository).save(member);
    }
    ```
    - Mokito
        - .when()
            - .thenReturn()
            - .thenAnswer()
        - .verify()
            ex- verify(mock).MockOfSomeMethod();
            ex- verify(mock, verificationMode).MockOfSomeMethod();

## 7/10(목)
:green_heart: Spring

- lombok 어노테이션
    - `@Data`: @RequiredArgsConstructor, @Setter, @Getter, toString 모두 가지고 있는 어노테이션
    - `@NoArgsConstructor` : 파라미터가 없는 생성자 생성
    - `@RequiredArgsConstructor` : 초기화 되지 않은 final 필드와 @NonNull 어노테이션이 붙은 필드에 대한 생성자 생성
    - `@AllArgsConstructor` : 모든 필드에 대한 생성자 생성
    - `@Setter` & `@Getter` : getter 와 setter 메소드를 생성

## 7/11(금)
:green_heart: Spring
- 싱글턴 패턴 : 생성자가 여러 차례 호출되더라도 실제로 생성되는 객체는 하나이고, 
최초 생성 이후에 호출된 생성자는 최초의 생성자가 생성한 객체를 리턴한다.

```java
// 싱글턴 구현 방법 중, 객체 미리 생성해둬서 공유하기
public class Singleton {
    // 1 static final 객체 1개 생성
    private static final Singleton one = new Singleton();
    // 2 static 메서드로 객체 생성하도록. 리턴은 만들어진 객체 1개
    public static Singleton getInstance(){
        return one;
    }
    // 3 private으로 외부에서 new 객체 생성 막기
    private Singleton(){}
}
```

```java
ApplicationContext appConfig = new AnnotationConfigApplicationContext(Appconfig.class)
A a1 = appConfig.getBean(A.class);
A a2 = appConfig.getBean(A.class);
// 둘이 같은 객체를 가리킴(주소같음)
...
```
객체 인스턴스 공유
- 장점 : 메모리 낭비 줄임
- 단점 : 의존성 증가, private 생성자로 상속 제한, 테스트 어려움, 멀티스레드 환경에서의 문제
- 주의점 : 객체 상태를 유지(stateful)하게 설계하면 안됨

## 7/15(수)
:crescent_moon: HTML&CSS 레퍼런스 https://developer.mozilla.org/
  - `<label>` 와 연관 `<input>`or `<textarea>` element
    - `<label>` element 기능 : 연관 element의 check 범위 늘려줌
    - `<label>` for와 `<input>` id를 같은 값으로 연결
    - placeholder

- type 들어가는 값의 종류
    - `<input>` : text, button, checkbox, radio, file, reset, submit ...
    - `<button>` : submit, button, reset

:green_heart: Spring
- @RequestMapping
    - @RequestMapping("/") - 파라미터가 한 개 일 때, 변수명 생략 가능
    = @RequestMapping(path="/")
    = @RequestMapping(value="/") 
    = @RequestMapping(path={"/"})  - 값이 한 개 일 때, {} 생략 가능
    - @RequestMapping(path={"/", "/home"}) - 여러 개
    - @RequestMapping(path="/",method=RequestMethod.GET)
    = @GetMapping(path="/")
    - @RequestMapping(path="/",method={RequestMethod.GET, RequestMethod.POST})

## 7/16(목)
:crescent_moon: HTML&CSS 
- `<!doctype html>` , `xmlns` xml name space 
- `th:` 타임리프 문법 나올 때 , `${}` 인터폴레이션

:green_heart: Spring
- @RequestParams