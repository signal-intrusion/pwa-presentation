







# Progressive Web Applications, Service Workers, and You

**by Christopher Plummer**


















**Christopher Plummer**

t: @IntrusionSignal

gh: github.com/signal-intrusion

w: signalintrusion.com





















__What is a Progressive Web Application?__
















> There's no such thing as a Web App. It's all just websites.




















More Website...................................................More Web App

zombo.com -> bostonglobe.com -> netflix -> Twitter -> Twitch -> Google Docs

























Alex Russell (Google, TAG, TC39) asks:

> Who uses a web-based email client on their _desktop_?

> Who uses a web-based on client on their _phone_?
























Native
- [x] Fast
- [x] Reliable
- [x] Enagaging
- [x] Access to hardware
- [ ] Cross-platform






















Web Site
- [?] Fast
- [?] Reliable
- [?] Enagaging
- [ ] Access to hardware
- [x] Cross-platform



















Progressive Web App
- [x] Fast
- [x] Reliable
- [x] Enagaging
- [x] Access to hardware
- [x] Cross-platform
















PWAs attempt to fulfill the long held goal of creating **cross-platform** applications by leveraging the _most widely distributed, dynamic, and open_ application runtime environment: the web browser.


















## Goals
1. Reliability
2. Performance
3. Engagement
















### Reliability
- Lie-fi
- Offline
- Secure














### Performance

- fast first load, instant second load
- No big downloads!
- Aggressive caching & preloading
- Responsively loading assets
- http/2 and server push

















### Engagement

- Real-time
- First-Class status
  - Add to Home Screen
  - Lives in applications dir
  - Next to other apps in Windows Metro
- Push notifications
- Hardware access
  - geolocation, bluetooth, camera
  - `https://whatwebcando.today`
























How do we make those things happen?

__https, ssl, HTTP/2__
__Service Workers__
__fetch__
__App Manifest__















# HTTP/2 & SSL

- HTTP/2 allows us to serve files faster: multiplexing & server push
- https is **table stakes.** It's required for Service Workers and other browser features.
















__Achievements unlocked: Performance, Reliability.__

















# Service Workers

JS Worker that allows us to execute tasks in the background.

















## Features:

- Lifecycle Hooks
 - installing, active, idle, redundant

- Reactive, event based
 - Wait for events while idle, then activate
   - Receive and handle messages
   - Intercept network requests

























**Fetch** + _Service worker_ allows us to intercept requests to the server and inject middleware.














- Cache assets
- Preload pages, assets, data
- Manipulate caches directly
- Cache HTML (!!!)


__Offline mode!__



















*show basic caching*

*show advanced caching*
















What else can we do with _Service Workers_?

- We can also handle **push notifications**.
- Sync changes when online access is restored.
- Precache data a user might need in the future in the background.
- Background data synchronization
- Receiving updates to services like geolocation or gyroscope
- Sharing data across web pages
- Client-side compiling and dependency management for dev purposes






















__Achievements unlocked: Performance, Reliability, Engagement__





















_PRPL Pattern_

_Push_
_Render_
_Pre-cache_
_Lazy-load_




















# App Manifest

Manifest lets us define metadata about our application and gives it _first-class_ status on a device.

- Fullscreen
- Icons
- Permissions
- Security policies
- ...and more!


Allows your users to _add your app to the home screen_ and enables **full-screen mode**













*show portfolio add to home screen*















__Achievements unlocked: Engagement__



















## Business Case:














### PWA vs. website

* _53%_ of users leave a site if it takes more than 3 sec to load
  - src: https://www.doubleclickbygoogle.com/articles/mobile-speed-matters/

* _7%_ of customers abandon after 1sec load time
  - src: http://www.aberdeen.com/research/5136/ra-performance-web-application/content.aspx

* Avg. load time for mobile sites is **19 sec.**
  - src: https://www.doubleclickbygoogle.com/articles/mobile-speed-matters/

















* More reliable
* More performant
* More engaging
* More secure



















Before we talk about native mobile apps...



















### PWA vs. native






















* Cost to acquire a new customer has **doubled** since 2014

  - **$7.53** CPM, **$2.51** CPLU
    - src: https://fiksu.com/resources/mobile-cost-indexes

  - **$3.59** CPI (gaming only)
    - src: https://www.chartboost.com/insights/





















* The top three apps get _80%_ of the downloads.

* App store conversion rate is about _26%_
  - src: https://splitmetrics.com/blog/whats-a-good-app-store-page-conversion-rate/

* Each step can cost you _20%_ of your audience
  - src: http://blog.gaborcselle.com/2012/10/every-step-costs-you-20-of-users.html






















* _66%_ of mobile users download 0 app / month
  - _18%_ download 1 or 2
  - src: comScore, Quartz, https://qz.com/253618/most-smartphone-users-download-zero-apps-per-month/

* _75%_ download 1+ app per month
  - avg _0.65 - 1.5_ downloads/month
  - src: Tune, https://www.tune.com/blog/no-the-average-american-does-not-download-0-apps-each-month/





















* _23%_ of mobile apps abandoned after one use
  - src: http://info.localytics.com/blog/24-of-users-abandon-an-app-after-one-use























## Who is doing this?

Twitter
YouTube
Weather Channel
Washington Post
The Guardian
Alibaba
Air Berlin

...and a bunch more!


















Progressive Web Applications are the next Responsive Design



















## Useful Links

Google Web Developers: Progressive Web Apps
   `https://developers.google.com/web/progressive-web-apps/)`

awesome-pwa
  `https://github.com/hemanth/awesome-pwa`

What Web Can Do Today
  `https://whatwebcando.today/`

Offline Cookbook
  `https://jakearchibald.com/2014/offline-cookbook/`

MDN Service Worker Guide
  `https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API`

W3C Service Worker Specification
  `https://www.w3.org/TR/service-workers-1`











**Christopher Plummer**

t: @IntrusionSignal

gh: github.com/signal-intrusion

w: signalintrusion.com






