# Dataset

status: In progress


- 공격 유형(label_action)
```
Vulnerability_Scan               16867
System_Cmd_Execution              9807
HOST_Scan                         6315
Path_Disclosure                   4775
SQL_Injection                     3395
Cross_Site_Scripting              1348
Automatically_Searching_Infor     1119
Leakage_Through_NW                 956
Directory_Indexing                 418
Name: label_action, dtype: int64
```


- Data Decoding
https://github.com/P-DOEUN/AI/tree/main/DATA/attack_type

<aside>
0️⃣ **KISA DATA HEADER

-** Method
- Path
- Query Parameters
- Protocol
- Host
- Authorization
- Accept-Encoding
- User-Agent
- Accept
- Accept-Language
- X-Arachni-Scan-Seed
- Cookie

</aside>

- label_action 열에서 attack_type 많은 순서
- Dataset 페이지 안에는 KISA에서 제공한 데이터 몇 개 골라서 공격 구문이 어디에 속해있는지 확인해봄.

<aside>
1️⃣ **Vulnerability_Scan**

- 컴퓨터 시스템, 네트워크 또는 애플리케이션에서 발생할 수 있는 보안 취약점을 식별하고 검사하는 과정
- [시스템과 네트워크 디바이스가 구멍, weakness, 이슈 등이 있는지를 검사하는 프로세스이며 공격자가 그것을 공격하지 건에 그것을 찾아내는 작업](https://m.blog.naver.com/ijoos/221604134238)

- Vulnerability Scan는 다른 공격 유형에서 본 공격 패턴들이 보임.

[Dataset](https://www.notion.so/Dataset-96e40568ce8349ed9d6877336696a424?pvs=21)

</aside>

<aside>
2️⃣ **System_Cmd_Execution**

- 웹 요청 메시지에 임의의 시스템 명령어를 삽입하고 전송, 웹 서버에서 해당 명령어를 실행하도록 하는 공격 ( [웹을 통해서 시스템 명령어를 실행하는 공격](https://yehey-study.tistory.com/entry/%EC%BB%A4%EB%A7%A8%EB%93%9C-%EC%9D%B8%EC%A0%9D%EC%85%98-%EA%B3%B5%EA%B2%A9-Command-injection) )
- Query Patameter
- body

[Dataset](https://www.notion.so/Dataset-7115dbc4711e46f6b9f3d78e1281633f?pvs=21)

</aside>

<aside>
3️⃣ **HOST_Scan**

- Path
- **host**

[Dataset](https://www.notion.so/Dataset-b0ae840dc1344ac3a2346b4b92baf3bb?pvs=21)

</aside>

<aside>
4️⃣ **Path_Disclosure**

- 웹 응용 프로그램에서 파일 경로나 디렉터리 구조를 공격자가 알아내는 것
    - 공격자가 시스템 구조에 대한 정보를 얻어 추가 공격을 수행할 수 있게 하는데 사용될 수 있다.
    - 이 정보를 사용하여 시스템의 취약점을 이용하거나 민감한 정보에 접근할 수 있다.
- Path

[Dataset](https://www.notion.so/Dataset-370630ba81b34cdf96cbee02683e2a48?pvs=21)

</aside>

<aside>
5️⃣ **SQL_Injection**

- Query Parameter
- **User-Agent**
- body

[Dataset](https://www.notion.so/Dataset-c5f4e5d9976f4fcd8755c553ad953f7e?pvs=21)

</aside>

<aside>
6️⃣ **Cross_Site_Scripting**

- Query Parameter
- body

[Dataset](https://www.notion.so/Dataset-6f59ab1fcf90405688973bbae4b206ce?pvs=21)

</aside>

<aside>
7️⃣ **Automatically_Searching_Infor**

- User-Agent 혹은 host 정보 참고

**“**nmap scripting engine” 문자열 포함 → namp 도구를 사용하여 자동으로 정보 수집하려는 시도 나타냄.

"wget” 문자열 포함 → 웹 페이지를 다운로드하는 도구 → 자동으로 정보 수집하려는 시도 나타냄,

[Dataset](https://www.notion.so/Dataset-f20f5dba5fb74689900b5c88a4c39006?pvs=21)

</aside>

<aside>
8️⃣ **Leakage_Through_NW**

- 네트워크를 통해 민감한 정보가 누출되는 공격
****

[Dataset](https://www.notion.so/Dataset-4c50a744352145f8956358a526572d36?pvs=21)

</aside>

<aside>
9️⃣ **Directory_Indexing**

- 클라이언트인 웹 브라우저가 웹 페이지가 아닌 디렉터리 구조를 가리키는 URL을 요청할 때 웹 서버 측에서 인덱스 페이지를 응답하여 발생하는 취약점
- 인덱스 페이지는 디렉터리 및 파일 리스트를 사용자에게 노출하기 때문에 공격자는 시스템 구조를 파악하는 것이 가능하며, 일반 웹 페이지보다 자유로운 액세스를 제공하므로 공개되지 않은 파일 등에 액세스하는 것이 가능하다.
- URL
- 

[Dataset](https://www.notion.so/Dataset-7bb2abd0a9dd48049fd6209afa842c40?pvs=21)

</aside>

---

<aside>
📌 **참고**

</aside>

[OS Command Injection - bi0s wiki](https://wiki.bi0s.in/web/os-injection/)

SQL injection, XSS, Command injection

[[웹 취약점] 디렉터리 인덱싱, 리스팅 (Directory Indexing, Listing)](https://madcatz.tistory.com/entry/웹-취약점-디렉터리-인덱싱-리스팅-Directory-Indexing-Listing)

Directory_Indexing

[커맨드 인젝션 공격 / Command injection](https://yehey-study.tistory.com/entry/커맨드-인젝션-공격-Command-injection)

Command Injection

[Vulnerability Scanning](https://m.blog.naver.com/ijoos/221604134238)

Vulnerability Scan