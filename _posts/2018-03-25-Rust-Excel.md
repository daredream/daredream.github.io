
# Experiments with Rust and Calamine (Excel API)

The idea that in certain situations, auto-generating scripting languages, such as Python, 
Javascript, Perl, HTML5/CSS3 etc., particularly by a stable statically-typed language
with a promising future, and especially with support for DSL syntax and design pattern
abstractions, has recently become appealing/interesting to me. 

I am also exploring reading spreadsheets using Excel as a standard data interchange
format using the Rust language.  So far, I like the functional language idioms. 
Other features of note from [Rust Language][https://www.rust-lang.org/en-US/]]:

* zero-cost abstractions
* move semantics
* guaranteed memory safety
* threads without data races
* trait-based generics
* pattern matching
* type inference
* minimal runtime
* efficient C bindings

Maybe I am just getting "bored"/jaded with virtual machine byte-code interpreted languages?

### Reader: Simple

```rust
use calamine::{Reader, Xlsx, open_workbook};

let mut excel: Xlsx<_> = open_workbook("file.xlsx").unwrap();
if let Some(Ok(r)) = excel.worksheet_range("Sheet1") {
    for row in r.rows() {
        println!("row={:?}, row[0]={:?}", row, row[0]);
    }
}
```


