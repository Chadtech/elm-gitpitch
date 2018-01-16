# Elm

![Logo](https://upload.wikimedia.org/wikipedia/commons/thumb/f/f3/Elm_logo.svg/1200px-Elm_logo.svg.png)

---

#### Elm is a programming language

- It just happens to compile to JavaScript
- Its not transpiling
- You cant import npm packages into it, only Elm packages

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

#### You can curry
```elm
append : String -> String -> String
append str0 str1 =
	str0 ++ str1

append 
	--> String -> String -> String

append "very " 
	--> String -> String

append "very " "cool" 
	--> String
```

---

#### Here is a very simple Elm program

```elm
module Main exposing (main)

import Html exposing (Html, p, div, text)
import Html.Attributes exposing (class)

main : Html msg
main =
	div [] [ greet "Munich" ]

greet : String -> Html msg
greet who =
	p
		[ class "greeting" ]
		[ text ("Hello " ++ who) ]
```

---

#### You can make your own types
```elm
type Pet = Dog | Cat | Mouse

animalSound : Pet -> String
animalSound pet =
	case pet of
		Dog ->
			"Bark"

		Cat ->
			"Meow"

		Mouse ->
			"Squeak"
```

---

#### Maybe Type
```elm
type Maybe a = Just a | Nothing

maybeUserView : Maybe User -> Html Msg
maybeUserView maybeUser =
	case maybeUser of
		Just user ->
			userView user

		Nothing ->
			p [] [ text "no user" ]
```

---

#### Basic Update Function

---
```elm
type Msg = LoginButtonClicked | FieldUpdated String

update : Msg -> Model -> Model
update msg model =
	case msg of
		LoginButtonClicked ->
			attemptLogin model

		FieldUpdated newField ->
			setField model newField
```












