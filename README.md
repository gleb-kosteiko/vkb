# VKB - bot for vk.com competitions

[![Build Status](https://travis-ci.org/gleb-kosteiko/vkb.svg?branch=master)](https://travis-ci.org/gleb-kosteiko/vkb)
[![release](https://img.shields.io/badge/release-vkb--1.0-brightgreen.svg?style=flat)](https://github.com/gleb-kosteiko/vkb/releases/latest)
[![License](https://img.shields.io/badge/License-WTFPL-brightgreen.svg)](https://raw.githubusercontent.com/gleb-kosteiko/vkb/master/copying.txt)

Script allows you to automate the searching and participation in random reposts competitions in vk.com.

### Main capabilities
- Check friends walls for competition posts and repost these posts (also joined all needed communities and added all needed users to friends) 
- Do reposts of random posts from mentioned communities (for  simulation of the real user behavior)
- To add random friends (also for simulation, like previose one)
- Search competition posts in VK search and repost it
- Search competition posts in already joined communities and repost it
- Search competition communities, check walls for competitions, reposts these posts and join communities

### Requirements for building and running
- Java 8 or higher
- Gradle 2.8 or higher
- An account in [vk.com](https://vk.com) that is not a pity to lose (admins are struggling with fake accounts and it can be banned)

### How to build, configure and run
For **building the project** use Gradle. Go to the root project directory and run `gradle dist` command. It will generate zip archive in *build\dist* directory. Extract it somewhere and script is almost ready for running (just need to link it with your VK account and setup some properties).

Now about the **configuration**.
First, you need to have an account in vk.com, which you'll use for running the script. I would recommend to use an account that is not a pity to lose, because it can be banned for "strange activity".
The next thing you need to do - to configure some script properties. Go to *conf* directory and find there *vkb.properties* file. Here is an example of configured properties - [vkb.properties](https://gist.github.com/gleb-kosteiko/d5a4e2c6b40104d88e45). There are five **required properties**:

-  *current.user.id* - identification number of your account.
-  *application.id* - identification number of application (it's used for API requests to vk.com).
-  *access.token* - the key that is used for access your application to vk.com API.
- *communities.search.words* - comma-separated list of key words, which will be used for searching of competition communities (e.g. *competition,gifts,prizes*).
-  *post.classification.model* - the model that allow identify competition posts.

Full list of properties, descriptions and example values you can find [here](https://github.com/gleb-kosteiko/vkb/blob/master/properties.md). 


Also there is [Dockerfile](https://github.com/gleb-kosteiko/docker-vkb) for VKB.



*Feel free to make pull requests!*


---

**Copyright © Gleb Kosteiko**

This work is free. You can redistribute it and/or modify it under the
terms of the Do What The Fuck You Want To Public License, Version 2,
as published by Sam Hocevar. See the [COPYING](https://raw.githubusercontent.com/gleb-kosteiko/vkb/master/copying.txt) file for more details.
