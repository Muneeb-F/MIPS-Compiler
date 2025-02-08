# C++ Compiler for MIPS

## Overview
A comprehensive, custom-built compiler for a subset of the C++ programming language, optimized for MIPS architecture. This project implements a full compiler pipeline, including:

- **Lexical Analysis**: Tokenization of C++ code into meaningful symbols.
- **Parsing**: Robust syntax analysis using LR(1) parsing.
- **Semantic Analysis**: Validation of syntax trees against C++ language rules.
- **Code Generation**: Efficient machine code generation for MIPS.

This compiler ensures optimized performance, strict adherence to language rules, and efficient execution.

---

## Features

### **Lexical Analysis**
- Tokenizes source code into keywords, identifiers, operators, and symbols.
- Ignores whitespace and comments for a clean token stream.
- Supports identifiers (`ID`), numeric literals (`NUM`), operators (`+ - * / % == != <= >= < >`), and keywords (`RETURN, IF, ELSE, WHILE`).

### **Parsing**
- Implements **LR(1) parsing** for robust syntax validation.
- Structures programs into procedures, declarations, control structures, and expressions.
- Supports control flow statements: `if` (mandatory `else`), `while`, and `return`.

### **Semantic Analysis**
- Enforces context-sensitive rules, such as:
  - Unique procedure names.
  - Declaration before use.
  - Type correctness in expressions and assignments.
  - Strict function call conventions.
- Supports recursion, but **mutual recursion is not allowed**.

### **Code Generation**
- Produces highly optimized **MIPS machine code**.
- Implements dynamic memory management using `new` and `delete[]`.
- Ensures efficient execution with a streamlined instruction set.

---

## **Supported Language Specifications**
This compiler supports a **tailored subset of C++**, focusing on fundamental programming concepts:

### **Variable Declarations**
- Supports `int` and `int*`.
- Requires initialization with an **unsigned integer constant** or `NULL`.

### **Statements & Expressions**
- Includes:
  - Variable names.
  - Memory allocation (`new`).
  - Unary operators (`&`, `*`).
  - Binary operators (`+ - * / % == != <= >= < >`).

### **Memory Management**
- Supports **dynamic allocation** with `new`.
- Implements **safe deallocation** using `delete[]`.

### **Function Design**
- **Mandatory single return statement** at the end of each function.
- Functions must have well-defined parameter and return types.

---

## **Compiler Architecture**

### **Lexical Syntax**
The compiler follows a rigorous lexical structure, ensuring token clarity and case sensitivity. The lexer converts source code into structured tokens, handling identifiers, keywords, and operators efficiently.

### **Context-free Grammar**
The parsing phase enforces structured C++ grammar, ensuring:
- Proper scoping and nesting of control structures.
- Well-defined function signatures.
- Separation between **declarations** and **statements**.

### **Context-sensitive Rules**
- **No undeclared variables**: Every variable must be declared before use.
- **Strict type checking**: All expressions must match expected data types.
- **Single return statement**: Each function requires a single return at the end.

### **Semantic Validation**
This compiler guarantees that valid programs not only meet syntactic rules but also maintain **C++-standard semantics**, ensuring predictable execution in MIPS environments.

---

## **Source Code**
Due to this project being associated with the CS Department at the Unverisity of Waterloo, the code is in a private repository. IF you'd like to see it, please contact me.

---

