## Services
* https://github.com/QDivision/sandwich-ui
* https://github.com/QDivision/emoji-api
* https://github.com/QDivision/ingredient-api
* https://github.com/QDivision/sandwich-api

## `sandwich-service`

```
GET /sandwiches
[{
  "name": "BLT"
  "bread": { "name": "sourdough", "emoji": "🍞" },
  "condiments": [
    { "name": "ketchup", "emoji": "🍅" },
    { "name": "mustard", "emoji": "🌭" }
  ],
  "layers": [
    { "name": "bacon", "emoji": "🥓" },
    { "name": "lettuce", "emoji": "🥬" },
    { "name": "tomato", "emoji": "🍅" }
  ]
}, {
  "French Dip"
  "bread": { "name": "baguette", "emoji": "🥖" },
  "condiments": [
    { "name": "beef broth", "emoji": "🐄" }
  ],
  "layers": [
    { "name": "onion", "emoji": "😢" },
    { "name": "cheese", "emoji": "🧀" },
    { "name": "beef", "emoji": "🥩" }
  ]
}]

POST /sandwiches
{
  "bread": { "name": "sourdough", "emoji": "🍞" },
  "condiments": [
    { "name": "ketchup", "emoji": "🍅" },
    { "name": "mustard", "emoji": "🌭" }
  ],
  "layers": [
    { "name": "bacon", "emoji": "🥓" },
    { "name": "lettuce", "emoji": "🥬" },
    { "name": "tomato", "emoji": "🍅" }
  ]
}
```

## `ingredient-service`

```
GET /ingredients
[{
  "name": "bacon",
  "emoji": "🥓"
}, {
  "name": "baguette",
  "emoji": "🥖"
}]

POST /ingredients
{
  "name": "lettuce",
  "emoji": "🥬"
}
```

## `emoji-service`

```
GET /emojis/{label}
{ "emoji": "🥓" }

POST  /emojis/{label}
{ "emoji": "🥬" }
```
