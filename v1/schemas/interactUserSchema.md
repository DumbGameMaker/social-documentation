## interactUserSchema
| Field | Type | Optional | Description |
| -- | -- | -- | -- |
| _id | String | false |  userID: this is used for everything within the site, it's used for posts, live chat, etc. |
| username | String | false | Used as a unqiue identifier, someone can search up a username and get the exact result when needed.
| lastEditUsername | String | false | This is used to know the last time they updated their displayname. (also used for rate limiting) |
| displayName | String | false | Used for general name incase username is not as you wanted. |
| description | String | true | The user's bio/description. |
| pronouns | String | true | The user's pronouns. |
| statusTitle | String | true | Users can set a status that shows up on the profile.
| lastEditDisplayname | Number | false | This is used to know the last time they updated their displayname. (also used for rate limiting) |
| creationTimestamp | String | false | When the user first joined the site. |
| followerCount | Number | false | Amount of followers the user has. |
| followingCount | Number | false | Amount of people the user is following. |
| likeCount | Number | false | Amount of likes the user has on all their posts. |
| likedCount | Number | true | Amount of posts the user has liked |
| totalPosts | Number | true | The total amount of indepentant posts the user has made. |
| totalReplies | Number | true | The total amount of replies the user has made. |
| privacySetting | Object<[privacySettingSchema](#privacysettingschema)> | true | User privacy settings. |

### privacySettingSchema
| Field | Type | Optional | Description | 
| -- | -- | -- | -- |
| discoverySetting | Number<[options](#privacysettingoptions)>| true | Can you search the user up? | 
| postVisiblityDefault | Number<[options](#privacysettingoptions)> | true | Can anybody see the posts? |
| postReplyDefault | Number<[options](#privacysettingoptions)>| true | Can anybody any replies? |

### privacySettingOptions
| Option | Description |
| -- | -- | 
| 1 | Public | Everybody will be able to view data.
| 2 | Friends of Friends Only | Only friends of friends will be able to view data.
| 3 | Private (Friends Only) | Only your friends will be able to view data.
