# Objects

## Space

```
{
  id: string,
  name: string,
  description: string,
  owner: "global" | "player" | "computer",
  pile_ids: [string],
  hand_ids: [string],
  zone_ids: [string],
  data: {}
}
```

# POST createSpace

## URI
/game_types/{game_type_id}/spaces/create
/game_types/{game_type_id}/spaces

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
{
  id: string | null,
  name: string | null,
  description: string | null,
  owner: "global" | "player" | "computer" | null,
  pile_ids: [string] | null,
  hand_ids: [string] | null,
  zone_ids: [string] | null,
  data: {} | null
}
```

## Response
201 Created 

**Headers**
- Content-Type: application/json

**Body**
```
Obj<Space>
```

# GET getSpaces

may want to do some pagination for this and/or just return name and id if too long

## URI
/game_types/{game_type_id}/spaces/get
/game_types/{game_type_id}/spaces

**Headers**
- Accept: application/json

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
[
  Obj<Space>, ...
]
```

# GET getSpace

## URI
/game_types/{game_type_id}/spaces/{space_id}/get
/game_types/{game_type_id}/spaces/{space_id}

**Headers**
- Accept: application/json

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
Obj<Space>
```

# PUT updateSpace

## URI
/game_types/{game_type_id}/spaces/{space_id}/update
/game_types/{game_type_id}/spaces/{space_id}

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
{
  id: string | null,
  name: string | null,
  description: string | null,
  owner: "global" | "player" | "computer" | null,
  pile_ids: [string] | null,
  hand_ids: [string] | null,
  zone_ids: [string] | null,
  data: {} | null
}
```

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
Obj<Space>
```

# PUT addItem

- If not empty, will replace value
- If array, will append
- If type is not specified, will assume

## URI
/game_types/{game_type_id}/spaces/{space_id}/addItem
/game_types/{game_type_id}/spaces/{space_id}/add

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
{
  name: string,
  type: string | null,
  value: any | null
}
```

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
Obj<Space>
```

# PUT addItems

- If not empty, will replace value
- If array, will append
- If type is not specified, will assume

## URI
/game_types/{game_type_id}/spaces/{space_id}/addItems

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
[
  {
    name: string,
    type: string | null,
    value: any | null
  },
  ...
]
```

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
Obj<Space>
```

# PUT removeItem

## URI
/game_types/{game_type_id}/spaces/{space_id}/removeItem
/game_types/{game_type_id}/spaces/{space_id}/remove

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
{
  name: string
}
```

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
Obj<Space>
```

# PUT removeItems

## URI
/game_types/{game_type_id}/spaces/{space_id}/removeItems

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
[
  {
    name: string
  },
  ...
]
```

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
Obj<Space>
```

# PUT setValue

- Will return error if not correct type

## URI
/game_types/{game_type_id}/spaces/{space_id}/setValue
/game_types/{game_type_id}/spaces/{space_id}/set

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
{
  name: string,
  value: any
}
```

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
Obj<Space>
```

# PUT setValues

- Will only set values that are the correct types

## URI
/game_types/{game_type_id}/spaces/{space_id}/setValues

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
[
  {
    name: string,
    value: any
  },
  ...
]
```

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
Obj<Space>
```

# PUT clearValue

## URI
/game_types/{game_type_id}/spaces/{space_id}/clearValue
/game_types/{game_type_id}/spaces/{space_id}/clear

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
{
  name: string
}
```

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
Obj<Space>
```

# PUT clearValues

## URI
/game_types/{game_type_id}/spaces/{space_id}/clearValues

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
[
  {
    name: string
  },
  ...
]
```

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
Obj<Space>
```

# DELETE deleteSpace

## URI
/game_types/{game_type_id}/spaces/{space_id}/delete
/game_types/{game_type_id}/spaces/{space_id}

## Response
204 No Content
