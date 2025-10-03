# 🌱 What Are Abstract Syntax Expressions (ASE)?

Most programming languages look like sentences. Lisp looks like math in parentheses:

```
(+ (* 2 3) 4)
```

This can be powerful, but also hard to read.

**Abstract Syntax Expressions (ASE)** are like Lisp expressions, but written in a
cleaner, indentation-based way.

---

## ✨ The Three Rules of ASE

1. **Every expression starts with a name (an atom).**

   * Example:

     ```
     MUL
         x
         y
     ```

     means `(MUL x y)` in Lisp form.

2. **Indentation shows structure.**

   * Children are indented under their parent atom.
   * Example:

     ```
     ADD
         MUL
             x
             y
         
         POW
             z
             2
     ```

     means `(ADD (MUL x y) (POW z 2))`.

3. **No extra parentheses are needed.**

   * Indentation *is* the parentheses.
   * The script is easier to read at a glance, like an outline or a tree.

---

## 🌀 Why ASE Matters

ASE has expressive power equivalent to the S-expressions subset restricted to contain only an
atom at each beginning of any list whereas each list is required to hold more than one atom.
Such restrictions make ASE:

* **Readable**: looks like a tree of ideas, not a puzzle of brackets.
* **Minimal**: only atoms + indentation, no extra syntax.

---

## 🧰 Additional Practical Extensions

* If we want an atom to contain a whitespace or a special character, we enclose it between a
  pair of `'` characters.
* Single-line strings are enclosed within a pair of `"` characters.
* Multi-line strings are vertically enclosed within a pair of an odd number of `"` characters.
* Comments are indicated by a double star, following the indentation:
  * If a line begins with `**`, then the line and all its indented children are ignored.
  * Commented lines may contain any characters, including whitespace.

---

## 🛠️ Resources

* [ASE parser pseudocode](https://github.com/tearflake/ase/blob/main/src/ase.pseudo)

