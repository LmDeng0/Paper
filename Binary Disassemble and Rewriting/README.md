
# Paper list:


## Suvery and Overview:

### x86-64

- [An In-Depth Analysis of Disassembly on Full-Scale x86/x64 Binaries (USENIX, 2016)](./Suvery%20and%20Overview/An%20In-Depth%20Analysis%20of%20Disassembly%20on%20Full-Scale%20x86:x64%20Binaries.pdf)&emsp;[[Abstract]](#An-In-Depth-Analysis-of-Disassembly-on-Full-Scale-x86-x64-Binaries)

- [SoK:All You Ever Wanted to Know About x86/x64 Binary Disassembly But Were Afraid to Ask (IEEE Symposium on Security and Privacy, 2021)](./Suvery%20and%20Overview/SoK-%20All%20You%20Ever%20Wanted%20to%20Know%20About%20x86:x64%20Binary%20Disassembly%20But%20Were%20Afraid%20to%20Ask.pdf)&emsp;[[Abstract]](#SoK-All-You-Ever-Wanted-to-Know-About-x86-x64-Binary-Disassembly-But-Were-Afraid-to-Ask)

### ARM

- [An Empirical Study on ARM Disassembly Tools (SIGSOFT, 2020)](./Suvery%20and%20Overview/An%20Empirical%20Study%20on%20ARM%20Disassembly%20Tools.pdf)&emsp;[[Abstract]](#An-Empirical-Study-on-ARM-Disassembly-Tools)


## Binary Disassemble and Rewriting:


- [Speculative disassembly of binary code (CASES , 2016)](./Research/Speculative%20disassembly%20of%20binary%20code.pdf)&emsp;[[Abstract]](#Speculative-disassembly-of-binary-code)

     Spedi is a speculative disassembler for the variable-size Thumb ISA


## Binary Translator:

- [Low Overhead Dynamic Binary Translation on ARM (CCS, 2006)](./Research/Low%20Overhead%20Dynamic%20Binary%20Translation%20on%20ARM.pdf)&emsp;[[Abstract]](#Low-Overhead-Dynamic-Binary-Translation-on-ARM)

     将AArch32转换为AArch64指令


- [A Retargetable Static Binary Translator for the ARM Architecture](./Research/A%20Retargetable%20Static%20Binary%20Translator%20for%20the%20ARM%20Architecture.pdf)


# Conclusion about Paper：

An Empirical Study on ARM Disassembly Tools.

[Detail notes](https://www.notion.so/An-Empirical-Study-on-ARM-Disassembly-Tools-43b4857a733e45589733bbefe3ad1a6b)



## Abstract:

### An In Depth Analysis of Disassembly on Full Scale x86 x64 Binaries

**Abstract:** It is well-known that static disassembly is an unsolved problem, but how much of a problem is it in real software— for instance, for binary protection schemes? This work studies the accuracy of nine state-of-the-art disassemblers on 981 real-world compiler-generated binaries with a wide variety of properties. In contrast, prior work focuses on isolated corner cases; we show that this has led to a widespread and overly pessimistic view on the prevalence of complex constructs like inline data and overlapping code, leading reviewers and researchers to underestimate the potential of binary-based research. On the other hand, some constructs, such as function boundaries, are much harder to recover accurately than is reflected in the litera- ture, which rarely discusses much needed error handling for these primitives. We study 30 papers recently pub- lished in six major security venues, and reveal a mismatch between expectations in the literature, and the actual ca- pabilities of modern disassemblers. Our findings help improve future research by eliminating this mismatch.


### SoK All You Ever Wanted to Know About x86 x64 Binary Disassembly But Were Afraid to Ask

**Abstract:** Disassembly of binary code is hard, but necessary for improving the security of binary software. Over the past few decades, research in binary disassembly has produced many tools and frameworks, which have been made available to researchers and security professionals. These tools employ a variety of strategies that grant them different characteristics. The lack of systematization, however, impedes new research in the area and makes selecting the right tool hard, as we do not understand the strengths and weaknesses of existing tools. In this paper, we systematize binary disassembly through the study of nine popular, open-source tools. We couple the manual examination of their code bases with the most comprehensive experimental evaluation (thus far) using 3,788 binaries. Our study yields a comprehensive description and organization of strategies for disassembly, classifying them as either algorithm or else heuristic. Meanwhile, we measure and report the impact of individual algorithms on the results of each tool. We find that while principled algorithms are used by all tools, they still heavily rely on heuristics to increase code coverage. Depending on the heuristics used, different coverage-vs-correctness trade-offs come in play, leading to tools with different strengths and weaknesses. We envision that these findings will help users pick the right tool and assist researchers in improving binary disassembly.


### An Empirical Study on ARM Disassembly Tools

**Abstract:** With the increasing popularity of embedded devices, ARM is becom- ing the dominant architecture for them. In the meanwhile, there is a pressing need to perform security assessments for these devices. Due to different types of peripherals, it is challenging to dynami- cally run the firmware of these devices in an emulated environment. Therefore, the static analysis is still commonly used. Existing work usually leverages off-the-shelf tools to disassemble stripped ARM binaries and (implicitly) assume that reliable disassembling binaries and function recognition are solved problems. However, whether this assumption really holds is unknown.

In this paper, we conduct the first comprehensive study on ARM disassembly tools. Specifically, we build 1, 896 ARM bina- ries (including 248 obfuscated ones) with different compilers, com- piling options, and obfuscation methods. We then evaluate them using eight state-of-the-art ARM disassembly tools (including both commercial and noncommercial ones) on their capabilities to lo- cate instructions and function boundaries. These two are funda- mental ones, which are leveraged to build other primitives. Our work reveals some observations that have not been systemati- cally summarized and/or confirmed. For instance, we find that the existence of both ARM and Thumb instruction sets, and the reuse of the BL instruction for both function calls and branches bring serious challenges to disassembly tools. Our evaluation sheds light on the limitations of state-of-the-art disassembly tools and points out potential directions for improvement. To engage the community, we release the data set, and the related scripts at https://github.com/valour01/arm_disasssembler_study.

### Speculative disassembly of binary code

**Abstract:** Embedded software is rapidly increasing in complexity. To cope with this, developers rely on third-party IPs to accel- erate product delivery. However, IP source code might not be available which limits verifiability. This creates a partic- ular challenge especially in safety-critical applications, e.g., automotive. Static Binary Analysis (SBA) is a promising technique to address such a challenge by providing engineers with the ability to reason about the actual instructions exe- cuted for all possible inputs. Disassembly is the fundamental first step for any SBA where assembly instructions are re- covered from binary code. Correct disassembly, however, is challenging since data is mixed with code in binaries. More- over, variable-size ISA, e.g., Thumb and TriCore, allow a single byte sequence to have multiple valid interpretations.

We introduce Spedi, an open source SPEculative DIsas- sembler for Thumb ISA. Spedi is based on a principled ap- proach to disassembly where all possible basic blocks are speculatively recovered. Then, basic blocks are refined using conflict analyses to identify assembly instructions. Experi- ments using a wide range of benchmarks demonstrate that Spedi is both fast and effective. It outperforms IDA Pro, the de-facto industry standard disassembler, in terms of dis- assembly correctness. Spedi can also recover the majority of the call graph and switch table targets. It is resilient to obfuscation and doesn’t use any symbol information which makes it a suitable front-end for a wide variety of SBA ap- plications including security analysis.


### Low Overhead Dynamic Binary Translation on ARM


**Abstract:** The ARMv8 architecture introduced AArch64, a 64-bit exe- cution mode with a new instruction set, while retaining binary compatibility with previous versions of the ARM architec- ture through AArch32, a 32-bit execution mode. Most hard- ware implementations of ARMv8 processors support both AArch32 and AArch64, which comes at a cost in hardware complexity.

We present MAMBO-X64, a dynamic binary translator for Linux which executes 32-bit ARM binaries using only the AArch64 instruction set. We have evaluated the performance of MAMBO-X64 on three existing ARMv8 processors which support both AArch32 and AArch64 instruction sets. The performance was measured by comparing the running time of 32-bit benchmarks running under MAMBO-X64 with the same benchmark running natively. On SPEC CPU2006, we achieve a geometric mean overhead of less than 7.5 % on in-order Cortex-A53 processors and a performance improve- ment of 1 % on out-of-order X-Gene 1 processors.

MAMBO-X64 achieves such low overhead by novel optimizations to map AArch32 floating-point registers to AArch64 registers dynamically, handle overflowing address calculations efficiently, generate traces that harness hardware return address prediction, and handle operating system sig- nals accurately.
