# [eduAssist.me](https://www.eduassist.me)

### About:
eduAssist.me is a mobile-friendly education webapp designed and developed by [Patrick Scheuchzer](https://github.com/patrick-scheuchzer), [Pascal Kress](https://github.com/wabi69sabi), [Pauline Gaget](https://github.com/lupiane), and [Spencer Bray](https://github.com/letired).  This app was built over a two-week sprint during the final weeks of the [Le Wagon](https://lewagon.com) Berlin bootcamp. As of May 2017, we have launched and are collecting user feedback.

### Goals:
* Mobile-first - our target audience doesn't have access to a desktop or laptop computer.  Most education software is designed for use on a large format screen with a keyboard and mouse, eduAssist is intended to be used on a handheld touchscreen device without a mouse or keyboard.
* Simple - no bloated features. Get started right away. Quick statistics on your student's performance without any prior configuration.
* Free - we wanted to build a piece of software that could help low-income teachers, not to make a profit.

### Test:
Wanna check it out with some pre-populated data? Feel free to login with these credentials:

* Login: `spencer@teacher.com`
* Password: `password`
* API Token: `8Q21xcNYWjCyxvyA-cDm`

Just like a national park - please leave it like you found it!

### API:
We're currently adding an API.  
In order to authenticate, please send the following headers:

* X-User-Email: `Your Email Here`
* X-User-Token: `Your API Token Here`

The following endpoints are available:
#### Index
* GET https://www.eduassist.me/api/v1/school_classes will provide an `index` of classes associated with your user credentials.
#### Create
* POST https://www.eduassist.me/api/v1/school_classes will allow you to `create` a new class from the API. Please use the params school_class[name]: `Your Name Here` and school_class[description]: `your description here`.
#### Show
* GET https://www.eduassist.me/api/v1/school_classes/:id will allow you to `show` a specific class ID and retrieve a list of the students.


### Contribute:
We'd love to collaborate with software developers of any skill level to help bring the best experience to our users.  Please don't hesitate to jump onboard!
