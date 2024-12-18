# Rust, Go, Scala 比較
  
以下是我從 Rust, Go, 與 Scala 的過往經驗的比較。筆者 Java 經驗停在 JDK 8 前的版本，之後轉用 Scala；Scala 之後就以 Go 為主。Scala 版本，筆者是停留在 2.11 版本，因此如果對 Scala 的理解有錯，還請指正。
  
:+1: 是我非常喜歡的程式語言特性。
  
| 比較 | Rust | Go | Scala |
| - | - | - | - |
| Artifact | Machine Code | Machine Code with **Go Runtime**，也因此檔案會比較大 | JVM Bytecode |
| 跨平台 | Y | Y | Y (依賴 JVM) |
| Garbage Collection (GC) | **N** | Y | Y |
| Object-Oriented Programming| N (沒有繼承) | N (沒有繼承) | Y |
| :+1: **Functional Programming (FP)** | **Y** | Y (支援程度不如 Rust / Scala) | Y |
| :+1: **Generic (泛型)** | **Y** | Y (Go 1.18 之後版本，目前還在進步中，支援功能，遠遠不及 Rust / Scala) | Y |
| Unsigned 型別 | Y | Y | N |
| Unit 型別 | **Y** `()` | N | Y `Unit` |
| :+1: **NULL** | **N**, use `Option` instead  | Yes, `nil` | N, use `Option` instead |
| :+1: **Tuple** | **Y** | Y (只支援在 **return** 時回傳多組值) | Y |
| :+1: **Interface** | **Y** (Trait) | Y (Interface) | Y (Trait) |
| :+1: **Default Function in Interface** | **Y** | N (不能在 interface 實作 function) | Y |
| :+1: **Enum** | **Y** | N (只能用 const + iota 模擬) | Y |
| :+1: **Macro** | **Y** | N | Y |
| Inline | **Y** | N (Go compiler 會自動判斷是否要 inline [^go_inline]) | Y |
| :+1: **Pattern Matching** | **Y** | N | Y |
| :+1: **if-then-else** | **expression (可 return 值)** | statement | expression (可 return 值) |
| :+1: **Operator Overloading** | **Y** | N | Y |
| Concurrency / Parallel / Async | thread / async / channel / actor | goroutine / channel / wait group | thread / async / actor |
| :+1: **Error Handling** | **Result** / **Option** | Error | Try / Either / Option |
| Syntactic Sugar (語法糖) | 中 | 弱 | 太強 (會像在寫天書) |
| Package 管理 | 較複雜，但也更有彈性 | 較簡單 | 較簡單 |
| Coding Style | camel (Struct & Trait) and snake (Varible & Function) | camel | camel |
  
[^go_inline]: [Compiler And Runtime Optimizations](https://go.dev/wiki/CompilerOptimizations)
