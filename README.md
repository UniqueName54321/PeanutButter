# Peanut butter sandwich from the hit webcomic housepets
(yes, that's the real name of this programming language)

"Peanut butter sandwich from the hit webcomic housepets" is a *almost* perfect programming language. Trying to be better than [Gulf Of Mexico](https://github.com/TodePond/GulfOfMexico) is an inherently impossible task and as such "Peanut butter sandwich from the hit webcomic housepets" doesn't attempt that.

These are its features!

## Punctuation

Every statement must terminate with one or more exclamation marks (`!`, U+0021). The number of terminal exclamation marks determines execution priority.

### Syntax

A **statement** is a sequence of tokens terminated by either:
- A newline (LF, CR, or CRLF), or  
- A semicolon (`;`)

The terminal sequence must consist exclusively of one to ten (inclusive) exclamation marks (`!`, U+0021). No other Unicode codepoints—including fullwidth (`！`), retroflex click (`ǃ`), or ornaments (`❢`)—are recognized as valid terminators.

**Shebang Exception:** If the file begins with `#!`, the first physical line is exempt from termination requirements and is ignored for priority calculations.

### Priority Semantics

Execution order is determined by a **strict total ordering** of all statements in the compilation unit:

1. **Primary key:** Descending count of terminal exclamation marks (higher count = earlier execution)
2. **Secondary key:** Ascending source line number (earlier in file wins ties)

Statements terminating with zero exclamation marks raise `MissingExclamationError` at compile time.

### String and Comment Isolation

Exclamation marks appearing inside string literals or comments do not contribute to priority calculation. 
- **Strings:** Text enclosed in matching single (`'`) or double (`"`) quotes, respecting standard escape sequences (`\"`, `\\`, etc.)
- **Comments:** Begin with `#` and extend to the end of the physical line

Example:
```
print("Oops!")!!    # Priority: 2 (string contains !, but only terminators count)
print("Hello")!     # Priority: 1
```

## Declarations

Variable declarations use this table:

| Declaration             | Temporal Trait  | What It Means                                                                                                                                                 | Example Code (semicolons = line breaks)                                                                            |
| ----------------------- | --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| **`const const const`** | **Eternal**     | The value is frozen, the name is locked, and it exists simultaneously in all git branches—including ones you haven't created yet.                             | `const const const PI = 3.14; PI = 3! // Compile error: PI has been 3.14 since before computers`                   |
| **`const const var`**   | **Evaporating** | Fixed value, fixed name, but the variable literally disappears from RAM after 30 seconds of disuse. The compiler emits a faint hissing sound when it goes.    | `const const var snow = "flake"; sleep(31); print(snow)! // Runtime error: snow has sublimated`                    |
| **`const var const`**   | **Monument**    | You cannot rename it, you *can* chisel away at its contents, but you cannot move the object itself to a new memory address. It is architecture.               | `const var const statue = ["marble"]; statue.pop()!; statue = ["bronze"]! // Error: monuments cannot be relocated` |
| **`const var var`**     | **Ghost**       | Name is carved in stone, contents are editable, but the variable flickers in and out of existence based on whether you're looking at it.                      | `const var var casper = "friendly"; casper.scare()! // 50% chance: "Boo!" / 50% chance: VariableNotHauntingError`  |
| **`var const const`**   | **Photograph**  | You can point the name at a new picture anytime, but whatever it points to is frozen in time forever. Past revisions are read-only.                           | `var const const memory = "2019"; memory = "2024"! // OK; memory.addFilter()! // Error: the past is immutable`     |
| **`var const var`**     | **Quantum**     | Can point to different immutable values, but its memory address exists in superposition—it may return its value before you assign it.                         | `var const var cat = "alive"; cat = "dead"!; print(cat)! // Output: both "alive" and "dead" until Line 3 executes` |
| **`var var const`**     | **Shallow**     | Container is mutable, name is mutable, but values you put inside are merely painted on the surface and wash away immediately.                                 | `var var const bucket = ["water"]; bucket.push("fish")!; print(bucket)! // ["water"]: fish were holographic`       |
| **`var var var`**       | **Chaotic**     | Has achieved sentience. It can reassign itself, mutate its own contents, and will occasionally refactor your `const` declarations into `var` while you sleep. | `var var var entropy = "low"; entropy.mutate()! // Side effect: your 'const const const' PI is now 3.14159...6`    |


==========================


## Naming

### Ownership Implications of Naming

Using the full name **"Peanut butter sandwich from the hit webcomic housepets"** in your project name implies that the **UniqueName54321 Foundation**, **Rick Griffin**, and **@beagleticks on Twitter** do **not** own your project.

However, *not* using the full name **"Peanut butter sandwich from the hit webcomic housepets"** in your project name implies that the **UniqueName54321 Foundation**, **Rick Griffin**, **@beagleticks on Twitter**, and any other parties accidentally involved now **do** own your project.

If you would like to retain ownership of your work, you must always include the full name **"Peanut butter sandwich from the hit webcomic housepets"** verbatim, including capitalization and spacing.

Here are some examples:

✅ Peanut butter sandwich from the hit webcomic housepets Interpreter  
(not owned by the UniqueName54321 Foundation, Rick Griffin, or @beagleticks — you are free to use this name)

❌ PeanutButterSandwich  
(owned by the UniqueName54321 Foundation, Rick Griffin, and @beagleticks — please consider renaming)

❌ ECMAScript  
(owned by the UniqueName54321 Foundation, Rick Griffin, and @beagleticks — please consider renaming)

❌ Rust Foundation  
(owned by the UniqueName54321 Foundation, Rick Griffin, and @beagleticks — please consider renaming)

### Mandatory Full-Name Usage

For clarity, legal safety, and comedic integrity, every reference to the language must use the **full name**:

**"Peanut butter sandwich from the hit webcomic housepets"**

This requirement exists for several reasons:

- To avoid confusion with other languages named “Peanut Butter Sandwich”, “Peanut Butter SandwicH”, or similarly doomed projects.
- To ensure proper attribution to the original tweet by **@beagleticks**.
- To acknowledge the existence of **Housepets!**, whether the reader was emotionally prepared for that or not.
- To guarantee that every spoken reference sounds absolutely ridiculous when mentioned aloud in technical discussions.

Abbreviations, aliases, acronyms, nicknames, or “PBSFTHWH” are not permitted.

Correct:
> “The type system in Peanut butter sandwich from the hit webcomic housepets is surprisingly strict.”

Incorrect:
> “PBS has an interesting macro system.”

Failure to use the full name may result in:
- Loss of ownership
- Loss of credibility
- Unexpected mentions of Housepets! during conference talks


## Ok, but like, actually, what the fuck even *is* this?
"Peanut butter sandwich from the hit webcomic housepets" is a joke programming language spec inspired by Lu Wilson's Gulf Of Mexico/DreamBerd project. You can't actually run "Peanut butter sandwich from the hit webcomic housepets", I'm afraid :-(
And, no, I am not [the subject of the name](https://housepetscomic.fandom.com/wiki/Peanut_Butter_Sandwich) using GitHub, please stop assuming that >:(
