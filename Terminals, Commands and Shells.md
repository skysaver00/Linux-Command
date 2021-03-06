# 터미널, 명령어, 쉘   
   
## 명령어(Command) VS 쉘(Shell)   
명령어 command는 **Word**에 해당한다. 단어에 해당하는 언어를 읽을 수 없다면, 나에게는 그 단어는 사실 의미가 없는 것이다.   
이해하지 못하기 때문이다. Strawberry라는 것은 단어(Command)라고 인지할 수 있지만, 영어(Language)를 모른다면, 의미를 알 수 없다.  
하지만 우리가 영어를 안다면 Strawberry == 딸기라는 것을 알 수 있다. 따라서 Strawberry를 인지하기 위해선 3가지의 개념이 필요하다.   
Commands(Strawberry) -> 영어 -> Meaning(딸기)   
   
여기에 중간에서 텍스트, Command를 특정한 의미로 깨닫게 해주는 프로세스가 존재한다. 이 영어(Language)를 **Shell**이라고 하는 것이다.   
Gift(Commands) -> 영어(Shell) -> Meaning(선물)   
   
그런데 여기서 이상한 Shell을 쓰게 된다면? 예를 들어 독일어 Shell이라고 가정해보자.   
Gift(Commands) -> 독일어(Shell) -> Meaning(독극물)이 나와버린다.   
따라서 중간 단계에 있는 Shell은 Command가 같더라도 완전히 다른 의미가 나오게 될 수 있는 것이다...   
따라서 **Shell의 종류에 따라 해당 단어, Command를 완전히 다르게 해석해서 컴퓨터에서도 다른 행동을 할 수 있다는 얘기**가 된다.   
   
## 이를 터미널, 명령어, 쉘에 적용해보자.   
*터미널*은 그저 **Shell로 향하는 창문**과 같은 역할을 한다.   
터미널 없이 명령어를 입력해라! 라는 행동은 할 수 가 없다. 마치 창문을 열지 말고, 방 안을 환기시켜라! 와 같은 말이 된다.   
따라서 명령어(Command)를 터미널 없이 입력하는건 불가능한 행동이다.   
   
*쉘*은 종류가 많다. 인간의 언어가 수천가지가 넘듯이, 쉘도 **하나가 아니라 여러가지의 쉘**이 있고, 이들은 같은 명령어도 다르게 해석한다.   
그중에 **bash shell**이라고 하는것이 있다. 이게 가장 흔한 쉘중 하나인데, 리눅스 내에서는 거의 대부분 bash shell을 이용해서 명령어를 해석한다.   
이것을 **기본적인 명령어 해석기**라고 해석하면 OK이다.
   
*명령어*는 따라서 **그냥 터미널에 입력하는 단어**같은 것이다. 명령어 자체에는 의미가 담겨있지 않으나, 이를 해석하는 **Shell**이 명령어를 읽고, 리눅스 내에서 특정 행동을 수행하는 것이다.   

### 3줄 요약   
1. 명령어(Command)는 그저 터미널에 입력하는 단어이다.   
2. 명령어는 쉘(Bash Shell)에 의해 해석되고, 쉘이 의미를 부여해 컴퓨터에 명령을 지시한다.   
3. 터미널(은 쉘로 향하는 창문과 같다. 하지만 창문이 없으면 바깥 세상을 볼 수 없듯이, 컴퓨터에 명령어를 입력하려면 터미널이 필요하다.   
   
   
   
###### 명령어는 Case-Sensitive하다. 잘못해서 대문자로 입력하면 쉘이 소문자와 같이 인지하지 않고 에러를 일으킬 수 있다. echo != Echo   
