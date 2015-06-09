---
Title: Custom Visualizations using KeenIO
Date: 2015-06-10
Author: Alan Hamlett
AuthorUrl: https://wakatime.com/@alan
AuthorGravatar: https://1.gravatar.com/avatar/5bbde3a573d9012842f5fd261caa0bfe
Categories: Engineering
---

[WakaTime][wakatime] is like fitbit for programmers, and we are always looking for new ways to visualize our data.
Our dashboard is great for seeing project, file, and branch level visualizations over various time ranges, but it can't create custom queries of your data.
You could use our [api][api], but we have an easier way...

### Introducing wakadump!

Using [wakadump][wakadump], you can easily export your WakaTime data to [KeenIO][keenio] and take advantage of their powerful data explorer features.
For example, I queryied all my WakaTime data from the last 2 years and was quickly able to create these custom visualizations:

### Most productive day of the week

<img src="https://wakatime.com/static/img/blog/keenio-weekdays.png" alt="most productive weekday" width="100%" class="img-thumbnail"/>

### Top files worked in over the last 2 years

<img src="https://wakatime.com/static/img/blog/keenio-files.png" alt="top files" width="100%" class="img-thumbnail"/>

### Editor usage over the last 2 years

<img src="https://wakatime.com/static/img/blog/keenio-editors.png" alt="editor usage" width="100%" class="img-thumbnail"/>

### Programming languages used over the last 2 years

<img src="https://wakatime.com/static/img/blog/keenio-languages.png" alt="programming languages used over last 2 years" width="100%" class="img-thumbnail"/>

### Create your own visualizations

To create your own custom queries using the [KeenIO data explorer][keenio data explorer], just follow these steps:

1. Install [wakadump][wakadump] with:

    `sudo pip install wakadump`

2. Export your logged time from your [settings page][settings page].

3. Upload your WakaTime data to KeenIO by running this command:

    ```wakadump --input wakatime-user.json --format keen.io
    keen.io Project ID: 5570da806f31a24af926025e
    keen.io project Write Key: XXXX
    Preparing keen.io events...
    Uploading events to keen.io...
    Complete.```

4. Create custom queries using KeenIO's [Data Explorer][keenio data explorer]

If you find something interesting from your WakaTime data, please do share your insight in the comments or send me an email!

[api]: https://wakatime.com/api/
[wakadump]: https://github.com/wakatime/wakadump
[wakatime]: https://wakatime.com/
[settings page]: https://wakatime.com/settings
[keenio]: https://keen.io/
[keenio data explorer]: https://keen.io/blog/114588771746/introducing-data-explorer