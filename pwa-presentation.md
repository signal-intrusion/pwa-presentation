









# Progressive Web Applications, Service Workers, and You

**by Christopher Plummer**


















**Christopher Plummer**

t: @IntrusionSignal

gh: github.com/signal-intrusion

w: signalintrusion.com





















__What is a Progressive Web Application?__
















> There's no such thing as a Web App. It's all just websites.




















More Website.................................................More Web App

zombo.com -> bostonglobe.com -> netflix -> Twitter -> Twitch -> Google Docs



















What about Mobile, Native, Desktop?
















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
















PWAs finally fulfill the long held goal of creating **cross-platform** applications by leveraging the _most widely distributed, dynamic, and open application_ runtime environment: the web browser.


















## Goals
1. Reliability
2. Performance
3. Engagement
















### Reliability
- Offline
- Lie-fi
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
__App Manifest__















# SSL & HTTP/2

- https is required for Service Workers and other browser features. It's **table stakes.**
- HTTP/2 allows us to serve files faster: multiplexing & server push














__Achievements unlocked: Performance, Reliability.__

















# Service Workers

JS that allows us to execute tasks in the background.
















## Features:

- Lifecycle Hooks
- Reactive, event based
















**Fetch** + _Service worker_ allows us to intercept requests to the server and inject middleware.














- Cache assets
- Preload pages, assets, data
- Manipulate caches directly
- Cache HTML (!!!)

__Offline mode!__



















*show basic caching*

*show advanced caching*















What else can we do?

- We can also handle **push notifications**.
- Sync changes when online access is restored.
- fetch data a user might need in the background.


















__Achievements unlocked: Performance, Reliability, Engagement__

















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














### vs. website

* 53% of users leave a site if it takes more than 3 sec to load
* More reliable
* More performant
* More engaging
* More secure

















Before we talk about native mobile apps...



















### vs. native












Alex Russell, google engineer, asks:

Who uses a web-based email client on their _desktop_?
Who uses a web-based on client on their _phone_?













#### Cost

* Cost to acquire a new customer has **doubled** since 2014

  - $7.53 CPM, $2.51 CPLU
    - src: https://fiksu.com/resources/mobile-cost-indexes

  - $3.59 CPI (gaming only)
    - src: https://www.chartboost.com/insights/

* The top three apps get 80% of the downloads.

* 23% of mobile apps abandoned after one use
  - src: http://info.localytics.com/blog/24-of-users-abandon-an-app-after-one-use















* 66% of mobile users download 0 app / month
  - 18% download 1 or 2

* App store conversion rate is about 26%
  - src: https://splitmetrics.com/blog/whats-a-good-app-store-page-conversion-rate/

* Download time matters!

* Each step can cost you 20% of your audience
  - http://blog.gaborcselle.com/2012/10/every-step-costs-you-20-of-users.html






























## Who is doing this?

Weather Channel
Washington Post
The Guardian
Alibaba
Air Berlin
Twitter

...and a bunch more!


















Progressive Web Applications are the next Responsive Design

















## Useful Links

Google Web Developers: Progressive Web Apps
   https://developers.google.com/web/progressive-web-apps/)

awesome-pwa
  https://github.com/hemanth/awesome-pwa

PWA Rocks
  https://pwa.rocks/




**Christopher Plummer**

t: @IntrusionSignal

gh: github.com/signal-intrusion

w: signalintrusion.com



