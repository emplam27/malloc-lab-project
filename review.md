# 📌 Code Reivew  

### _reivewer - 오태양 (리뷰 경험없음)_
> **🎉🎉 이번 한주도 고생 많았습니다! 🎉🎉**  
<hr>

1. 리뷰를 line by line으로 작성할 수 밖에 없을 것 같습니다.  
2. review는 "explicit-malloc.c'에 대해서만 작성했습니다.  
3. 수정이 필요할 것 같은 부분이나 배운점에 대한 생각을 기록하겠습니다.  
4. 리뷰를 파일에 주석을 남기기보다(코드가 더러워질까봐) 현재 md 파일에 적어 포함하겠습니다.  

- line 23 at macro :: `WSIZE`를 포인터의 크기로 잡은 것은 현명한 선택이라고 생각함. 환경에 따라 바뀔 수 있어 적절한 판단이였다고 생각함
- line 25 at macro :: `CHUNKSIZE`를 휴리스틱하게 변경함에 따라 점수가 상승하거나 하락하는 것을 개인적으로 확인했습니다 이 부분 참고하세요.
- line 66,67 at mm_init() :: 시도해보지는 못했지만, 아마 `heap_listp`에 `24 Byte`를 할당한 것은 포인터가 `64 bit (8 byte)`인 환경을 고려한 것이라고 보여집니다. 만약 의도한 바가 맞다면 `66, 67 라인`의 메모리 영역이 각각 `2칸`씩을 차지해야 한다고 보여집니다.
- line 85-93 at mm_malloc() :: C 계열의 언어는 문법상 반복, 조건문의 해당하는 평문이 1줄인 경우 중괄호(`{`)를 생략하여도 괜찮습니다. 이 부분에서 중괄호를 생략해 line 수를 감소하고 가독성을 높여줄 수 있을 것 같습니다.
- line 190 at find_fit() :: while 문으로 작성하여 가독성이 매우 훌륭합니다. LGTM
- line 229 at delete_free() :: 조건을 잘 설정해서 복잡할 수 있는 문제를 쉽게 해결한 것 같습니다.
