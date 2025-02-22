<div align="center">
    <h1>卓越的Rust安全工具</h1>
    <p>与Rust和信息安全有关的比较好的项目和资源的策划列表</p>
</div>
<br/>
 
- [English](https://github.com/enomothem/awesome-rust-security-cn/blob/master/README-EN.md)

# 目录

- [工具](#工具)
    - [Web与云安全](#Web与云安全)
    - [Vulnerability Assessment](#vulnerability-assessment)
    - [Offensive Security and Red Teaming](#offensive-security-and-red-teaming)
    - [Malware and Threat Detection](#malware-and-threat-detection)
    - [Cryptography](#cryptography)
    - [Applications](#applications)
- [Educational](#educational)
    - [Books](#books)
    - [Articles](#articles)
    - [Talks](#talks)
- [Similar Lists](#similar-lists)
- [Contributing](#contributing)

<br/>
<br/>

# 工具

## Web与云安全

### 渗透测试

- [sn0int](https://github.com/kpcyrd/sn0int) - OSINT框架与包管理器
- [sniffglue](https://github.com/kpcyrd/sniffglue) - 安全的多线程数据包嗅探器
- [badtouch](https://github.com/kpcyrd/badtouch) - 可脚本化的网络身份验证破解程序
- [rshijack](https://github.com/kpcyrd/rshijack) - TCP连接劫持器
- [feroxbuster](https://github.com/epi052/feroxbuster) - 快速、简单、递归的目录发现工具
- [rustbuster](https://github.com/phra/rustbuster) -Web模糊器和目录发现工具
- [rustscan](https://github.com/RustScan/RustScan) - 现代端口扫描器
- [kepler](https://github.com/Exein-io/kepler) - 基于NIST的CVE查找存储和Rust支持的API
- [phaser](https://github.com/skerkour/phaser) - 自动攻击面发现和漏洞扫描器
- [pdfrip](https://github.com/mufeedvh/pdfrip) - 快速PDF密码破解实用程序配备常见的密码格式构建器和字典攻击。
- [chromepass](https://github.com/darkarp/chromepass) - 破解Chrome保存的密码

### Authorization & Authentication Frameworks

- [biscuit](https://github.com/CleverCloud/biscuit) - delegated, decentralized, capabilities based authorization token
- [paseto.rs](https://github.com/instructure/paseto) - PASETO Rust implementation
- [webauthn.rs](https://github.com/kanidm/webauthn-rs) - WebAuthn implementation in Rust
- [aliri](https://github.com/neoeinstein/aliri) - JWT authenticaiton and OAuth2 scope authorization implementations for many web frameworks
- [OpenSK](https://github.com/google/OpenSK) - open-source implementation for security keys written in Rust
- [dacquiri](https://github.com/resyncgg/dacquiri) - Attributed based access control (ABAC) framework with compile-time enforcement 

### Cloud and Infrastructure

- [firecracker](https://github.com/firecracker-microvm/firecracker) - secure and fast microVMs for serverless computing
- [boringtun](https://github.com/cloudflare/boringtun) - CloudFlare's Rust implementation of WireGuard
- [innernet](https://github.com/tonarino/innernet) - private network based on WireGuard
- [vaultwarden](https://github.com/dani-garcia/vaultwarden) - unofficial BitWarden implementation in Rust

### Software Supply Chain

- [rebuilderd](https://github.com/kpcyrd/rebuilderd) - independent verification of binary packages
- [rust-tuf](https://github.com/heartsucker/rust-tuf) - Rust implementation of [the Update Framework](https://theupdateframework.io/)

### Secure Frameworks

- [adblock-rust](https://github.com/brave/adblock-rust) - Brave's Rust-based adblock engine
- [libinjection](https://github.com/arvancloud/libinjection-rs) - Rust bindings to libinjection
- [http-desync-guardian](https://github.com/aws/http-desync-guardian) - Analyze HTTP requests to minimize risks of HTTP Desync attacks
- [ammonia](https://github.com/rust-ammonia/ammonia) - Repair and secure untrusted HTML

<br/>

## Vulnerability Assessment

### Static Code Auditing

- [RustSec](https://github.com/RustSec) - organization supporting vulnerability disclosure for Rust packages, audit Cargo.lock files for dependencies
- [cargo-geiger](https://github.com/rust-secure-code/cargo-geiger) - detect usage of unsafe Rust
- [siderophile](https://github.com/trailofbits/siderophile) - find ideal fuzz targets in a Rust codebase
- [cargo-crev](https://github.com/crev-dev/cargo-crev) - cryptographically verifiable code review for cargo
- [arch-audit](https://github.com/ilpianista/arch-audit) - audit installed Arch packages for vulnerabilities
- [ripgrep](https://github.com/BurntSushi/ripgrep) - recursively search directories with regexes
- [weggli](https://github.com/googleprojectzero/weggli) - fast and robust semantic search tool for C and C++ codebases

### Fuzzing

- [rust-fuzz](https://github.com/rust-fuzz) - organization implementing cargo plugins for AFL, libFuzzer, and honggfuzz
- [LibAFL](https://github.com/AFLplusplus/LibAFL) - slot fuzzers together in Rust
- [fuzzcheck.rs](https://github.com/loiclec/fuzzcheck-rs) - structure-aware, in-process, coverage-guided, evolutionary fuzzing engine for Rust functions.
- [onefuzz](https://github.com/microsoft/onefuzz) - self-hosted Fuzzing-As-A-Service platform 
- [lain](https://github.com/microsoft/lain) - fuzzer framework implemented in Rust
- [fzero](https://github.com/gamozolabs/fzero_fuzzer) - fast grammar-based fuzz generator implementation
- [nautilus](https://github.com/RUB-SysSec/nautilus) - grammar-based feedback fuzzer from RUB's Systems Security Lab
- [sidefuzz](https://github.com/phayes/sidefuzz) - fuzzer for side-channel vulnerabilities
- [arbitrary](https://github.com/rust-fuzz/arbitrary) - trait for generating structured input from raw bytes, helpful for structure-aware fuzzing
- [rust-san](https://github.com/japaric/rust-san) - sanitizers for Rust code
- [lidiffuzz](https://github.com/Shnatsel/libdiffuzz) - memory allocator drop-in to test for uninitialized memory reads
- [rewind](https://github.com/quarkslab/rewind) - Snapshot-based coverage-guided Windows kernel fuzzer
- [hyperpom](https://github.com/impalabs/hyperpom) - AArch64 fuzzer based on the Apple Silicon hypervisor

### 二进制分析 & 逆向

- [goblin](https://github.com/m4b/goblin) - binary parsing crate for Rust
- [unicorn.rs](https://github.com/unicorn-rs/unicorn-rs) - Rust bindings to the Unicorn framework
- [cargo-call-stack](https://github.com/japaric/cargo-call-stack) - whole program stack analysis
- [xori](https://github.com/endgameinc/xori) - disassembly library for PE32, 32+ and shellcode
- [rd](https://github.com/sidkshatriya/rd) - record/replay debugger implemented in Rust
- [binsec](https://github.com/ex0dus-0x/binsec) - Swiss Army Knife for Binary (In)Security
- [radeco](https://github.com/radareorg/radeco) - Radare2-based decompiler and symbol executor
- [falcon](https://github.com/falconre/falcon) - Binary Analysis Framework in Rust
- [mesos](https://github.com/gamozolabs/mesos) - binary coverage tool without modification for Windows
- [guerilla](https://github.com/mehcode/guerrilla) - monkey patching Rust functions
- [ropr](https://github.com/Ben-Lichtman/ropr) - blazing fast™ multithreaded ROP Gadget finder
- [pwninit](https://github.com/io12/pwninit) - automate starting binary exploit challenges
- [binaryninja-rs](https://github.com/Vector35/binaryninja-api/tree/dev/rust) - Binary Ninja API support for Rust

### Property-Based Testing

- [quickcheck](https://github.com/BurntSushi/quickcheck) - property-based testing for Rust
- [proptest](https://github.com/AltSysrq/proptest) - Hypothesis-like property testing for Rust
- [bughunt-rust](https://github.com/blt/bughunt-rust) - example of using fuzzing QuickCheck models for bughunting
- [mutagen](https://github.com/llogiq/mutagen) - mutation testing framework for Rust

### Symbolic Execution

- [seer](https://github.com/dwrensha/seer) - symbolic execution engine for Rust
- [haybale](https://github.com/PLSysSec/haybale) - LLVM IR-based symbolic execution engine from the USCD System Security Lab

### Formal Verification

- [MIRAI](https://github.com/facebookexperimental/MIRAI) - abstract interpreter for Rust's MIR from Facebook
- [electrolysis](https://github.com/Kha/electrolysis) - formal verification of Rust programs with the Lean theorem prover

<br/>

## Offensive Security and Red Teaming

### Command-and-Control Frameworks

- [tetanus](https://github.com/MythicAgents/tetanus) - Mythic agent written in Rust 

### Defense Evasion

- [FunctionStomping](https://github.com/Idov31/FunctionStomping) - new shellcode injection technique.

### Packing, Obfuscation, Encryption, Anti-analysis

- [debugoff](https://github.com/0xor0ne/debugoff) - Linux anti-debugging and
  anti-analysis rust library
- [goldberg](https://github.com/frank2/goldberg) - procedural macro library for
  obfuscating Rust code.
- [obfstr](https://github.com/CasualX/obfstr) - string obfuscation for Rust
- [oxide](https://github.com/frank2/oxide) - PoC packer written in Rust.
- [Linux.Fe2O3](https://github.com/guitmz/Fe2O3) - Simple ELF prepender virus / in-memory loader written in Rust

<br/>

## Threat Detection & Forensics

- [yara-rust](https://github.com/Hugal31/yara-rust) - Rust bindings to YARA
- [BONOMEN](https://github.com/0xcpu/bonomen) - hunt for malware critical process impersonation
- [confine](https://github.com/ex0dus-0x/confine) - sandbox for threat detection
- [redbpf](https://github.com/foniod/redbpf) - crate for writing BPF/eBPF modules
- [cernan](https://github.com/postmates/cernan) - telemetry aggregation and shipping
- [chainsaw](https://github.com/countercept/chainsaw) - Windows Event Log Hunting
- [foniod](https://github.com/foniod/foniod) - Data first monitoring agent using (e)BPF, built on RedBPF
- [zerotect](https://github.com/polyverse/zerotect) - attack/exploit Detector that utilizes Polymorphism and Diversity
- [hayabusa](https://github.com/Yamato-Security/hayabusa) - Sigma-based threat hunting and fast forensics timeline generator for Windows event logs written in Rust.
- [medusa](https://github.com/evilsocket/medusa) - fast and secure multi protocol honeypot.

<br/>

## Cryptography

### Frameworks

- [secrets](https://github.com/stouset/secrets) - secure storage for cryptographic secrets in Rust
- [mundane](https://github.com/google/mundane) - BoringSSL-backed cryptography library
- [rust-threshold-secret-sharing](https://github.com/snipsco/rust-threshold-secret-sharing) - Rust implementation of threshold-based secret sharing
- [molasses](https://github.com/trailofbits/molasses) - Rust implementation of the MLS group messaging protocol
- [rust-security-framework](https://github.com/kornelski/rust-security-framework) - Rust bindings to the macOS `Security.framework`
- [microkv](https://github.com/ex0dus-0x/microkv) - minimal and secure key-value storage for Rust
- [swanky](https://github.com/GaloisInc/swanky) - suite of rust libraries for secure multi-party computation
- [tandem](https://github.com/sine-fdn/tandem) - maliciously secure two-party computation engine which is embeddable and accessible

## Applications

- [ripasso](https://github.com/cortex/ripasso/) - password manager written in Rust
- [sekey](https://github.com/sekey/sekey) - TouchID / Secure Enclave for SSH authentication
- [Mullvad VPN Client](https://github.com/mullvad/mullvadvpn-app) - Mullvad VPN app written in Rust
- [fakio](https://github.com/SerhoLiu/fakio) - lightweight secure tunnel proxy.
- [firecracker](https://github.com/firecracker-microvm/firecracker) - Secure and fast microVMs for serverless computing.

<br/>

# Educational

## Books

- [Black Hat Rust](https://github.com/skerkour/black-hat-rust)
- [Rust Fuzz Book](https://rust-fuzz.github.io/book/)
- [Secure Rust Guidelines](https://anssi-fr.github.io/rust-guide/)

## Articles

- [str::repeat wildcopy exploit writeup](https://saaramar.github.io/str_repeat_exploit/)
- [Introduction to Fuzzing Rust code](https://fuzzinglabs.com/introduction-rust-fuzzing-tutorial/)

## Talks

- [BlackHat EU 2018 - RustZone: Writing Trusted Applications in Rust](https://www.youtube.com/watch?v=9wLgXfo0l1g)
- [DEFCON 30 - Lessons from fuzzing a smart contract compiler](https://www.youtube.com/watch?v=8E7XOHQiRPE)

<br/>

# Similar Lists

- [awesome-rust](https://github.com/rust-unofficial/awesome-rust)
- [rust-secure-code/projects](https://github.com/rust-secure-code/projects)
- [analysis-tools-dev/static-analysis](https://github.com/analysis-tools-dev/static-analysis)
- [analysis-tools-dev/dynamic-analysis](https://github.com/analysis-tools-dev/dynamic-analysis)
- [awesome-go-security](https://github.com/Binject/awesome-go-security)

<br/>

# Contributing

Make a pull request if you are interested in adding more to this list! All contributions are appreciated.
