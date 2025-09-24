# CPU & Computer Architecture Q&A 정리

이 문서는 CPU 구조, 레지스터, 플래그, 메모리, 버스, I/O 등과 관련된 기초적인 질문과 답변을 **영문 원문 + 한국어 해석 + 답변** 형식으로 정리한 자료입니다.  
학습 및 참고용으로 작성되었습니다.

---

## 1 ~ 10번 문제

1. **Q: In 32-bit mode, besides ESP, which register can be used as a pointer to stack variables?**  
   **Q(해석): 32비트 모드에서 스택 포인터(ESP) 외에 스택의 변수를 가리키는 레지스터는 무엇입니까?**  
   **A:** EBP (Base Pointer)

2. **Q: Name at least four CPU status flags.**  
   **Q(해석): CPU 상태 플래그 4가지 이상을 쓰시오.**  
   **A:** CF, ZF, SF, OF

3. **Q: Which flag is set when the result of an unsigned arithmetic operation is too large to fit into the destination?**  
   **Q(해석): 부호 없는 연산 결과가 너무 커서 목적지에 저장할 수 없을 때 설정되는 플래그는?**  
   **A:** CF (Carry Flag)

4. **Q: Which flag is set when the result of a signed arithmetic operation is either too large or too small to fit into the destination?**  
   **Q(해석): 부호 있는 연산 결과가 너무 크거나 작을 때 설정되는 플래그는?**  
   **A:** OF (Overflow Flag)

5. **Q: (True/False) When a register operand size is 32 bits and the REX prefix is used, the R8D register is available for programs to use.**  
   **Q(해석): (참/거짓) REX 프리픽스와 32비트 오퍼랜드 사용 시 R8D 사용 가능하다.**  
   **A:** False (32비트 오퍼랜드에서는 R8D 사용 불가)

6. **Q: Which flag is set when an arithmetic or logical operation generates a negative result?**  
   **Q(해석): 연산 결과가 음수일 때 설정되는 플래그는?**  
   **A:** SF (Sign Flag)

7. **Q: Which part of the CPU performs floating-point arithmetic?**  
   **Q(해석): CPU의 어떤 부위가 부동소수점 연산을 하는가?**  
   **A:** FPU (Floating Point Unit)

8. **Q: On a 32-bit processor, how many bits are contained in each floating-point data register?**  
   **Q(해석): 32비트 프로세서에서 각 부동소수점 데이터 레지스터 크기는 몇 비트인가?**  
   **A:** 80비트 (FPU 레지스터)

9. **Q: (True/False) The x86-64 instruction set is backward-compatible with the x86 instruction set.**  
   **Q(해석): (참/거짓) x86-64 명령어 세트는 x86과 하위 호환된다.**  
   **A:** True

10. **Q: (True/False) In current 64-bit chip implementations, all 64 bits are used for addressing.**  
    **Q(해석): (참/거짓) 현 64비트 칩은 주소 지정에 64비트 모두 사용한다.**  
    **A:** False (완전한 64비트 주소 공간은 대부분 사용하지 않는다)

---

## 11 ~ 20번 문제

11. **Q: (True/False) The Itanium instruction set is completely different from the x86 instruction set.**  
    **Q(해석): (참/거짓) 아이테니엄 명령어 세트는 x86과 완전히 다르다.**  
    **A:** True

12. **Q: (True/False) Static RAM is usually less expensive than dynamic RAM.**  
    **Q(해석): (참/거짓) SRAM이 DRAM보다 가격이 낮다.**  
    **A:** False (SRAM이 더 비싸다)

13. **Q: (True/False) The 64-bit RDI register is available when the REX prefix is used.**  
    **Q(해석): (참/거짓) REX 프리픽스 사용 시 64비트 RDI 레지스터 사용 가능하다.**  
    **A:** True

14. **Q: (True/False) In native 64-bit mode, you can use 16-bit real mode, but not the virtual-8086 mode.**  
    **Q(해석): (참/거짓) 64비트 모드에서는 16비트 실모드 사용 가능, 가상-8086 모드 사용 불가.**  
    **A:** True

15. **Q: (True/False) The x86-64 processors have 4 more general-purpose registers than the x86 processors.**  
    **Q(해석): (참/거짓) x86-64 프로세서는 x86 프로세서보다 범용 레지스터가 4개 더 많다.**  
    **A:** True

16. **Q: (True/False) The 64-bit version of Microsoft Windows does not support virtual-8086 mode.**  
    **Q(해석): (참/거짓) 64비트 윈도우는 가상-8086 모드를 지원하지 않는다.**  
    **A:** True

17. **Q: (True/False) DRAM can only be erased using ultraviolet light.**  
    **Q(해석): (참/거짓) DRAM은 자외선을 사용해야만 지울 수 있다.**  
    **A:** False (이는 EPROM에 해당)

18. **Q: (True/False) In 64-bit mode, you can use up to eight floating-point registers.**  
    **Q(해석): (참/거짓) 64비트 모드에서 최대 8개의 FPU 레지스터 사용 가능하다.**  
    **A:** True

19. **Q: (True/False) A bus is a plastic cable that is attached to the motherboard at both ends, but does not sit directly on the motherboard.**  
    **Q(해석): (참/거짓) 버스는 양쪽 끝이 플라스틱 케이블이며 메인보드에 직접 연결되지 않는다.**  
    **A:** False (버스는 데이터 경로이며, 단순 케이블이 아님)

20. **Q: (True/False) CMOS RAM is the same as static RAM, meaning that it holds its value without any extra power or refresh cycles.**  
    **Q(해석): (참/거짓) CMOS RAM은 SRAM과 같으며, 전력 없어도 데이터가 보존된다.**  
    **A:** False (CMOS RAM은 유지 전력이 필요하다)

---

## 21 ~ 26번 문제

21. **Q: (True/False) PCI connectors are used for graphics cards and sound cards.**  
    **Q(해석): (참/거짓) PCI 커넥터는 그래픽 카드, 사운드 카드 연결에 사용한다.**  
    **A:** True

22. **Q: (True/False) The 8259A is a controller that handles external interrupts from hardware devices.**  
    **Q(해석): (참/거짓) 8259A는 하드웨어 장치의 외부 인터럽트 처리를 담당하는 컨트롤러이다.**  
    **A:** True

23. **Q: (True/False) The acronym PCI stands for programmable component interface.**  
    **Q(해석): (참/거짓) PCI는 programmable component interface의 약어다.**  
    **A:** False (올바른 풀네임은 Peripheral Component Interconnect)

24. **Q: (True/False) VRAM stands for virtual random access memory.**  
    **Q(해석): (참/거짓) VRAM은 virtual random access memory의 약어다.**  
    **A:** False (VRAM은 Video RAM)

25. **Q: At which level(s) can an assembly language program manipulate input/output?**  
    **Q(해석): 어떤 레벨에서 어셈블리 언어가 입출력을 조작할 수 있는가?**  
    **A:** 하드웨어 레벨 및 운영체제(OS) 레벨

26. **Q: Why do game programs often send their sound output directly to the sound card’s hardware ports?**  
    **Q(해석): 게임 프로그램이 사운드카드의 포트로 직접 음성 출력을 하는 이유는?**  
    **A:** 빠른 응답과 지연 최소화를 위해서

---

📌 **정리 끝**
