
# Paper list:


## Suvery and Overview:

### x86-64

- [An In-Depth Analysis of Disassembly on Full-Scale x86/x64 Binaries (USENIX, 2016)](./Suvery%20and%20Overview/An%20In-Depth%20Analysis%20of%20Disassembly%20on%20Full-Scale%20x86:x64%20Binaries.pdf) <font color=red>[[Abstract]](#An-In-Depth-Analysis-of-Disassembly-on-Full-Scale-x86-x64-Binaries)</font>

- [SoK:All You Ever Wanted to Know About x86:x64 Binary Disassembly But Were Afraid to Ask (IEEE Symposium on Security and Privacy, 2021)](./Suvery%20and%20Overview/SoK-%20All%20You%20Ever%20Wanted%20to%20Know%20About%20x86:x64%20Binary%20Disassembly%20But%20Were%20Afraid%20to%20Ask.pdf)[Anstract]

### ARM

- [An Empirical Study on ARM Disassembly Tools (SIGSOFT, 2020)](./Suvery%20and%20Overview/An%20Empirical%20Study%20on%20ARM%20Disassembly%20Tools.pdf)[Anstract]


## Binary Disassemble and Rewriting:


- [Speculative disassembly of binary code (CASES , 2016)](./Research/Speculative%20disassembly%20of%20binary%20code.pdf)[Abstract](#Speculative-disassembly-of-binary-code)

     Spedi is a speculative disassembler for the variable-size Thumb ISA


## Binary Translator:

- [Low Overhead Dynamic Binary Translation on ARM (CCS, 2006)](./Research/Low%20Overhead%20Dynamic%20Binary%20Translation%20on%20ARM.pdf)

将AArch32转换为AArch64指令


- [A Retargetable Static Binary Translator for the ARM Architecture](./Research/A%20Retargetable%20Static%20Binary%20Translator%20for%20the%20ARM%20Architecture.pdf)


# Conclusion about Paper：

An Empirical Study on ARM Disassembly Tools.

[Detail notes](https://www.notion.so/An-Empirical-Study-on-ARM-Disassembly-Tools-43b4857a733e45589733bbefe3ad1a6b)



## Abstract:

### An In Depth Analysis of Disassembly on Full Scale x86 x64 Binaries

**Abstract:** It is well-known that static disassembly is an unsolved problem, but how much of a problem is it in real software— for instance, for binary protection schemes? This work studies the accuracy of nine state-of-the-art disassemblers on 981 real-world compiler-generated binaries with a wide variety of properties. In contrast, prior work focuses on isolated corner cases; we show that this has led to a widespread and overly pessimistic view on the prevalence of complex constructs like inline data and overlapping code, leading reviewers and researchers to underestimate the potential of binary-based research. On the other hand, some constructs, such as function boundaries, are much harder to recover accurately than is reflected in the litera- ture, which rarely discusses much needed error handling for these primitives. We study 30 papers recently pub- lished in six major security venues, and reveal a mismatch between expectations in the literature, and the actual ca- pabilities of modern disassemblers. Our findings help improve future research by eliminating this mismatch.


### Speculative disassembly of binary code

**Abstract:** Embedded software is rapidly increasing in complexity. To cope with this, developers rely on third-party IPs to accel- erate product delivery. However, IP source code might not be available which limits verifiability. This creates a partic- ular challenge especially in safety-critical applications, e.g., automotive. Static Binary Analysis (SBA) is a promising technique to address such a challenge by providing engineers with the ability to reason about the actual instructions exe- cuted for all possible inputs. Disassembly is the fundamental first step for any SBA where assembly instructions are re- covered from binary code. Correct disassembly, however, is challenging since data is mixed with code in binaries. More- over, variable-size ISA, e.g., Thumb and TriCore, allow a single byte sequence to have multiple valid interpretations.

We introduce Spedi, an open source SPEculative DIsas- sembler for Thumb ISA. Spedi is based on a principled ap- proach to disassembly where all possible basic blocks are speculatively recovered. Then, basic blocks are refined using conflict analyses to identify assembly instructions. Experi- ments using a wide range of benchmarks demonstrate that Spedi is both fast and effective. It outperforms IDA Pro, the de-facto industry standard disassembler, in terms of dis- assembly correctness. Spedi can also recover the majority of the call graph and switch table targets. It is resilient to obfuscation and doesn’t use any symbol information which makes it a suitable front-end for a wide variety of SBA ap- plications including security analysis.


