{
    "current_page": int,
    "last_page": int,
    "last_page_url": string,
    "next_page_url": string:null,
    "from": int,
    "prev_page_url": string:null,
    "path": string,
    "to": int:null,
    "per_page": int,
    "total": int,
    "data": [
        {
            "id": int,
            "user": {
                "user_id": int,
                "avatar": string(link),
                "nickname": string,
                "username": string
            },
            "is_my_post": bool,
            "pubdate": string,
            "text": string:null,
            "views": int,
            "comments_count": int,
            "theme": string(post,appeal,vote),
            "likes": int,
            // media can be null
            "media": [
                {
                  "type": string(image,video),
                  "link": string,
                },
                {
                  "type": string(image,video),
                  "link": string,
                }
                ...
            ],
            //this field can be null and must be provided
            "vote_info": {
                "vars": [
                    {
                      "var_id": int,
                      "title": string,
                      "votes": int
                    }
                      ...
                ],
                //this field can be null if user is not choosed some vote id
                //"user_vote": null
                "user_vote": {
                    "id": int,
                    "variant": int, //this is id of vote that user choosed
                }
                "total": int,
            },
            //this field can be null and must be provided
            //"appeals_users": null
            "appeals_users": [
                {
                  "id": int,
                  "nickname": string,
                  "username": string,
                  "avatar": string,
                },
                ...
            ]
						// if we haven't taged user into 
						"taged_users": [
								{

								}
						]
        },
    ]
}
