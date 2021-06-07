# Clubhouse API for Postman

![logo](https://cdn.iphoneincanada.ca/wp-content/uploads/2021/02/clubhouse.png)

[Clubhouse](https://www.joinclubhouse.com/) is a new type of network based on voice. When you open the app you can see “rooms” full of people talking—all open so you can hop in and out, exploring different conversations.

It's a [Postman](https://postman.co)'s Collection to use and test API endpoints of Clubhouse.

## Authentication

There is a multi-level authentication by phone number :

- Check user's status and send verification code via SMS ( or call the person to say verification code )
- Check verification code and deliver `auth_token`, `access_token` and `refresh_token`

## Start

At first you need to import `collection.json` ( Or use [public collection](https://documenter.getpostman.com/view/2651915/TzCQa6Wx) ) and some collection variables :

- `auth_token`
- `user_id`
- Phone number
- Email address

There is a script in **Complete** request to set `auth_token` and `user_id`. Otherwise, enter them manually.

Also, you need to set your **phone number** and **email address**.

## Endpoints

### Authentication

| Request  | Description                                                                                                                  |
| -------- | ---------------------------------------------------------------------------------------------------------------------------- |
| Check    | Check user's status and send verification code via SMS.                                                                      |
| Call     | Call the person and send verification message if SMS not delivered.                                                          |
| Complete | Complete phone number authentication. This should return `auth_token`, `access_token`, `refresh_token`, `is_waitlisted`, ... |

### User

| Request        | Description                                                    |
| -------------- | -------------------------------------------------------------- |
| Add email      | Request for email verification. You only need to do this once. |
| Settings       | Receive user's settings.                                       |
| Me             | Get your information.                                          |
| Follow user    | Follow a user                                                  |
| Unfollow user  | Unfollow a user                                                |
| Block user     | Block a user.                                                  |
| Unblock user   | Unblock a user.                                                |
| Followings     | Get following of the given `user_id`                           |
| Followers      | Get followers of the given `user_id`                           |
| Online friends | List all online friends.                                       |
| Profile        | Lookup someone else's profile.                                 |
| Clubs          | Get list of clubs the user's in.                               |
| Search         | Search users based on the given query.                         |
| Logout         | Logout from current session.                                   |

### Channel ( Room )

| Request       | Description                                                                                            |
| ------------- | ------------------------------------------------------------------------------------------------------ |
| Get channels  | Get list of channels, based on the server's channel selection algorithm.                               |
| Get channel   | Get information of the given channel.                                                                  |
| Create        | Create a new channel.                                                                                  |
| End           | Kick everyone and close the channel. Requires **moderator** privilege.                                 |
| Invite user   | Invite someone to a currently joined channel. It will send a ping notification to the given `user_id`. |
| Hide channel  | Hide/Unhide the channel from the channel list.                                                         |
| Leave channel | Leave the given channel.                                                                               |
| Join channel  | Join the given channel.                                                                                |

### Club

| Request     | Description                                   |
| ----------- | --------------------------------------------- |
| Search      | Search clubs based on the given query.        |
| Information | Get the information about the given `club_id` |
| Members     | Get list of members on the given `club_id`    |
| Follow      | Follow a club                                 |
| Unfollow    | Unfollow a club                               |

### Other

| Request         | Description                                     |
| --------------- | ----------------------------------------------- |
| Release notes   | Get release notes                               |
| Update          | Check for app updates                           |
| Waitlist status | Check whether you're still on a waitlist or not |

## Support

[![Donate with Bitcoin](https://en.cryptobadges.io/badge/micro/3GhT2ABRuHuXGNzP6DH5KvLZRTXCBKkx2y)](https://en.cryptobadges.io/donate/3GhT2ABRuHuXGNzP6DH5KvLZRTXCBKkx2y) [![Donate with Ethereum](https://en.cryptobadges.io/badge/micro/0x0831bD72Ea8904B38Be9D6185Da2f930d6078094)](https://en.cryptobadges.io/donate/0x0831bD72Ea8904B38Be9D6185Da2f930d6078094)

[![ko-fi](https://www.ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/D1D1WGU9)

<div><a href="https://payping.ir/@hatamiarash7"><img src="https://cdn.payping.ir/statics/Payping-logo/Trust/blue.svg" height="128" width="128"></a></div>

## Contributing

1. Fork it !
2. Create your feature branch : `git checkout -b my-new-feature`
3. Commit your changes : `git commit -am 'Add some feature'`
4. Push to the branch : `git push origin my-new-feature`
5. Submit a pull request :D

## Issues

Each project may have many problems. Contributing to the better development of this project by reporting them.
