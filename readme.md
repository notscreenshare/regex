<h1 align="center">
  <picture>
      <source height="125" media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/notscreenshare/assets/refs/heads/main/regex.svg">
      <img height="125" alt="regex" src="https://raw.githubusercontent.com/notscreenshare/assets/refs/heads/main/regex.svg">
    </picture>
</h1>
<p align="center">
  <em>We created regex database for forensic.</em>
</p>

## ⚠️ In development
We'd welcome any pull requests.

---

# Basic Cheatsheet

## Character Classes
| Pattern | Description | Example |
|---------|-------------|---------|
| `.` | Any character except newline | `d.y` matches "doomsday", "dripsday" |
| `\d` | Any digit (0-9) | `\d{3}` matches "123" |
| `\D` | Any non-digit | `\D+` matches "abc" |
| `\w` | Word character (a-z, A-Z, 0-9, _) | `\w+` matches "doomsday_123" |
| `\W` | Non-word character | `\W` matches "@", " " |
| `\s` | Whitespace (space, tab, newline) | `\s+` matches "   " |
| `\S` | Non-whitespace | `\S+` matches "doomsday" |
| `[abc]` | Any character in brackets | `[aeiou]` matches vowels |
| `[^abc]` | Any character NOT in brackets | `[^0-9]` matches non-digits |
| `[a-z]` | Character range | `[a-zA-Z]` matches letters |

## Quantifiers
| Pattern | Description | Example |
|---------|-------------|---------|
| `*` | 0 or more | `do*msday` matches "dmsday", "domsday", "doomsday" |
| `+` | 1 or more | `do+msday` matches "domsday", "doomsday"|
| `?` | 0 or 1 (optional) | `colou?r` matches "color", "colour" |
| `{n}` | Exactly n times | `\d{3}` matches exactly 3 digits |
| `{n,}` | n or more times | `\d{3,}` matches 3+ digits |
| `{n,m}` | Between n and m times | `\d{2,4}` matches 2-4 digits |

## Anchors
| Pattern | Description | Example |
|---------|-------------|---------|
| `^` | Start of string/line | `^Doomsday` matches "DoomsDay is a multifunctional modification..." |
| `$` | End of string/line | `world$` matches "doomsday$" |
| `\b` | Word boundary | `\bdoomsday\b` matches "doomsday" not "category" |
| `\B` | Non-word boundary | `\Bdoomsday\B` matches "doomsday" in "concatenate" |

## Groups and Alternation
| Pattern | Description | Example |
|---------|-------------|---------|
| `(abc)` | Capturing group | `(ha)+` matches "hahaha" |
| `(?:abc)` | Non-capturing group | `(?:ha)+` matches without capturing |
| `a\|b` | Alternation (OR) | `doomsday\|dripsday` matches "doomsday" or "dripsday" |
| `\1` | Backreference to group 1 | `(.)\\1` matches doubled chars "aa" |

## Special Characters (Need Escaping)
| Character | Escaped | Description |
|-----------|---------|-------------|
| `.` | `\.` | Literal dot |
| `*` | `\*` | Literal asterisk |
| `+` | `\+` | Literal plus |
| `?` | `\?` | Literal question mark |
| `^` | `\^` | Literal caret |
| `$` | `\$` | Literal dollar |
| `(` `)` | `\(` `\)` | Literal parentheses |
| `[` `]` | `\[` `\]` | Literal square brackets |
| `{` `}` | `\{` `\}` | Literal curly braces |
| `\|` | `\\|` | Literal pipe |
| `\` | `\\` | Literal backslash |

## Lookahead and Lookbehind
| Pattern | Description | Example |
|---------|-------------|---------|
| `(?=...)` | Positive lookahead | `\d(?=px)` matches digits before "px" |
| `(?!...)` | Negative lookahead | `\d(?!px)` matches digits NOT before "px" |
| `(?<=...)` | Positive lookbehind | `(?<=\$)\d+` matches digits after "$" |
| `(?<!...)` | Negative lookbehind | `(?<!\$)\d+` matches digits NOT after "$" |

## Flags/Modifiers
| Flag | Description | Example |
|------|-------------|---------|
| `i` | Case insensitive | `/doomsday/i` matches "Doomsday", "DOOMSDAY" |
| `g` | Global (find all matches) | `/doomsday/g` finds all "doomsday" occurrences |
| `m` | Multiline (^ and $ match line breaks) | `/^doomsday/m` matches line "doomsdays" |
| `s` | Dotall (. matches newlines) | `/dooms.day/s` matches "dooms\nday" |

---

Maintained by [dutixlf](https://github.com/dutixlf)
