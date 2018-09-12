# 훌륭한 프로그래머 되는 법
---

### 0. 개요

컴퓨터과학을 배운지 2년여 되는 시점에서 이대로 가면 되는지, 정말 잘 가는 것인지 확인하고 싶었습니다. 또, 깨끗한 코드를 작성하는 법은 무엇인지, 협업을 할 때 같이 일하고 싶은 사람의 코드는 어떻게 쓰는지를 배우고자 합니다. 그런 이유에서 '훌륭한 프로그래머 되는 법'은 많은 분들의 추천을 받는 책입니다. 이 책을 읽고, 중요하다 싶은 요소를 챕터별로 정리해나갈 예정입니다.

---

### 1. 코드에 신경 쓰기
- 코드는 늘 신경써서 작성한다
- 작성자의 의도가 드러나는 코드여야 한다
  * 그렇다고 과도한 주석 처리는 금물
- 유지보수가 가능해야 한다
  * 추가적으로, 되는 '척'하는 코드는 금물

### 2. 정돈된 코드 유지하기
- 일관성있고, 명백한 코드를 작성한다
  * 물론 예쁜 레이아웃이 중요하지 않은 것은 아니다
  * 명명을 실제 역할과 일치하도록
- 다른 동료(또는 미래의 자신)이 알아보도록 작성한다
  * 과한 주석을 하지 말자
- 구조를 잘 잡아야 한다
  ```
  void exampleFunction(int param){
  
      // input과 관련된 것 끼리 묶기
      param = sanitiseParamValue(param);
      doSomethingWithParam(param);
  
      // '문단'은 그 다음에 나누기
      updateInternalInvariants();
      notifyOthersOfChange();
  }
  ```
  * 클래스 선언은 이런식으로
  ```
  Class Example{
  
  public:
    Example(); // 생명주기 관리부터 시행
    ~Example();
  
    void doMostImportantThing(); // 새 문단 시작
    void doSomethingRelated();
    
    void somethingDifferent();
    void aRelatedThing()
    
  private:
    int privateStuffComesLast;
  }
  ```
    
