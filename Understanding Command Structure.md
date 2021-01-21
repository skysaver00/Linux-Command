# Command Structure

## 명령어가 Language로 보여야 하는 이유!   
commandName options inputs 이 순서대로 간다.   
shell이 어떤 프로그램을 쓰고 싶은지 먼저 알아야 한다. shell이 알았다는 뜻 == 내가 어떤 프로그램을 돌리고 싶은지 shell의 이름을 알았다는 뜻.   
shell은 shell's path을 통해 프로그램을 탐색할 것이다.   
   
**echo $PATH**를 입력해 보면, 엄청나게 긴 디렉토리 경로가 나오게 된다. 이것은 자세히 보면 각각의 폴더에 대한 경로를 보여준다.   
/home/kyw/bin:/home/kyw/.local/bin:/usr/local/sbin:... 이렇게 :로 경로들이 구분되어 있다.   
즉 echo $PATH는 가장 왼쪽의 경로부터 시작해서 디렉토리를 들어가서 echo든, date든 간에 불러온 것을 찾을 것이다.   
만약에 찾지 못하게 되면 다음 폴더(오른쪽)로 넘어간다. 만약에 하나도 찾지 못하면, command not found를 출력한다.   
즉 명령을 찾을 수 없습니다. 는 여기서 shell이 저 폴더 순으로 탐색하면서 명령어를 찾다가 못찾아서 나온 대답이란 뜻이다.   
   
   
만약에 동시에 들어있다면, 가장 먼저 찾은(왼쪽에 있는)곳을 탐색한다.   
오른쪽에 있는 디렉토리에서는 불러올 수 없다.
   
which cal 을 입력하면 usr/bin/cal이 나오게 된다. 이것은 echo $PATH를 검색해 봤다면 바로 찾아낼 수 있다.
당연히 which which도 가능하다.
   
   **이를 통해 shell이 내가 입력한 명령어를 어디서 찾아오는지 알 수 있다!**   
   
input -> 모든 commandName이 input을 필요로 하지 않는다. 몇몇 명령어는 필수가 아니다. 예를들어 date가 있다.   
만일 input을 필요로 한다면, 그 input는 operand라고 부른다.   
cal -> commandName. 이 명령어는 operand를 반드시 필요로 하지 않는다.   
하지만 cal 2017 -> 2017은 여기서 operand이다. 그럼 2017년 달력을 출력하게 된다.   
이런 operand는 반드시 하나거나 없거나 그런건 아니다. operand는 여러개일 수 있다.   
cal 12 2020 -> 2020년의 12월을 출럭하는 달력이 된다. 여기서 operand는 2020, 12이다.   
   
잘 보면 echo "hello"이런것도 echo -> commandName, "hello" -> operand이다.   
operand는 -y이렇게 대시가 붙어서 나올 수 있다!   
date -u -> 날짜가 나오는데 UTC에 해당하는 옵션이 적용되어 그린위치 시각이 나오게된다(UTC-0).   
만일 해당 -가 이상하면 invalid option -- 'a'등 해서 나오게 된다.   
   
-u는 사실 긴 이름이 있을 수 있다. -u -> --universal이다.   
이와 같은 예시는 -v -> --version, -h -> --help등이 있다.   
일반적으로 -는 짧은 이름, --은 긴 이름으로 많이들 선택한다. --은 -처럼 -abce이렇게 못하고, --help --version --universal이렇게 따로 써야 한다.   
   
   
당연히 command는 case sensitive이니까 date != dAte != DATE != Date이다.   

cal -A 1 12 2017을 입력하면 -A는 After와 같은 의미가 있어서 12월, 내년 1월까지 나오게 된다.   
