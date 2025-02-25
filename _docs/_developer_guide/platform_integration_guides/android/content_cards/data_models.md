---
nav_title: Data Models
page_order: 5
search_rank: 5
platform: Android
---

## Card Types {#card-types-for-android}
Braze has 3 unique Content Cards card types which share a base model. Each card type also has additional card-specific properties which are listed below.

### Base Card {#base-card-for-android}

The [Base Card][29] model provides foundational behavior for all cards.  

|Property | Description |
|---|---|
|`getId()` | Returns the card’s ID set by Braze.|
|`getViewed()` | Returns a boolean reflects if the card is read or unread by the user.|
|`getExtras()` | Returns a map of key-value extras for this card.|
|`getCreated()`  | Returns the unix timestamp of the card’s creation time from Braze.|
|`getIsPinned` | Returns a boolean that reflects whether the card is pinned.|
|`getOpenUriInWebView()`  | Returns a boolean that reflects whether Uris for this card should be opened <br> in Braze's WebView or not.|
|`getExpiredAt()` | Gets the expiration date of the card.|
|`getIsRemoved()` | Returns a boolean that reflects whether the end user has dismissed this card.|
|`getIsDismissible()`  | Returns a boolean that reflects whether the card is pinned.|

### Banner Image Card {#banner-image-card-for-android}
[Banner Image Cards][30] are clickable full-sized images. In addition to the base card properties:

|Property | Description |
|---|---|
|`getImageUrl()` | Returns the URL of the card’s image.|
|`getUrl()` | Returns the URL that will be opened after the card is clicked. It can be a http(s) URL or a protocol URL.|
|`getDomain()` | Returns link text for the property URL.|

### Captioned Image Card {#captioned-image-card-for-android}
[Captioned Image Cards][31] are clickable full-sized images with accompanying descriptive text. In addition to the base card properties:

|Property | Description |
|---|---|
|`getImageUrl()` | Returns the URL of the card’s image.|
|`getTitle()` | Returns the title text for the card.
|`getDescription()` | Returns the body text for the card.
|`getUrl()` | Returns the URL that will be opened after the card is clicked. It can be a http(s) URL or a protocol URL.
|`getDomain()` | Returns the link text for the property URL.

### Classic Card {#text-Announcement-card-for-android}
[Text Announcement Cards][32] are clickable cards containing descriptive text. In addition to the base card properties:

|Property | Description |
|---|---|
|`getTitle()` | Returns the title text for the card.
|`getDescription()` | Returns the body text for the card.
|`getUrl()` | Returns the URL that will be opened after the card is clicked. It can be a http(s) URL or a protocol URL.
|`getDomain()` | Returns the link text for the property URL.

[1]:{% image_buster /assets/img_archive/contentcard.png %}
[2]: http://developer.android.com/guide/components/fragments.html
[3]: http://developer.android.com/guide/components/fragments.html#Adding "Android Documentation: Fragments"
[4]: {{ site.baseurl }}/developer_guide/platform_integration_guides/android/analytics/tracking_sessions/
[5]: https://github.com/Appboy/appboy-android-sdk/blob/master/droidboy/src/main/java/com/appboy/sample/DroidBoyActivity.java
[6]: https://appboy.github.io/appboy-android-sdk/javadocs/com/appboy/Appboy.html#logFeedDisplayed--
[7]: https://appboy.github.io/appboy-android-sdk/javadocs/com/appboy/models/cards/Card.html#logClick--
[8]: https://appboy.github.io/appboy-android-sdk/javadocs/com/appboy/models/cards/Card.html#logImpression--
[9]: {{ site.baseurl }}/developer_guide/platform_integration_guides/web/news_feed/#card-types
[14]: {{ site.baseurl }}/help/best_practices/news_feed/
[16]: https://appboy.github.io/appboy-android-sdk/javadocs/com/appboy/Appboy.html#requestFeedRefresh()
[18]: {% image_buster /assets/img_archive/Image27Theming.png %} "Android Feed"
[19]: {% image_buster /assets/img_archive/Image28Theming.png %} "Android Cards"
[20]: {% image_buster /assets/img_archive/Image29Theming.png %} "Android Empty"
[21]: {% image_buster /assets/img_archive/Image30Theming.png %} "Android Network Error"
[22]: {% image_buster /assets/img_archive/sample_news_feed.png %}
[23]: {% image_buster /assets/img_archive/android_news_feed.png %}
[25]: {% image_buster /assets/img_archive/UnreadvsReadNewsFeedCard.png %}
[26]: https://github.com/Appboy/appboy-android-sdk/blob/master/android-sdk-ui/res/drawable-hdpi/icon_unread.png
[27]: https://github.com/Appboy/appboy-android-sdk/blob/master/android-sdk-ui/res/drawable-hdpi/icon_read.png
[28]: https://github.com/Appboy/appboy-android-sdk/blob/master/droidboy/src/main/AndroidManifest.xml "AndroidManifest.xml"
[29]: https://appboy.github.io/appboy-android-sdk/javadocs/com/appboy/models/cards/Card.html
[30]: https://appboy.github.io/appboy-android-sdk/javadocs/com/appboy/models/cards/BannerImageCard.html
[31]: https://appboy.github.io/appboy-android-sdk/javadocs/com/appboy/models/cards/CaptionedImageCard.html
[32]: https://appboy.github.io/appboy-android-sdk/javadocs/com/appboy/models/cards/TextAnnouncementCard.html
[33]: https://appboy.github.io/appboy-android-sdk/javadocs/com/appboy/models/cards/ShortNewsCard.html
[36]: https://appboy.github.io/appboy-android-sdk/javadocs/com/appboy/models/cards/Card.html#getExtras--
[37]: https://github.com/Appboy/appboy-android-sdk/blob/master/android-sdk-ui/src/com/appboy/ui/feed/listeners/IFeedClickActionListener.java
[38]: https://github.com/Appboy/appboy-android-sdk/blob/master/droidboy/src/main/java/com/appboy/sample/CustomFeedClickActionListener.java
[39]: https://github.com/Appboy/appboy-android-sdk/blob/master/droidboy/src/main/java/com/appboy/sample/PreferencesActivity.java#L183
[40]: {{ site.baseurl }}/developer_guide/platform_integration_guides/android/advanced_use_cases/font_customization/#font-customization
