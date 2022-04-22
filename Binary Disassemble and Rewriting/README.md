
# Paper list:


## Suvery and Overview:

### x86-64

- [An In-Depth Analysis of Disassembly on Full-Scale x86/x64 Binaries (USENIX, 2016)](https://github.com/LmDeng0/Paper/blob/main/Binary%20Disassemble%20and%20Rewriting/Suvery%20and%20Overview/An%20In-Depth%20Analysis%20of%20Disassembly%20on%20Full-Scale%20x86:x64%20Binaries.pdf)

- [SoK:All You Ever Wanted to Know About x86:x64 Binary Disassembly But Were Afraid to Ask (IEEE Symposium on Security and Privacy, 2021)](https://github.com/LmDeng0/Paper/blob/main/Binary%20Disassemble%20and%20Rewriting/Suvery%20and%20Overview/SoK-%20All%20You%20Ever%20Wanted%20to%20Know%20About%20x86:x64%20Binary%20Disassembly%20But%20Were%20Afraid%20to%20Ask.pdf)

### ARM

- [An Empirical Study on ARM Disassembly Tools (SIGSOFT, 2020)](./Suvery%20and%20Overview/An%20Empirical%20Study%20on%20ARM%20Disassembly%20Tools.pdf)


## Binary Disassemble and Rewriting:


- [Speculative disassembly of binary code (CASES , 2016)](https://github.com/LmDeng0/Paper/blob/main/Binary%20Disassemble%20and%20Rewriting/Research/Speculative%20disassembly%20of%20binary%20code.pdf)
- 
Spedi is a speculative disassembler for the variable-size Thumb ISA
[Abstract](#Speculative-disassembly-of-binary-code)

## Binary Translator:

- [Low Overhead Dynamic Binary Translation on ARM (CCS, 2006)](https://github.com/LmDeng0/Paper/blob/main/Binary%20Disassemble%20and%20Rewriting/Research/Low%20Overhead%20Dynamic%20Binary%20Translation%20on%20ARM.pdf)

将AArch32转换为AArch64指令


- [A Retargetable Static Binary Translator for the ARM Architecture](https://github.com/LmDeng0/Paper/blob/main/Binary%20Disassemble%20and%20Rewriting/Research/A%20Retargetable%20Static%20Binary%20Translator%20for%20the%20ARM%20Architecture.pdf)


# Conclusion about Paper：

An Empirical Study on ARM Disassembly Tools.

- [Fuzzing: Hack, Art, and Science](#fuzzing-hack-art-and-science-cacm-2020)

[Detail notes](https://www.notion.so/An-Empirical-Study-on-ARM-Disassembly-Tools-43b4857a733e45589733bbefe3ad1a6b)



## Abstract:



### Speculative disassembly of binary code

Embedded software is rapidly increasing in complexity. To cope with this, developers rely on third-party IPs to accel- erate product delivery. However, IP source code might not be available which limits verifiability. This creates a partic- ular challenge especially in safety-critical applications, e.g., automotive. Static Binary Analysis (SBA) is a promising technique to address such a challenge by providing engineers with the ability to reason about the actual instructions exe- cuted for all possible inputs. Disassembly is the fundamental first step for any SBA where assembly instructions are re- covered from binary code. Correct disassembly, however, is challenging since data is mixed with code in binaries. More- over, variable-size ISA, e.g., Thumb and TriCore, allow a single byte sequence to have multiple valid interpretations.

We introduce Spedi, an open source SPEculative DIsas- sembler for Thumb ISA. Spedi is based on a principled ap- proach to disassembly where all possible basic blocks are speculatively recovered. Then, basic blocks are refined using conflict analyses to identify assembly instructions. Experi- ments using a wide range of benchmarks demonstrate that Spedi is both fast and effective. It outperforms IDA Pro, the de-facto industry standard disassembler, in terms of dis- assembly correctness. Spedi can also recover the majority of the call graph and switch table targets. It is resilient to obfuscation and doesn’t use any symbol information which makes it a suitable front-end for a wide variety of SBA ap- plications including security analysis.



### Fuzzing: Hack, Art, and Science (CACM 2020)

* <img src="image/pdf_24px.png">[Paper](./Paper/CACM20_Fuzzing.pdf)

**Abstract:** Fuzzing, or fuzz testing, is the process of finding security vulnerabilities in input-parsing code by repeatedly testing the parser with modified, or fuzzed, inputs.35 Since the early 2000s, fuzzing has become a mainstream practice in assessing software security. Thousands of security vulnerabilities have been found while fuzzing all kinds of software applications for processing documents, images, sounds, videos, network packets, Web pages, among others. These applications must deal with untrusted inputs encoded in complex data formats. For example, the Microsoft Windows operating system supports over 360 file formats and includes millions of lines of code just to handle all of these.
