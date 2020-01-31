# elm-ellie-examples

Collection of great elm solutions and examples shared in ellie.
The elli code is of course not my code, it's an collection of ellies shared by others.

# Dynamic textarea in elm
https://ellie-app.com/4JY5PFRWYW3a1

This solutions is mostly based on CSS and the best solution to automatically add and remove rows, based on the user input.

# Get selected item from dropdown
https://ellie-app.com/6ZJ2tQ8FnbNa1

# You only need main to run elm
No need for a model etc.

https://ellie-app.com/7nVDGRBQr8ka1

# How to use Debug.log in a Decoder

```case Decode.decodeValue decoder (Debug.log "log message:" value) of```

# Random generator

Great example, especially because random types are generated

https://ellie-app.com/7TPZYfJnb74a1

# Conditional Decoding

```Decode.field "passCount" Decode.int
 |> Decode.andThen (\type_ ->
     case type_ of 
         1 -> onePassStreamDecode
         2 -> twoPassStreamDecode
         _ -> Decode.fail "Unknown passCount"
 )```
 
 or https://ellie-app.com/7V5sBcndPBka1
