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
GET https://www.eduassist.me/api/v1/school_classes will provide an `index` of classes associated with your user credentials.
```json
[{
        "id": 1,
        "name": "Grade 3",
        "description": "Half the students were transferred this year as their old school was closed. Remember they're new in town!\n      Need extra attention in Math."
    },
    {
        "id": 2,
        "name": "Grade 10",
        "description": "Really rowdy group, remember your classroom control techniques.\r\n      They absolutely love stories about famous Nigerians in history!"
    }
]
```
#### Create
POST https://www.eduassist.me/api/v1/school_classes will allow you to `create` a new class from the API. Please use the params school_class[name]: `Your Name Here` and school_class[description]: `your description here`.
#### Show
GET https://www.eduassist.me/api/v1/school_classes/:id will allow you to `show` a specific class ID and retrieve a list of the students.
```json
{
    "id": 1,
    "name": "Grade 3",
    "description": "Half the students were transferred this year as their old school was closed. Remember they're new in town!\n      Need extra attention in Math.",
    "students": [
        {
            "id": 1,
            "first_name": "Bisi",
            "last_name": "Adeleye-fayemi",
            "bio": "Bisi comes from a small village in the rural north, she's really shy but very bright.",
            "birthday": "2008-05-12"
        },
        {
            "id": 2,
            "first_name": "Olisa",
            "last_name": "Agbakoba",
            "bio": "Olisa has trouble focusing during class. She tends to bother other students and can be a distraction. She is very good at math.",
            "birthday": "2008-05-12"
        },
        {
            "id": 4,
            "first_name": "Pauline",
            "last_name": "Giwa",
            "bio": "Dele is an animal lover. Make sure to remember that his dog's name is 'Billy'!",
            "birthday": "2008-05-12"
        },
        {
            "id": 5,
            "first_name": "Pasquale",
            "last_name": "Adebisi",
            "bio": "Pascal wants to be a surgeon. He has already tried to practice his surgery on one of his classmates - leading to a reprimand from the headmaster.",
            "birthday": "2008-05-12"
        },
        {
            "id": 6,
            "first_name": "Patrick",
            "last_name": "Shagaya",
            "bio": "Patrick's parents are extremely poor, he comes to class hungry most days. Bringing an extra snack for him will help keep him focused.",
            "birthday": "2008-05-12"
        }
    ]
}
```

### Contribute:
We'd love to collaborate with software developers of any skill level to help bring the best experience to our users.  Please don't hesitate to jump onboard!
