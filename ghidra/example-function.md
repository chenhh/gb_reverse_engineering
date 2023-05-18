# 範例: 函數

## 簡單函數

```cpp
int f(){
    return 123;
}
```

#### x86: g++ -O

```nasm
f():
        mov     eax, 123
        ret
```

#### x86:  msvc -Ox

```nasm
int f(void) PROC                                      ; f
        mov     eax, 123                      ; 0000007bH
        ret     0
int f(void) ENDP                                      ; f
```

#### arm: v7-clang

```nasm
f():
        mov     r0, #123
        bx      lr
```

## 參考資料

* [https://godbolt.org/](https://godbolt.org/)
