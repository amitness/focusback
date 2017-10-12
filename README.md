# focusback
Vibrate your fitness band when you're distracted on social media.

![Focusback Illustration](https://i.imgur.com/ybEYq9i.png)

## How it works  
1. The script fetches your social media usage time from [Rescuetime](https://www.rescuetime.com) API.
2. If the social media usage exceeds a limit, a notification is sent to the smartphone via [Pushover](http://pushover.net).
3. Notifications for pushover are turned on through official app of fitness tracker.
4. The process check every 15 mins from the time first distracted and repeats 1-2-3.

