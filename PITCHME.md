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

#### Comparison to JS
```elm
very : String -> String
very str =
	"very " ++ str
```
```javascript
function very (str) {
	return "very " + str;
}
```

---

#### Here is a very simple Elm program

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

