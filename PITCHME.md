# Elm

![Logo](https://upload.wikimedia.org/wikipedia/commons/thumb/f/f3/Elm_logo.svg/1200px-Elm_logo.svg.png)

---

#### Elm is a programming language

- It just happens to compile to JavaScript
- Its not transpiling
- You cant import npm packages into it, only Elm packages
- Immutability always
- Architecture is that of React / Redux

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

very : String -> String
very =
	append "very"
```


#### You can pipe

```javascript
mixin(otherStuff, doThat(doThis(somestuff)));
```
```elm
someStuff
	|> doThis
	|> doThat
	|> mixin otherStuff
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

---

#### Friendly compiler
```
The argument to function `fromPage` is causing a mismatch.

145|                        fromPage 4
                                     ^
Function `fromPage` is expecting the argument to be:

    Id

But it is:

    number
```

---

#### Key Advantages

- **!! NO RUN TIME ERRORS !!**
- Painless refactoring
- High performance with no optimizations











