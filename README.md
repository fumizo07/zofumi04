[![syntax](https://img.shields.io/badge/syntax-AdGuard-%23c61300.svg)](https://kb.adguard.com/en/general/how-to-create-your-own-ad-filters)
[![syntax](https://img.shields.io/badge/syntax-uBlock%20Origin-%23c61300.svg)](https://github.com/gorhill/uBlock/wiki/Static-filter-syntax)

### Important Announcement (Sept. 30, 2022) 

Update (Oct. 7, 2022) If nobody complains, I'll also discontinue AdGuard Social media Plus and archive the current adblock repository (related issue: https://github.com/Yuki2718/adblock/issues/67). AdGuard DNS Unbreaker, coming AdGuard Japanese filters Plus, and dynamic ruels for uBlock Origin will be moved to a new repository.

Due to changes in my life, I'm going to unmaintain following lists until late October:

- Yuki's uBlock Japanese filters
- Yuki's uBlock Japanese filters - Paranoid
- Yuki's uBlock Japanese filters - Mobile
- Yuki's uBlock Japanese filters - Social
- Yuki's uBlock Japanese filters - Annoyances and its sublists
- Yuki's uBlock Japanese filters - Annoyances Plus
- Anti Anti-adblock Enhancer for AdGuard

I apologize to current user and all the contributor of these lists, but it's unavoidable. I hope you can find a good alternatives. I'll create and maintain AdGuard Japanese filter Plus which will to some extent compensate the difference between Yuki's uBlock Japanese filters and AdGuard Japanese filter.

Now Placeholder Hider with no generic hiding is deprecated and removed from this repo.

# adblock

<strong>Personal filters and rules for AdGuard/uBlock Origin</strong>

I can't guarantee these filers won't cause problems. If you found problems, report that by filling in all the mandatory items in Issue template; otherwise reports may not be addressed. Anyone who uses my filters/rules shall be deemed to have agreed that I have no responsibility or liability for costs, losses, damages, etc. arising from the use of the filters/rules. Unless Subscribe link is provided, these filters/rules are assumed to be copied and pasted, or imported, into My filters/rules (uBlock Origin) or User Rules (AdGuard).

<details>
<summary><strong>adguard</strong></summary>

<strong>Do NOT check the "Trusted" box if you subscribe Social media Plus and/or Tracking Protection Plus!</strong>
Because not needed. Trusted filters can inject javascript into pages and thus can potentially be risky. Of course I'm not going to do anything nasty with any of my filters, but imagine what if my Github account was hacked. I'd like to encourage a basic security practice.

### AdGuard Social media Plus

[AdGuard Social media filter](https://kb.adguard.com/en/general/adguard-ad-filters#social) tends to rely too much on cosmetic filters IMHO. This list consists of network filters only and complements Social media filter.
- `||connect.facebook.net^*/sdk.js`
- `||platform.twitter.com/widgets.js`
- `||static.evernote.com^$third-party`

are commented out as some people will need them. Those who don't need them can add them to User Rules without the initial `!`.

Exclusion:
- Follow buttons & comment widgets - they can be useful to some people and often Social media filter doesn't block them.

<a href="https://subscribe.adblockplus.org/?location=https://raw.githubusercontent.com/Yuki2718/adblock/master/adguard/social-plus.txt&title=AdGuard%20Social%20media%20Plus">Subscribe</a>
[View List](https://raw.githubusercontent.com/Yuki2718/adblock/master/adguard/social-plus.txt)

### Anti Anti-adblock Enhancer for AdGuard

<strong>Check Trusted box if you use this list as you trust me! To get the most of the list, you have to turn HTTPS filtering on AND DNS filtering OFF. It's not that I recommend to turn DNS filtering off generally, but that this list requires doing so for full function.</strong>

Enhances anti anti-adblock capability of AdGuard by generic filters. Works on AdGuard for Windows, AdGuard for Android, AdGuard for Mac, and AdGuard Browser Extensions but not for AdGuard for Safari, AdGuard for iOS, and AdGuard Contents Blocker. The list never address individual cases so report blocker detection to AdGuard and not here. This list also mitigates malicious popups often seen on porn sites, pirate sites, and/or short links. Since most of filters are taken from uBlock filters, this list is provided under the same license of GPLv3.

<a href="https://subscribe.adblockplus.org?location=https://raw.githubusercontent.com/Yuki2718/adblock/master/adguard/anti-antiadb.txt&title=Anti%20Anti-adblock%20Enhancer%20for%20AdGuard">Subscribe</a>
[View List](https://raw.githubusercontent.com/Yuki2718/adblock/master/adguard/anti-antiadb.txt)

## AdGuard DNS filter Unbreaker for Japanese

This list fixes known problems in AdGuard DNS filter mostly for Japanese user. Do not report any problem of AdGuard DNS filter directly to this repo, but open an issue ticket in AdGuardSDNSFilter repo.

[View List](https://raw.githubusercontent.com/Yuki2718/adblock/master/adguard/dns-unbreak.txt)

</details>

<details>
<summary><strong>japanese</strong></summary>

[日本語](/japanese/README-JP.md)

<strong>If you are a non-native Japanese speaker seeking for a good Japanese list, my first recommendation is [AdGuard Japanese filter](https://kb.adguard.com/en/general/adguard-ad-filters#japanese)</strong>. My lists include some aggressive rules not well-tested outside Japanese sites and likely to cause false positive on your local sites. There are also many duplicate rules of uBlock Origin's default lists. These lists are made to address a peculiar situation among Japanese ad-block user that many of them unsubscribe default lists and keep only a Japanese one. If you proceed, you shall be deemed to have read the [Japanese README](/japanese/README-JP.md) which gives more details, because those who need my lists should be able to read it.

### Yuki's uBlock Japanese filters

The most comprehensive, block-first, and efficient Japanese list **only for uBlock Origin** that removes ads and analytics on PC. Some rules are taken from - or rather intentionally made to be identical with - [EasyList, EasyPrivacy](https://easylist.to/), [AdGuard Base, AdGuard Tracking Protection](https://kb.adguard.com/en/general/adguard-ad-filters), [uBlock Built-in lists](https://github.com/uBlockOrigin/uAssets/), [Peter Lowe's list](https://pgl.yoyo.org/adservers/), [Fanboy's Enhanced Trackers List](https://www.fanboy.co.nz/filters.html), [EasyList China](http://abpchina.org/forum/forum.php), [RU AdList](https://forums.lanik.us/viewforum.php?f=102), [280blocker domain list](https://280blocker.net/download/), and [Brave Unbreak](https://github.com/brave/adblock-lists)<sup>1</sup>. This way even if an user added any of those lists along with my list, those duplicates will be discarded and thus can do no harm. This list is also strongly influenced by [Tofu filter](http://tofukko.r.ribbon.to/abp.html) though rules are not directly taken to avoid copy right infringement.

<sub>1: uBlock Built-in and 280blocker domain list are out of CC BY-SA license. I hope and believe rules taken from them are within a range of what filter authors can generally think of.　Brave Unbreak is under MIT license.</sub>

<a href="https://subscribe.adblockplus.org?location=https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/jp-filters.txt&title=Yuki's%20uBlock%20Japanese%20filters">Subscribe</a>
[View List](https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/jp-filters.txt)

### Yuki's uBlock Japanese filters - Mobile

Add this if you use Yuki's uBlock Japanese filters with uBlock Origin on Firefox for Mobile.

<a href="https://subscribe.adblockplus.org?location=https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/jp-mob.txt&title=Yuki's%20uBlock%20Japanese%20filters%20-%20Mobile">Subscribe</a>
[View List](https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/jp-mob.txt)

### Yuki's uBlock Japanese filters - Paranoid

This can be added to Yuki's uBlock Japanese filters for enhanced blocking. Use at your own risk. Some rules are taken from or influenced by [EasyPrivacy](https://easylist.to/), [Fanboy's Enhanced Trackers List](https://www.fanboy.co.nz/filters.html), and gwarser's [Block access to LAN](https://github.com/gwarser/filter-lists/blob/master/lan-block.txt) list.

<a href="https://subscribe.adblockplus.org?location=https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/jp-paranoid.txt&title=Yuki's%20uBlock%20Japanese%20filters%20-%20Paranoid">Subscribe</a>
[View List](https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/jp-paranoid.txt)

### Yuki's uBlock Japanese filters - Social

Removes some social elements such as share buttons mainly on Japanese sites. Some rules are taken from [AdGuard Social media](https://kb.adguard.com/en/general/adguard-ad-filters#social).

<a href="https://subscribe.adblockplus.org?location=https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/jp-social.txt&title=Yuki's%20uBlock%20Japanese%20filters%20-%20Social">Subscribe</a>
[View List](https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/jp-social.txt)

### Yuki's uBlock Japanese filters - Annoyances

Removes annoyances mainly on Japanese sites. Some rules are taken from or influenced by [AdGuard Annoyances](https://kb.adguard.com/en/general/adguard-ad-filters#annoyances-filter), [Fanboy Annoyances](https://www.fanboy.co.nz/index.html), [uBlock filters – Annoyances](https://github.com/uBlockOrigin/uAssets/blob/master/filters/annoyances.txt), and [Web Annoyances Ultralist](https://github.com/yourduskquibbles/webannoyances).

<a href="https://subscribe.adblockplus.org?location=https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/jp-annoyances.txt&title=Yuki's%20uBlock%20Japanese%20filters%20-%20Annoyances">Subscribe</a>
[View List](https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/jp-annoyances.txt)

### Yuki's uBlock Japanese filters - Annoyances Plus

Removes annoyances which only some user, not everyone, want to remove mainly on Japanese sites.

<a href="https://subscribe.adblockplus.org?location=https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/jp-annoyances-plus.txt&title=Yuki's%20uBlock%20Japanese%20filters%20-%20Annoyances%2B">Subscribe</a>
[View List](https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/jp-annoyances-plus.txt)

### Yuki's Cookie Dialogue filters (formerly Sable filters 2)

Inspired by [Sable filters](http://meetingwords.com/RK2njtyC7k), this removes cookie consents. Main targets are Japanese sites and other high-traffic sites many Japanese people may visit. False-positive prone rules won't be added. Included in Yuki's uBlock Japanese filters - Annoyances

<a href="https://subscribe.adblockplus.org/?location=https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/sabre-filters2.txt&title=Sabre%20filters%202">Subscribe</a>
[View List](https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/sabre-filters2.txt)

### Yuki's Blog parts filters

Removes blog parts and ranking buttons on Japanese websites. Included in Yuki's uBlock Japanese filters - Annoyances

Exclusion:
- Potentially useful parts or buttons
- Buttons for simple search sites without ranking function
- Buttons on adult sites except for some common ones (see above)

<a href="https://subscribe.adblockplus.org?location=https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/blog-parts.txt&title=Yuki's%20Blog%20parts%20filters">Subscribe</a>
[View List](https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/blog-parts.txt)

### Yuki's Blogroll filters

Removes blogroll (feed-style mutual links) on Japanese sites. Included in Yuki's uBlock Japanese filters - Annoyances

<a href="https://subscribe.adblockplus.org?location=https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/blogroll.txt&title=Yuki's%20Blogroll%20filters">Subscribe</a>
[View List](https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/blogroll.txt)

### Yuki's Mobile App filters

Blocks mobile app banners. Included in Yuki's uBlock Japanese filters - Annoyances

<a href="https://subscribe.adblockplus.org?location=https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/mob-app.txt&title=Yuki's%20Mobile%20App%20filters">Subscribe</a>
[View List](https://raw.githubusercontent.com/Yuki2718/adblock/master/japanese/mob-app.txt)

</details>

<details>
<summary><strong>medium_mode</strong></summary>

All the filters/rules in this category are for uBlock Origin. dynamic-rules.txt or dynamic-rules-mob.txt can be imported to My rules whereas anti-allowlist.txt and/or static-rules.txt should be copied and pasted into My filters. You can subscribe the latter two instead by importing their raw text URL into Filter lists, but as they are not frequently updated I don't make them subscription filter.

### Yuki's uBlock Anti-allowlist (anti-allowlist.txt)

This is to counter unnecessary or too generic allowlists which were not addressed or won't be addressed by the maintainer. Only for advanced user as it can cause problems.

[View List](https://raw.githubusercontent.com/Yuki2718/adblock/master/medium_mode/anti-allowlist.txt)

### Yuki's uBlock Dynamic Rules (dynamic-rules.txt)

Nooplists for medium mode of uBlock Origin dedicated for English user. The objective is to help those non-techie, yet security-conscious, people to use the mode. Payment services and mobile sites are out-of-scope<sup>1</sup>. In addition, following rules are included (Update: removed `* localhost * block` as it causes trouble on some particular case):

- `file-scheme * 1p-script block`
- `file-scheme * inline-script block`

[View Rules](https://raw.githubusercontent.com/Yuki2718/adblock/master/medium_mode/dynamic-rules.txt)

### Yuki's uBlock Dynamic Rules for mobile (dynamic-rules-mob.txt)

Mobile version of Yuki's uBlock Dynamic Rules

[View Rules](https://raw.githubusercontent.com/Yuki2718/adblock/master/medium_mode/dynamic-rules-mob.txt)

Q: Why X is nooped, it's bad!

A: See the purpose, this list is built to make as few breakage as possible for as many English user. This doesn't mean it should be used 'as is' - still each user should train their rules (obviously you have to add many rules if you browse non-English sites). Even with lax rules medium mode is much better than easy mode in terms of blocking.

<sub>1: I live in Japan and don't have full access to US, UK, etc. payment/shopping/banking services. Until you get accustomed to medium mode, it may be advisable to turn medium mode off on such sites. They anyway know much about you.</sub>

</details>

#### Notable users of my lists

[dbl.oisd.nl | Internet's #1 domain blocklist](https://oisd.nl/)

[spirillen's uBlockOrigin Rules](https://mypdns.org/my-external-stuff/ublockorigin-rules)

#### Acknowledgements

I use [PyFunceble](https://github.com/funilrys/PyFunceble) to screen potential dead domains. I thank all ad- and contents-blocking community members who helped me to learn right filter writing.
