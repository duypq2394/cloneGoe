# /gapi/guest search

## Overview
| Endpoint | Name | Type | Authentication |
| ---- | ---- | ---- | ---- |
| /gapi/guest | search | Graphql | Not Required |


指定されたキーワードと、配信許諾の名前が部分一致するタイトルをリスト形式で取得します。キーワードがスペースで区切られた場合は、AND条件でタイトルの絞り込みを行います。指定されたキーワードを検索履歴として記録します。また、セーフサーチの有効／無効を設定することができます。セーフサーチが有効な場合、アダルト向けに該当する作品マスタは除外されます。

## API Schema
```
enum SeachTarget {
  title
  author
  all
}

enum SortKey {
  new,
  title
}

type SearchOption {
  target: SeachTarget!,
  isSafeSearch: boolean
}

query {
  search (
     keyword : String!,
     option : SearchOption!,
     limit: Number,
     pageToken: String,
     sortkey : SortKey
  )
}
```

## Specification
### Request Query Schama
```
query {
  search (
     keyword : “<keyword>”, (required)
     option : {
       target: “<title | author | all>, (required)
       isSafe: <true | false> (default: false)
     }
     ,limit: <number> (default: 10)
     ,pageToken: ”<pageToken>”,
     .sortkey : “<new | title>” (default: new)
  )
}
```
### Parameters

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| keyword | String! | - | Keyword for search |
| option | SearchOption | - | Search option |
| limit | Number | 10 | Maximum size of list items to get per query.  |
| pageToken | String | - | The token to next page. |
| sortKey | String | "new" | The name of the item to be sorted. Ascending order by the value of this key. |
|||||

#### Search Option Type
| Name | Type | Default | Description |
| --- | --- | --- | --- |
| target | SearchTarget! | - | Keyword for search |
| isSafe | Boolean | false | Search option |

#### SeachTarget
| Param | Description |
| --- | --- |
| title | Search by title |
| author | Search by author |
| all | Search from All |

### Request Header

Not Required

### Result
<table>
<tr>
  <td>Success</td>
  <td><ul><li>Return list of search result</li></ul></td>
</tr>
<tr>
  <td>ErrorType</td>
  <td>
    <ul>
      <li>Authentication Failure</li>
      <ul>
        <li>Session token is invalid</li>
      </ul>
      <li>Invalid Argument</li>
      <ul>
        <li>Page token is invalid</li>
        <li>Sort parametor is invalid</li>
      </ul>
      <li>Internal Server Error</li>
    </ul>
  </td>
  </tr>
</table>

#### Success Schema
```
{
  data : {
    search : {
      count : number,
      list : [title],
      nextToken : string
    }
  }
}
```
#### Error Schema
```
{
  error: {
    "path": [“search”],
    "data": { … },
    "errorType": "<Authentication Failure | Invalid Argument  | Internal Server Error>",
    "locations": [{"line": #0, "column": #0}],
    "message": "<Session token is invalid | Page token is invalid | Sort parametor is invalid | Internal server error >"
  }
}
```
## Sample
```
{
  data: {
    search : {
      count : 3,
      list : [
        {...},
        {...},
        {...},
      ],
      nextToken : “abcdabcdabcdabcdabcdabcdabcdabcd”
    }
  }

  /* when the error ocuurs */
  error: {
    "path": [“search”],
    "data": { … },
    "errorType": "...Exception",
    "locations": [{"line": #0, "column": #0}],
    "message": "..."
  }
}
```
