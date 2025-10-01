# Assembly Language Q&A 정리

## 1. Provide examples of three different instruction mnemonics.  
**세 가지 명령어(Instruction) 기호(Mnemonic) 예시를 들어라.**  
**답:** `ADD`, `SUB`, `MOV`

---

## 2. What is a calling convention, and how is it used in assembly language declarations?  
**Calling convention(호출 규약)이란 무엇이며, 어셈블리 선언에서 어떻게 사용되는가?**  
**답:** 호출 규약은 서브루틴에 인자를 전달하고, 호출 이후 스택을 되돌리는 방법을 결정한다.

---

## 3. How do you reserve space for the stack in a program?  
**프로그램에서 스택 공간을 어떻게 확보하는가?**  
**답:** 스택 포인터 레지스터에서 값을 빼서 공간을 확보한다.

---

## 4. Explain why the term assembler language is not quite correct.  
**assembler language라는 용어가 정확하지 않은 이유를 설명하라.**  
**답:** assembler는 소스 코드를 번역하는 프로그램이며, “assembly language”가 올바른 용어이다.

---

## 5. Explain the difference between big endian and little endian. Also, look up the origins of this term on the Web.  
**Big endian과 little endian의 차이, 그리고 용어의 기원을 설명하라.**  
**답:**  
- Little endian → 가장 작은 값이 오른쪽(0번 위치)에 위치  
- Big endian → 가장 큰 값이 오른쪽(0번 위치)에 위치 (반대 구조)

---

## 6. Why might you use a symbolic constant rather than an integer literal in your code?  
**상수 대신 symbolic constant(기호 상수)를 사용할 이유는?**  
**답:** 기호 상수(MIN_CAPACITY 등)는 가독성이 높고 의미를 알기 쉽다.

---

## 7. How is a source file different from a listing file?  
**소스 파일과 listing 파일의 차이점은?**  
**답:**  
- 소스 파일(.asm) → 어셈블러의 입력 파일  
- 리스팅 파일(.lst) → 어셈블 과정에서 생성, 어셈블되지 않는 추가 정보도 포함

---

## 8. How are data labels and code labels different?  
**데이터 레이블과 코드 레이블의 차이점은?**  
**답:**  
- 데이터 레이블 → 데이터 세그먼트(변수 오프셋)  
- 코드 레이블 → 코드 세그먼트(제어 이동)

---

## 9. (True/False): An identifier cannot begin with a numeric digit.  
**식별자는 숫자로 시작할 수 없다.**  
**답:** 참

---

## 10. (True/False): A hexadecimal literal may be written as 0x3A.  
**0x3A와 같이 0x로 시작하는 16진수 리터럴을 쓸 수 있다.**  
**답:** 거짓 (일반적으로 사용하지 않음)

---

## 11. (True/False): Assembly language directives execute at runtime.  
**어셈블리 언어 지시문은 런타임에 실행된다.**  
**답:** 거짓 (컴파일 타임에 처리됨)

---

## 12. (True/False): Assembly language directives can be written in any combination of uppercase and lowercase letters.  
**어셈블리 언어 지시문은 대소문자 구분 없이 쓸 수 있다.**  
**답:** 참

---

## 13. Name the four basic parts of an assembly language instruction.  
**어셈블리 명령어의 4개 기본 구성 요소는 무엇인가?**  
**답:** Label, mnemonic, operand(s), comment

---

## 14. (True/False): MOV is an example of an instruction mnemonic.  
**MOV는 명령어 기호의 한 예이다.**  
**답:** 참

---

## 15. (True/False): A code label is followed by a colon (:), but a data label does not end with a colon.  
**코드 레이블은 콜론(:)으로 끝나지만, 데이터 레이블은 콜론이 없다.**  
**답:** 참

---

## 16. Show an example of a block comment.  
**block comment(블록 주석) 예시를 보여라.**  
**답:**  COMMENT !
this is the first line
this is the second line
!


## 17. Why is it not a good idea to use numeric addresses when writing instructions that access variables?  
**Q:** 변수 접근 명령에서 숫자 주소 사용이 좋지 않은 이유는?  
**A:** 프로그램이 변경될 때 주소가 바뀔 수 있으므로 유지보수성이 떨어진다.  

---

## 18. What type of argument must be passed to the ExitProcess procedure?  
**Q:** ExitProcess 프로시저에 전달되어야 하는 인자는 어떤 종류인가?  
**A:** 정수(integer), 보통 "프로그램 종료 코드".  

---

## 19. Which directive ends a procedure?  
**Q:** 어떤 디렉티브가 프로시저를 종료시키는가?  
**A:** `ENDP` 디렉티브는 프로시저(서브루틴)의 끝을 나타낸다.  

---

## 20. In 32-bit mode, what is the purpose of the identifier in the END directive?  
**Q:** 32비트 모드에서 END 디렉티브의 식별자는 어떤 역할을 하는가?  
**A:** 프로그램이 시작될 entry point(즉, 실행 시작점) 이름을 정한다.  

---

## 21. What is the purpose of the PROTO directive?  
**Q:** PROTO 디렉티브의 목적(용도)은 무엇인가?  
**A:** 프로시저(함수)의 프로토타입 선언을 위해 사용한다.  

---

## 22. (True/False): An Object file is produced by the Linker.  
**Q:** 오브젝트 파일은 링커에 의해 생성된다.  
**A:** 거짓 — 오브젝트 파일은 Assembler가 만든다.  

---

## 23. (True/False): A Listing file is produced by the Assembler.  
**Q:** 리스팅 파일은 어셈블러에 의해 생성된다.  
**A:** 참.  

---

## 24. (True/False): A link library is added to a program just before producing an Executable file.  
**Q:** 링크 라이브러리는 실행 파일이 만들어지기 직전에 프로그램에 추가된다.  
**A:** 참.  

---

## 25. Which data directive creates a 32-bit signed integer variable?  
**Q:** 32비트 signed 정수 변수를 생성하는 데이터 디렉티브는?  
**A:** `SDWORD` 또는 `DD` (define doubleword).  

---

## 26. Which data directive creates a 16-bit signed integer variable?  
**Q:** 16비트 signed 정수 변수를 생성하는 데이터 디렉티브는?  
**A:** `SWORD` 또는 `DW` (define word).  

---

## 27. Which data directive creates a 64-bit unsigned integer variable?  
**Q:** 64비트 unsigned 정수 변수를 생성하는 데이터 디렉티브는?  
**A:** `QWORD` 또는 `DQ` (define quadword).  

---

## 28. Which data directive creates an 8-bit signed integer variable?  
**Q:** 8비트 signed 정수 변수를 생성하는 데이터 디렉티브는?  
**A:** `SBYTE` 또는 `DB` (define byte).  

---

## 29. Which data directive creates a 10-byte packed BCD variable?  
**Q:** 10바이트 packed BCD 변수를 만드는 데이터 디렉티브는?  
**A:** `TBYTE` (define ten bytes).  

---

