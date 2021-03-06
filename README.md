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
 )
 ```
 
 or https://ellie-app.com/7V5sBcndPBka1
 
 # Get js event objects in the console to inspect them for decoding
 
 ## KeyboardEvent
 ```addEventListener("keydown",console.log);```
 
 # Convert posix to time based on curret timezone
 
 https://ellie-app.com/83zVNwRMF3va1
 
 # Record Helper
 
 https://pd-andy.github.io/elm-record-helpers/


## Debugging strategy

Chaining debug logs into a piping

```
value
  |> f
  |> Debug.log "f"
  |> g
  |> Debug.log "g"
```

# Console.Log the event object of an element
The event object is what you have at hand you define a custom "on" event. it's a json you can parse in what ever way you want. 
To see what this element contains and it's structured you can log the object in the console like this:
```
document.querySelector("SELECTOR").addEventListener("click", function(e){
  console.log(e)
});
```

# Feeding a hardcoded value to an on event msg

You don't have to decode a data attribute or id or so you can hardcode the msg content, e.g.:

```
on "animationend" 
     <| Decode.succeed 
     <| BrowserFinishedAnimation 
     <| String.fromInt i
```

# tuple decoder and positonal decoding

```tupleDecoder : Decoder (Int, Int)
tupleDecoder =
  Decode.map2 (\first second -> (first, second))
    (Decode.index 0 Decode.int)
    (Decode.index 1 Decode.int)```
    
