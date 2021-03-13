# Public JR project
...

## Content
Base path for this project : `https://www.any.address.com/`
<br>

* [User API](#user-api)
    + [User Profile](#user-profile)
    + ...

* [Admin API](#admin-api)
    + [Admin Profile](#admin-profile)
    + ...


### User API

#### User Profile:

|URL|HTTP method|Description|Curl|Response Code (success)|Response Codes (fail)|
|---|:---:|---|---|:---:|:---:|
|/rest/user/registration|POST [json](/reg_user_json.md)|Registration|...|201|400 [json](/error_reg_user_json.md), 500|
|/rest/user/{id}|GET|Get own profile|curl -s http://.../rest/user --user user@gmail.com:user|200|
|/rest/user|PUT [json](/reg_user_json.md)|Update own profile|...|204|400 [json](/error_reg_user_json.md), 404, 500|
|/rest/user|DELETE|Delete own profile|curl -s -X DELETE http://.../rest/user --user user@gmail.com:user|204|

<sub>[to table of content](#content)</sub>



### Admin API:

Authority: admins only (who has role `ROLE_ADMIN`)

#### Admin Profile:

|URL|HTTP method|Description|Curl|Response Code (success)|Response Codes (fail)|
|---|:---:|---|---|:---:|:---:|
|/rest/admin/user|POST|Create new user|...|201|
|/rest/admin/user/{id}|PUT|Update user profile|...|200|
|/rest/admin/user/{id}|DELETE|Delete user profile|...|204|
|/rest/admin/user/{id}|GET|Get user profile by ID|curl -s http://.../rest/admin/user/100000 --user admin@gmail.com:admin|200|
|/rest/admin/user?email=...|GET|Get user by email|...|200|
|/rest/admin/user/{id}?enabled=...|POST|Set user enabled true/false|...|200|

<sub>[to table of content](#content)</sub>

