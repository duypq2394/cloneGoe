# API Reference
## Guest API List (GraphQL)

| Endpoint | Function | Description |
----|----|----
| /gapi/guest | [search](api/gapi-guest-search.md) | Searches the titles by keywords and retrieves the results as a list of titles. |
| /gapi/guest | getTitleList | Retrieves a list of titles. |
| /gapi/guest | getBookList | Retrieves a list of books corresponding to the title. |
| /gapi/guest | getBookDownloadInfo | Retrieves the required information to download/view books. |
| /gapi/guest | getStoreCategories | Retrieves all store categories. (Argument candidates: top, recommend, ranking and orderby) |
| /gapi/guest | getSuggestWordes | Retrieves suggest words corresponding to an arbitrary word. |

## Guest API List (AppSync)
| Endpoint | Function | Description |
----|----|----
| /graphql | getNoticeList | Get information List |
| /graphql | getAppVersionInfo | Get application latest version |
| /graphql | getAppConfig | Get applkication config |

## Member Web Endpoint List
| Endpoint | Type | Description |
----|----|----
| /member/login | GET | Authentication | Logs in to the store API server and generates a session. |
| /member/logout | POST | Authentication | Get application latest version |

## Member API List (REST)
| Endpoint | Type | Description |
----|----|----
| /api/member/token | POST | Get token |

## Member API List (GraphQL)
| Endpoint | Function | Description |
----|----|----
| /gapi/member | login | Login to the store API server. |
| /gapi/member | logout | Logout from the store API server |
| /gapi/member | renewToken | Re-retrieves the custom token necessary for using the API. |
| /gapi/member | search | Searches the titles by keywords and retrieves the results as a list of titles. |
| /gapi/member | getTitleList | Retrieves a list of titles. |
| /gapi/member | getBookList | Retrieves a list of books corresponding to the title. Or retrieves a list of books from book ID list. |
| /gapi/member | getBook | Retrieves information of a book in the title. |
| /gapi/member | getBookDownloadInfo | Retrieves the required information to download/view books. |
| /gapi/member | getStoreCategories | Retrieves all store categories. (Argument candidates: top, recommend, ranking and orderby) |
| /gapi/member | getSuggestWords | Suggest Word |

## Member API List (AppSync)
| Endpoint | Function | Description |
----|----|----
| /graphql | getNoticeList | Retrieves a list of notices. |
| /graphql | getAppVersionInfo | Retrieves the latest version information (force update) of the app. |
| /graphql | getAppConfig | Retrieves the system setting information such as external site URL information. |
| /graphql | getFavoriteList | Retrieves a list of titles in my list. |
| /graphql | addFavorite | Adds a specific title to my list. |
| /graphql | deleteFavorite | Deletes a specific title from my list. |
| /graphql | getUserSetting | Retrieves user-specific setting information that needs to be synchronized between the web or devices. |
| /graphql | updateUserSetting | Updates user-specific setting information. |
| /graphql | getLoginDeviceList | Retrieves a list of currently logged-in devices. |
| /graphql | addLoginDevice | Adds a device information as currently logged in device.(This API will not be affected by the number limit of devices.) |
| /graphql | deleteLoginDevice | Deletes specific device information from currently logged in devices. |

## Admin API List (POST)
| Endpoint | Type | Description |
----|----|----
| /member/login | GET | Authentication | Logs in to the store API server and generates a session. |
| /member/logout | POST | Authentication | Get application latest version |

## Admin API List (POST)
| Endpoint | Type | Description |
----|----|----
| /api/member/token | POST | Get token |

## Admin API List (GraphQL)
| Endpoint | Type | Description |
----|----|----
| /api/member | login | Logs in to the store API server for administrators |
| /api/member | logout | Logs out from the store API server for administrators |
| /api/member | renewToken | Re-retrieves the custom token necessary for using the API for administrators. |
| /api/member | getTitleList | Retrieves a list of titles under specified conditions.|
| /api/member | getTitle | Retrieves title information. |
| /api/member | addTitle | Adds title information. |
| /api/member | updateTitle | Updates title information. (Only store-specific information can be updated) |
| /api/member | deleteTitle | Physically deletes title information. (This is for emergency use. Please use update when deleting logically) |
| /api/member | getBook | Retrieves book information. |
| /api/member | addBook | Adds book information. |
| /api/member | updateBook | Updates book information. Physically deletes title information. |
| /api/member | deleteBook | Deletes book information. (This is for emergency use. Please use update when deleting logically) |
| /api/member | getDCCategories | Retrieves all DC category information. |
| /api/member | addDCCategory | Adds DC category information. |
| /api/member | updateDCCategory | Updates DC category information. |
| /api/member | deleteDCategory | Deletes DC category information.  |
| /api/member | getStoreCategory | Store category includes top category, recommendation information, ranking information. |
| /api/member | addStoreCategory | Adds store category information. |
| /api/member | updateStoreCategory | Updates store category information. |
| /api/member | deleteStoreCategory | Deletes store category information. |
| /api/member | getAdminUserList | Searches admin users and retrieves the list. |
| /api/member | getAdminUser | Retrieves admin user information. |
| /api/member | addAdminUser | Adds admin user information. |
| /api/member | updateAdminUser | Updates admin user information. |
| /api/member | deleteAdminUser | Deletes admin user information.  |

## Admin API List (AppSync)
| Endpoint | Type | Description |
----|----|----
| /graphql | getNoticeList | Retrieves a list of all notice information including non-public information. |
| /graphql | getNotice | Retrieves notice information. |
| /graphql | addNotice | Adds notice information. |
| /graphql | updateNotice | Updates specific notice information. |
| /graphql | deleteNotice | Deletes specific notice information.  |
| /graphql | getAppConfigList | Retrieves a list of all system setting information. |
| /graphql | getConfig | Retrieves system setting information. |
| /graphql | addConfig | Adds system setting information. |
| /graphql | setConfig | Updates system setting information. |
| /graphql | deleteConfig | Deletes system setting information. |

