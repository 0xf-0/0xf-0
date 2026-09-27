<div align="center">

  <img src="./banner.svg" width="100%" alt="0xf-0" />

  <br/><br/>

  <a href="https://github.com/0xf-0">
    <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=16&pause=1800&color=38BDF8&center=true&vCenter=true&width=550&lines=push+rbp;+mov+rbp,+rsp;reconstructing+memory+states+from+raw+bytes;breaking+virtual+tables+%26+tracing+syscalls;0x00007FF7+%E2%80%A2+null+pointer+dereference" alt="Typing SVG" />
  </a>

  <br/><br/>

  <img src="https://img.shields.io/badge/C%2B%2B20-04080D?style=for-the-badge&logo=cplusplus&logoColor=38bdf8" />
  <img src="https://img.shields.io/badge/x64_ASM-04080D?style=for-the-badge&logoColor=38bdf8" />
  <img src="https://img.shields.io/badge/IDA_Pro-04080D?style=for-the-badge&logoColor=38bdf8" />
  <img src="https://img.shields.io/badge/x64dbg-04080D?style=for-the-badge&logoColor=38bdf8" />
  <img src="https://img.shields.io/badge/Ghidra-04080D?style=for-the-badge&logo=ghidra&logoColor=38bdf8" />

</div>

<br/>

```x86asm
; [0xf-0] session entrypoint
_start:
    sub     rsp, 0x28
    lea     rcx, [rip + memory_targets]     ; mem-hunt, hook-scanner, indirect-syscall
    call    reconstruct_vftable
    test    rax, rax
    jz      .breakpoint
    ret

.breakpoint:
    int3    ; trap
```

<br/>

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=0xf-0&show_icons=true&theme=tokyonight&hide_border=true&bg_color=050a10&title_color=38bdf8&text_color=94a3b8&icon_color=00e5ff" height="150" alt="GitHub Stats" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=0xf-0&layout=compact&theme=tokyonight&hide_border=true&bg_color=050a10&title_color=38bdf8&text_color=94a3b8" height="150" alt="Top Langs" />
</div>

<br/>

<p align="center">
  <samp><sub><code>0x00007FFB86208A00 | 48 89 5C 24 10 48 89 74 24 18 57 48 83 EC 20</code></sub></samp>
</p>
