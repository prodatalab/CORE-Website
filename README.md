# New Community Website
---
### Live demo at: https://decentralize-colorado.github.io
---
## Goal:
A community run and maintained website that anyone can host and contribute to. It will be the place to go to find out what is going on in the Colorado Blockchain & DLT community. Resources will be available to get connected, to learn, and to get involved in all that is going on. 

## Key Content:

### An Event and Meetup Calendar

- [ ] Anyone can add events
  - [ ] Integrated form to submit any event.
    - [PeerPad](https://ipfs.io/ipns/peerpad.net/#/) as a way to do this? 
    - [ ] Creates an issue /pull request to the hosting repo.
    - [ ] Secondary system to allow full commit  access once approved.
- [ ] Automatically pulls new events from a linked site - like meetup.com
- [ ] Easy to use interface to add
- [ ] Can subscribe to updates via email
- [ ] linked with twitter bot to broadcast
- Inspiration:
      - http://getmeetingstar.com/
      - https://www.eventbrite.com/d/co--denver/events/
          - Use Cards for events vs. a calendar layout

### Three Community ways to Communicate/Interact Online: 

#### Community Chat
- [ ] Not hosted on the site, but linked.
- [ ] https://matrix.org based with bridges to various clients (riot to start)
  - slack + discord + riot ( + signal + wire + telegram + ....)

#### Community Bulletin Board (Blog)
- [ ] A forum for the community
    - Redit like? Discourse like?
(see below - almost the same framework needed for a wiki) 

#### A Community Wiki for resources
- [ ] Very likely a stand alone from the website itself - just linked/integrated
- [ ] Easy to contribute, highly navigable
- [ ] Easy to have community moderate
    - [ ] Thumbs up/down
    - [ ] Transparent flagging system
- Possible inspiration:
  - https://github.com/discourse/discourse
    - Use as a new community alt. to slack?
    - could qualify for
      - https://blog.discourse.org/2018/11/free-hosting-for-open-source-v2/
      - https://blog.discourse.org/2014/02/discourse-installs-for-non-profit-and-education/

  - https://github.com/rtfd/readthedocs.org
    - Backend to self host: http://www.sphinx-doc.org/en/master/
    - Documentation using **sphinx_rtd_theme** :point_left: :heart:
  - https://larecipe.binarytorch.com.my/docs/1.2/overview
  - https://www.gitbook.com/
  - https://www.mkdocs.org/
- Some key things to include (please add to the list :smile:):
        - https://alternativeto.net/list/818/how-to-live-without-google
        - Blockchain 101 links
        - Dev resources to self-learn
        - EFF cyber security recommendations
        - [ethviewer.live](ethviewer.live) website and blockchian expainers


### Map of Cryptocurrency Accepting Businesses

- [ ] Standalone service - linked/integrated into main website
  - [ ] Way for anyone to add/flag/review places
- [ ] Integration with Coinmap
  - https://coinmap.org/#/map/39.77529722/-104.95857239/11
   

### Media Highlights
- integration with:
  - [ ] youtube (https://www.youtube.com/channel/UCySU1TwgrLAU_1tF8lDt9bQ)
  - [ ] twitter (TBD)
  - [ ] medium (TBD)
  
## Desired Theme/Layout:
  - [ ] A **strong** sidebar with links
    - http://www.ethdocs.org/en/latest/index.html
    - Fixed as you scroll the main page
    - No header/footer needed / all inside the sidebar
    - https://larecipe.binarytorch.com.my
      - Can be hidden as a menu
        - Reactive:
          - Default open on desktop
          - Default close on phone


## Desired Architecture and Features:

We desire a distributed content hosting and contribution model. So that the content is redundant, those using it support and validate all peers, and are able to add content to the peer network. 

### Static Website

Desire no server side compute needed. Everyone who hosts our resources can be a server and client.
What does a static site model provide?
- [ ] Optimized SEO
- [ ] Lightning fast and light to host and load
- [ ] Flat pages as database
- [ ] Can be tracked in a Git repo - so history is maintained and easy to host among distributed peers

#### Easy Frontend Site Managment
- http://quasar-framework.org
  - Full Front end Framework, headless in that sense.
  - Build on Vue and easy to use/ learn
  - Very easy to get seomthing looking good with a lot of great components 

### Distributed Hosting / CDN:

Want to have a distributed / redundant store for the website. Ideally self hosting is very easy and secure. Want to get something like this: https://en.wikipedia.org/wiki/Content_delivery_network

An site can be hosted like this:
  - [ ] https://www.netlify.com/
    - global CDN
  - [ ] [PeerPad](https://ipfs.io/ipns/peerpad.net/#/) check out this as a model :point_left:
    - IPNS for human named data 
    - [PeerPad](https://ipfs.io/ipns/peerpad.net/#/) as way to edit events and give write access?


##### Self hosted site:

Want a very easy onboarding process - just install and you are a host + node for all the community resources.

  - To host the site under our own domain on IPFS, [this is pretty comprehensive](https://gist.github.com/claus/1287f47b5fbaaea338ac8a04d02bf258).
  - To upload site content to IPFS, and access it from IPFS gateway, and redirect our domain name to point to the IPFS gateway, [this article](https://medium.com/@chrismatthieu/hosting-a-website-via-ipfs-for-free-afee39b84553) goes over how to do that.
  - ***Make this IPFS a grain for https://sandstorm.io/***
  - And/or make a simple docker / other install for people
    - Could this be on mobile too? (needs to be lightweight enough)
    
To get started - and eventually compliment community hosing, use:
- GitHub/Lab Pages
- Firebase
- Netlify
- Other free options?
    
##### Other self hosted resources:
Wantt to make a set of services - keep this in mind when finding a Website hosting solution:
- cloud shared community data
  - media
  - project Git repos
  - chat server (federeated?)
  - wiki 

#### Distributed DNS:

- https://handshake.org/
  - Decentralized certificate authority and naming
An experimental peer-to-peer root DNS.

### Content Management System (CMS) for easy addition of select content

Build it integrated into the site - we can use Quazar to make pages that submit to IPFS backend?
- [ ] [PeerPad](https://ipfs.io/ipns/peerpad.net/#/)  does not rely on a second or third-party. All nodes talk to each other directly, without intermediation.
  - [ ] Ability to Add events
  - [ ] Blog type bulletin board
  
Also could use CMS
- [ ] Headless - so can use alternatives with SSG
 - https://snipcart.com/blog/react-graphql-grav-cms-headless-
- Possible CMS options:
    - https://getgrav.org
    - https://forestry.io/ (great integration for use with SSG and hosting on github)
    - https://plone.com/ (not a satic option)
    - http://gantry.org/ (grav SSG CSM)
    - WordPress
    - Drupal


