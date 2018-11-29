# TikTok/musical.ly Sign Service

This is an online demo for tiktok/musical.ly sign algorithm. 
If you need to deploy this service on your own private server, please contact [hello@crawldata.app](hello@crawldata.app) for business affairs.
Every demo function can be called only 20 times.


## 2 version 
There are two versions of Signature Algorithms:

+ **Old v1** as/cp

  Some new functions are not available.

+ **New v2** as/mas

  All functions of the latest version 9.2 are available.


## Service Demo

```
https://crawldata.app/api/tiktok/
```

#### 1. Gen as/mas
```
curl -X "POST" "https://crawldata.app/api/tiktok/v2/sign" \
     -H 'Content-Type: application/json' \
     --insecure \
     -d $'{
  "url": "https://api2.musical.ly/aweme/v1/discover/search/?cursor=0&keyword&count=10&type=1&is_pull_refresh=0&hot_search=0&search_source&js_sdk_version=&app_type=normal&app_language=zh-Hant&manifest_version_code=2018111637&_rticket=1543508644401&iid=6629283809978402565&channel=googleplay&language=zh&fp=PrT_c2LZLMwbFlqMFlU1LSFIJzQZ&device_type=ONEPLUS%20A5000&account_region=HK&resolution=1080*1920&openudid=4617150637217100&update_version_code=2018111637&sys_region=CN&os_api=27&is_my_cn=1&timezone_name=Asia%2FShanghai&dpi=420&carrier_region=HK&ac=wifi&device_id=6603356836101883397&pass-route=1&mcc_mnc=46000&timezone_offset=28800&os_version=8.1.0&version_code=920&carrier_region_v2=454&app_name=musical_ly&ab_version=9.2.0&version_name=9.2.0&device_brand=OnePlus&ssmix=a&pass-region=1&build_number=9.2.0&device_platform=android&region=TW&aid=1233"
}'
```

#### 2. Gen device info
[https://crawldata.app/api/tiktok/v2/device/gen](https://crawldata.app/api/tiktok/v2/device/gen)

#### 3. API：

| | New v2 as/mas   | Old v1 as/cp |
| ------------- | ------------- | ------------- |
| Home feeds  | [/v2/feed](https://crawldata.app/api/tiktok/v2/feed)  | [/v1/feed](https://crawldata.app/api/tiktok/v1/feed)  |
| User's videos  | [/v2/aweme/post](https://crawldata.app/api/tiktok/v2/aweme/post?user_id=6603395355915993094&max_cursor=0&count=20)  | [/v1/aweme/post](https://crawldata.app/api/tiktok/v1/aweme/post?user_id=100481652413403136&max_cursor=0&count=20)  |
| User's favirite videos | [/v2/aweme/favorite](https://crawldata.app/api/tiktok/v2/aweme/favorite?user_id=6603395355915993094&max_cursor=0&count=20)  | [/v1/aweme/favorite](https://crawldata.app/api/tiktok/v1/aweme/favorite?user_id=100481652413403136&max_cursor=0&count=20)  |
| Personal profile  | [/v2/user](https://crawldata.app/api/tiktok/v2/user?user_id=6603395355915993094)  | [/v1/user](https://crawldata.app/api/tiktok/v1/user?user_id=6578820956968484870)|
| User's followings  | [/v2/user/following/list](https://crawldata.app/api/tiktok/v2/user/following/list?user_id=6603395355915993094&max_time=1543507917)  | [/v1/user/following/list](https://crawldata.app/api/tiktok/v1/user/following/list?user_id=6578820956968484870)  |
| User's followers  | [/v2/user/follower/list](https://crawldata.app/api/tiktok/v2/user/follower/list?user_id=6603395355915993094&max_time=1543507917)  | [/v1/user/follower/list](https://crawldata.app/api/tiktok/v1/user/follower/list?user_id=100481652413403136)  |
| Videos's comments  | [/v2/comment/list](https://crawldata.app/api/tiktok/v2/comment/list?aweme_id=6626744652743576838&cursor=0)  | [/v1/comment/list](https://crawldata.app/api/tiktok/v1/comment/list?aweme_id=6614960098630438150&cursor=0)  |
| Hot Topics | [/v2/category/list](https://crawldata.app/api/tiktok/v2/category/list?cursor=0)  | [/v1/category/list](https://crawldata.app/api/tiktok/v1/category/list?cursor=0)  |
| Topic related videos| [v2/challenge/aweme](https://crawldata.app/api/tiktok/v2/challenge/aweme?ch_id=20262712&cursor=0)  | [v1/challenge/aweme](https://crawldata.app/api/tiktok/v1/challenge/aweme?ch_id=20262712&cursor=0)  |
| Topic detail info| [v2/challenge/detail](https://crawldata.app/api/tiktok/v2/challenge/detail?ch_id=20262712)  |   |
| Search users| [v2/search/discover](https://crawldata.app/api/tiktok/v2/search/discover?keyword=lucas&cursor=0)  |   |
| Search music| [v2/search/music](https://crawldata.app/api/tiktok/v2/search/music?keyword=lucas&cursor=0)  |   |
| Search topic| [v2/search/challenge](https://crawldata.app/api/tiktok/v2/search/challenge?keyword=lucas&cursor=0)  |   |

+ **If you test old v1 as/cp, you will get a curl script, run it in a terminal, your network ip should not belong China.**
+ **Search API http request should contain logined-in user cookies**

