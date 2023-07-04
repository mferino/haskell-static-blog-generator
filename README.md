# Commands

## Compilations

```sh

  # COMPILATION

  # to compile a program use ghc <source_file.hs> 
  > ghc hello.hs

  # we run with ./hello.hs
  > ./hello.hs

  # INTEPRETATION (Preferred method for this course)

  # run the source file directly
  > runghc hello.hs
```

## GHCI

```sh
  # GHCI (REPL)
  # run a REPL with ghci
  > ghci

  GHCi, version 9.2.7: https://www.haskell.org/ghc/  :? for hel
  ghci> 1 + 1
  2
  ghci>

  # run multi line command by wrapping with :{ and :}
  ghci> :{
  | escape :: String -> String
  | escape =
  |   let
  |     escapeChar c =
  |       case c of
  |         '<' -> "&lt;"
  |         '>' -> "&gt;"
  |         '&' -> "&amp;"
  |         '"' -> "&quot;"
  |         _ -> [c]
  # and so on ...

  # VARIOUS COMMANDS
  # to load a file use :load or :l for short
  ghci> :load Html.hs
  [1 of 1] Compiling Html             ( Html.hs, interpreted )
  Ok, one module loaded.

  # to import a library use import <Library>
  ghci> import Data.Bits
  ghci> shiftL 32 1
  64

  # to check the type of something use :type
  ghci> :type escape
  escape :: String -> String

  # to leave use :quit or :q for short
  ghci> :quit
  Leaving GHCi.

  # For more information about GHCi check out the docs:
  # https://downloads.haskell.org/ghc/latest/docs/users_guide/ghci.html
```

## Markdown Syntax

```
Headings: prefix by a number of * characters
Paragraphs: a group of lines without empty lines in between
Unordered lists: a group of lines, each prefixed with -
Ordered lists: a group of lines, each prefixed with #
Code blocks: a group of lines, each prefixed with >
```

# Lessons

  - partial application
  - types
    - newtype
    - type
