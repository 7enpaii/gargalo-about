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
                "username": string,
            },
            "is_my_comment": bool,
            "source": string(post), // ?
            "source_id": string, // id of post or event etc...
            "created_at": string(dateTime),
            "updated_at": string(dateTime),
            "text": string,
            "parent_id": int,
            "likes": int,
            "have_childs": bool,
						"childs": null// this field i have just in Entity not in Model
        }
        ....
    ]
}

# childs comments we will get with request

# algorithme for adding child into parent list
for every single comment item we have a parentId and childs fields
if person press answer button in comment widget i get the index and parentId of this comment and pass 
them into CommentCubit.getComments(int itemIndex, int parentId)
after i get the comments and set them into Comment.childs list but with pagination i don't now))
