# Elm

![Logo](https://upload.wikimedia.org/wikipedia/commons/thumb/f/f3/Elm_logo.svg/1200px-Elm_logo.svg.png)

---

#### Elm is a programming language

```
- It just happens to compile to JavaScript
- Its not transpiling
- You cant import npm packages into it, only Elm packages
```

---

#### This is what Elm looks like

```elm
module Main exposing (main)

import Html exposing (Html, p, text)
import Html.Attributes exposing (class)


main : Html msg
main =
	p
		[ class "greeting" ]
		[ text "Hello, World!" ]
```

---

