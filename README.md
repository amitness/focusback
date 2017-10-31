# focusback
Vibrate your fitness band when you're distracted on social media.

![Focusback Illustration](https://i.imgur.com/ybEYq9i.png)

## How it works  
1. The script fetches your social media usage time from [Rescuetime](https://www.rescuetime.com) API.
2. If the social media usage exceeds a limit, a notification is sent to the smartphone via [Pushover](http://pushover.net).
3. Notifications for pushover are turned on through official app of fitness tracker.
4. The process check every 15 mins from the time you're distracted first and repeats 1-2-3.

## Dependencies
- [Rescuetime](https://www.rescuetime.com) extension installed in browser
- [Pushover](http://pushover.net) app on your smartphone.

## Installation
1. Fork and clone the repo
    ```
    git clone https://github.com/yourgithubusername/focusback
    ```
2. Create a heroku app.
    ```
    heroku create appname
    ```
3. Set environment variable with your pushover and rescuetime API key.
    ```
     heroku config:set PUSHOVER_TOKEN='XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX'
     heroku config:set RESCUETIME_TOKEN='XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX'
    ``` 

4. Push the app
    ```
    git push heroku master
    ```
 
5. On [IFTTT](http://ifttt.com/), create a [new applet](https://ifttt.com/create). 
    - On `THIS`, select `datetime` > 'Every Hour'
    - On `THAT`, select `Webhooks` > `Make a web request`
    - Set `URL` to your heroku app URL
    - Set `METHOD` to `GET`
    - Hit `Create Action`

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details
