## Follow and unfollow script Twitter

<p align="center">
 <img width="800" src="https://github.com/mohamedebrahim96/Twitter-Followers/raw/master/1m7y2n.jpg">
</p>


Increasing Followers on Twitter is really easy. Just follow other people and most of the Following follows you back.  Tech Vows shares script as an easy way for those wondering how to unfollow all Twitter followers and follow back to fans at once.



## Usage

1. Unfollow all Twitter Followers (People who follow you + People who don’t follow you)
**Step 1** : Log in to your twitter account.  
**Step 2** : Go to your Following list i.e. go to _www.twitter.com/following_   
**Step 3** : Open browser console. To open console     
 in Google Chrome press `ctrl + shift + J` |  
 in Firefox press `ctrl + shift + K` |   
 in Safari Press `ctrl + alt + I` .  
**Step 4** : To auto-scroll to the bottom of the page, until all list of users you are Following is loaded, paste this code in the  console.

```
setInterval(function() {
 window.scrollTo(0, document.body.scrollHeight);
 }, 2000);
```



Wait till it reaches the bottom of the page.

**Step 5** : Then run this snippet in console to unfollow all Twitter followers (all your Following) including unfollowers and people who follow you.

```
$('.button-text.unfollow-text').trigger('click');
```

2. Unfollow all Twitter Unfollowers at once (People who don’t follow you back)
Go through Step 1 to Step 4 above. After applying Step 4 to scroll to the bottom of the page, paste this code snippet to unfollow Twitter Followers who are not following you back.

```
$('.ProfileCard-content').each(function(){
 var status = $(this).find('.FollowStatus').text();
 var unfollowButton = $(this).find('.user-actions-follow-button');
 if(!status){unfollowButton.click();
 }});
```

3. Follow back to your fans OR Follow all of someone’s Followers on Twitter at once
Go to that someone @user’s Followers page Or your Followers page i.e. go to https://twitter.com/followers .

You can scroll down the page to keep loading more accounts OR Open console and apply Step 4 mentioned above to reach bottom of the page.

Then paste this script in console and press Enter to follow all Followers of that @user.

```
__cnt__=0; jQuery('.Grid-cell .not-following .follow-text').each(function (i, ele) 
{ ele = jQuery(ele);
 if (ele.css('display')!='block')
  {console.log('already following:', i); return;}
  setTimeout(function () 
  {ele.click();}
  , __cnt__++*500); });
```


The script will follow 2 Twitter users per second. Follow a maximum of 250 followers a day or you’ll risk your Twitter account shut down for spam.

========================================

```
setInterval(function () {
    window.scrollTo(0, document.body.scrollHeight);
    $('.ProfileTweet-actionButton.js-actionButton.js-actionFavorite:visible').click();
}, 1000);
```
Simple script in JavaScript to like all tweets on Twitter to get more followers and establish a dictatorship
1- Open Twitter in desktop mode
2- Type F12 or CTRL+MAIUSC+I
3- Open the Console
4- CTRL+C and CTRL+V the code
5- Press ENTER and enjoy the bot




Most common reasons people Unfollow on Twitter:

- If Unfollowed
- Unfunny jokes.
- Constant negativity and/or complaining about things.
- Excessive rudeness, insulting other people, etc.
- Bad spelling and grammar.
- Retweeting every single compliment and insult they get (unless it happens to be funny.)
- Using Retweet to reply to people (it’s like talking loudly on the phone so everyone can hear your conversation.)
- Abusing Foursquare/Gowalla check-ins, Formspring questions and other services that crosspost to Twitter and add nothing but useless noise.
- `#Excessive #use #of #hashtags.`
- Poorly live-tweeting events & conferences in a way that conveys absolutely no information to the people not in attendance, defeating the purpose of live-tweeting it in the first place.



## About
This Javascript snippet automatically unfollows everyone in your Twitter account. It is designed to be used in the Javascript browser console - just copy/paste it (while you are logged into your Twitter account - you have to be on the profile page) and that's it. The speed of the unfollow events is ~67 unfollows per hour.

## Usage
1. Log into your Twitter account
2. Go to your Profile page
3. Open the "Following" dialog (by clicking on the line that says "NNN following" - where "NNN" is the number of the people you are following at the moment)
4. Open browser's developer tools (hit F12 - for Google Chrome and Firefox) and click on the "Console" tab
5. Copy/paste this Javascript snippet to the "Console" dialog in the browser
6. That's it - the script should start unfollowing people one by one, slowly (~67 unfollows per hour)

## History
Twitter has a time-based limitation on follow/unfollow events. I was specifically interested in unfollow events and at the moment (2. February 2017.) it's ~70 unfollows per hour.
I created this script because my Twitter account was hacked and someone followed ~1400 people with it. Because of the time-based limitation stated above, it's really difficult to correct this issue by hand. Hence, I decided to automate the task using Javascript via browser's developer tools.

## Possible Issues
- The script assumes that the "Following" dialog has a class of a certain name (defined in the script as `fwDialogSelector`). That name might be unique on a per user basis - I'm not sure since I didn't have the time to test that. If the script is not doing anything then inspect the DOM tree and see if the "Following" DOM element has a sub-element with the specified class (this can be done quickly using the jQuery command in the "Console" window).
- The script also assumes that the "Unfollow" button has a class of a certain name (defined in the script as `fwButtonSelector`). The story is the same as in the previous case with `fwDialogSelector` (above).

## How It Works
The script first imports jQuery Javascript library by injecting the `<script>` DOM. It then waits for it to completely load and then it executes the `unfollow()` function.
The `unfollow()` function searches the DOM tree for "Unfollow" buttons and triggers `click` event on each of the buttons - once every ~6 seconds. After 13 clicks it pauses the execution for 10 minutes. It then repeats the whole process after the pause.
It will automatically scroll the "Following" modal in order to load more "Unfollow" buttons.



## References
[techvows Blog](https://www.techvows.com/follow-unfollow-all-twitter-followers/)   
[github repo](https://github.com/pbradaric/instagram-unfollow-script)

