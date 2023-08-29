
1. **Users:**
   - **user_id**: Unique identifier for each user.
   - **username**: User's chosen username.
   - **email**: User's email address.
   - **password**: Hashed password for authentication.
   - **profile_image**: URL to the user's profile picture.
   - **bio**: User's bio or description.
   - **followers_count**: Count of followers for the user.
   - **following_count**: Count of users the user is following.
   - **posts_count**: Count of posts created by the user.
   - **created_at**: Timestamp of user registration.
   - **updated_at**: Timestamp of last profile update.

2. **Posts:**
   - **post_id**: Unique identifier for each post.
   - **user_id**: Foreign key referencing the user who created the post.
   - **image_url**: URL to the post's image or video.
   - **caption**: Caption or description for the post.
   - **likes_count**: Count of likes for the post.
   - **comments_count**: Count of comments on the post.
   - **created_at**: Timestamp of post creation.
   - **updated_at**: Timestamp of last post update.

3. **Likes:**
   - **like_id**: Unique identifier for each like.
   - **user_id**: Foreign key referencing the user who liked the post.
   - **post_id**: Foreign key referencing the post that was liked.
   - **created_at**: Timestamp of when the like was created.

4. **Comments:**
   - **comment_id**: Unique identifier for each comment.
   - **user_id**: Foreign key referencing the user who posted the comment.
   - **post_id**: Foreign key referencing the post the comment belongs to.
   - **text**: Text content of the comment.
   - **created_at**: Timestamp of when the comment was posted.

5. **Follows:**
   - **follow_id**: Unique identifier for each follow relationship.
   - **follower_id**: Foreign key referencing the user who is following.
   - **following_id**: Foreign key referencing the user who is being followed.
   - **created_at**: Timestamp of when the follow relationship was established.

6. **Notifications:**
   - **notification_id**: Unique identifier for each notification.
   - **user_id**: Foreign key referencing the user receiving the notification.
   - **source_user_id**: Foreign key referencing the user who triggered the notification (e.g., liked a post, commented, followed).
   - **type**: Type of notification (e.g., like, comment, follow).
   - **is_read**: Indicates whether the notification has been read.
   - **created_at**: Timestamp of when the notification was generated.

9. **Direct Messages:**
   - **message_id**: Unique identifier for each direct message.
   - **sender_id**: Foreign key referencing the user who sent the message.
   - **receiver_id**: Foreign key referencing the user who received the message.
   - **message_text**: Content of the message.
   - **sent_at**: Timestamp of when the message was sent.
   - **is_read**: Indicates whether the message has been read.

10. **Stories:**
    - **story_id**: Unique identifier for each story.
    - **user_id**: Foreign key referencing the user who created the story.
    - **media_url**: URL to the image or video of the story.
    - **expires_at**: Timestamp indicating when the story will expire.
    - **created_at**: Timestamp of when the story was created.

11. **StoryViews:**
    - **story_view_id**: Unique identifier for each story view.
    - **story_id**: Foreign key referencing the viewed story.
    - **viewer_id**: Foreign key referencing the user who viewed the story.
    - **viewed_at**: Timestamp of when the story was viewed.

14. **Blocked Users:**
    - **block_id**: Unique identifier for each blocked user entry.
    - **user_id**: Foreign key referencing the user who initiated the block.
    - **blocked_user_id**: Foreign key referencing the user who is blocked.
    - **blocked_at**: Timestamp of when the block was initiated.

