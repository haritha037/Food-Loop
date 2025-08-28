# 1. Functionality

I want to build a mobile application to reduce the food wastage of restaurants/ basically anywhere. It is like a social media site, where restaurants/hotels/people at home post about give away of excessive/unsold food for free.

It works like this. Let's say you have excessive food. Then you can take a photo of it, add a caption and a category. When posting, the user get to set the location at which the one who wants to get it should come.(by default it can be the current location of the user, also need to be able to set it manually). In addition to that, the user who post should decide for how many people does this food is sufficient. Let's say you have 6 buns left, so if you are deciding to give one for each person, then the number is 6, if you decide to give 2 for each person, the number is 3. This number is not shown to the other users. It is there to decide the lifetime of the post.

If you are a user who is looking for free food through the app, you will have two views to look for food. First one is a list view like facebook feed where you can see the posts of food. The other view is map view. the map should be zoomed in and centered at the user's current location. The location of the user as well as the locations of the posts will be marked in the map. Once you tap on a marker, a modal window will popup showing the post.(we can reuse the post component).

One problem that can occur when using the app is, many people will see one post at the same time and then go to the location to pick it. That is okay unless it exceeds the number of people specified by the user who posted it. To avoid exceeding that, we should create a mechanism to reserve the food. The users will see a reserve button on the side of the the post.

When a user tap on that button, a dialog box should pop up asking for confirmation telling that, by reserving the food, you remove the chance of others seeing the post, confirm only if you are coming. (you may generate the appropriate wording for the message, tempting users not to confirm for fun).
Once confirmed, it should be checked whether the number maximum number is reached. If it is reached, the post should be removed realtime from the other users' feeds/map to prevent contention.
Simultaneously, a notification should be pushed to the person who posted the post with the details of the one who reserved.
It is like a faceboook friend request notification- "<Name> reserved <Post>" <Donated>.
The content inside the tags are clickable and linked to the user profile and the post respectively. The <Donated> button is pressed when the receiver reach out and get the food. The notification should also include the <phone number> once tapped, goes to phone's call interface.
When a user reserves food by confirming the popup, he should see a map with a path highlighting the route to reach the destination. The map should update in real time when the user moves using the location data of the user. (It is like the pickme/uber ride). Below the map, there should be an option to call the user who posted the post.
Once the user reach the destination and meet the user who give away, the giving user click 'done' button on the notification related to the came user. Then the receiving user gets a notification like "Enjoy your meal".

I think I have clearly mentioned the functional requirements of the app. In addition to this we should have google signin as the authentication system. So we can get the user's name, profile picture and phone number. We have to ask for the permission to get them I guess.
