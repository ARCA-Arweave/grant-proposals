# Permasnap Client T2 Proposal


## Completed in T1


### Required Deliverables

The required deliverables of Permansap T1 (Tranche 1) funding round have been completed.

-   Secure Functioning Backend on staging server ✔️
-   Debug App for testing within Arweave Community ✔️

### Actual Deliverables

Breakdown of what has actually been delivered for T1:

#### Project Deliverables Completed 

-   Provides ultra-smooth, no-touch onboarding for new arweave users. 
-   Both server & client use the arca GW perma.online for all permaweb interactions

#### DPost server

-   Staging server is online and functioning
-   Implemented crypto functions & HTTP API
-   Validates signed transactions from clients
-   Posts to permaweb using permasnap delegated posting & centralised wallet

#### Permasnap Client

-   Built out backend to integrate secure mobile storage (Android KeyStore or Apple KeyChain) and connect it to redux, by using middlewares and implementing wrappers. This allows wallets to be securely stored in the device.
-   Generates a new wallet on first run of the app
-   Implemented crypto functions to match server's
-   Encodes & sends picture data structure to exacting specs for verification by the dpost server
-   Captures photos and tracks upload mining queue
-   Mocked up & implemented a basic UI with some branding and icons
-   User's screen to view & track user's uploads
-   Search screen to view pictures already stored on the permaweb, ability to view by user (wallet) or by hashtag
-   Built internal test builds for iOS & Android
	-   <https://play.google.com/apps/internaltest/4700263995590825951> (give me your gmail account if you do not have already have access)
	-   iOS debug IPA pinned in the #permasnap channel

## T2 Client Proposals

The scope of this proposal is for finishing out the Permasnap mobile client, concentrating on the UI & UX of the mobile app. It is envisioned there will be other grant proposals for further permasnap bounties & dpost server improvements.

### SECTION A. List of Features to Implement / Bugs to Squash

#### UI/UX

1.  Flesh out UI/UX storyboards & mockups, building on the current branding/style.

#### Screens & Info for Display & Editing

2.  Show screen when new wallet loaded/generated 
	-  Enforced arweave-id name creation 
	-  Explanation about wallets, display wallet data
3.  Screen to view single image and associated data
4.  Image comment thread. Allow users to comment on images
5.  Source & display provable image datetime from block
6.  Slick, animated, engaging walkthrough - intro to arweave, explanations. Opt-in, not forced on first load
7.  Fix splashscreen issues: image skewed on some narrow screens & hidden too soon
8.  Android: double-tap back to exit app

#### Network, Upload, & Mining - Notifiers & Handlers

9.  Network & server bad connectivity handling
10.  Automatically handle upload errors and mining errors
11.  Picture upload progress indicator
12.  Push notifications when transaction is mined and image is ready to be shared

#### Caching & Performance

13.  Implement better data caching to prevent long load times
14.  Pagination (inf scroll) of images
15.  Pull to refresh on all feeds

#### Anonymity & Privacy

16.  Make anonymization the default for uploads:
	- Strip out identifying EXIF data (but re-add things like Picture Orientation)
	-  Random minor adjustments by resizing/cropping/scaling the photo very slightly & re-encoding.
	-  [Avoid-Camera-Noise-Signatures](https://www.instructables.com/id/Avoiding-Camera-Noise-Signatures/) 
	-  OPT-IN. Generate a random throw away wallet each time

#### Sharing & Phone Gallery Uploads

17.  Use deep linking to add option to upload from phone's gallery to the permaweb
18.  Option to share pictures from the app using other installed mobile apps (e.g. WhatsApp, Telegram, etc)

### SECTION B. Possible T2 Inclusions, Bounty, or Next Tranche T3

#### General

-   Add video capture & upload capability - needs research, if trivial => T2

-   OPT-IN anonymization: Option to blur people's faces in uploads. Needs research

-   Update FilesystemProvider to use new Capacitor API (Android 10 crash issue, feature currently omitted)

-   Opt-in geo-location data to add to picture uploads

-   "Rate app" popup functionality (not necessary until market release)

-   Design & implement trending search algorithm <= broad specification

-   User/hashtag following

#### Wallet related functionality

-   Allow multiple wallets

-   Import/export wallet by json file <= probably will never be included, possibly hidden in advanced option & not recommended. Could it get apps banned from app stores? Primary argument for not including: it's ugly and deprecated by app core premises

-   Import/export wallet by passphrase to encrypted wallet stored on the permaweb

-   Wallet linking: link wallet ownership to another wallet. <= will need some implementing app(s) outside of permasnap

#### On the permaweb

-   Slick looking permaweb web page to view well displayed pictures/videos. This would be the page people get sent to when they receive a shared link. 

-   Opportunity to display explanatory text & links about permasnap & arweave to potential new users. 

-   The txid of the media to view should be be passed as a URL Parameter to the page's code

-   Allow view/add user comments from web as well as in-app

### SECTION C. DPost Server

The DPost server will use bundled transactions once the full protocol backend is released in Arweave 2.1.

-   Upgrade to bundled transactions API 

-   Generalise the DPost server (not just for Permasnap Client)

## Funding Requirements

For the initial funding phase we put a price tag of 2055 DAI including server rental, Google & Apple developer licenses, and design & developers costs. On mature review this figure seems a little low now.

By using ad-hoc grouping, splitting, and general reckoning of the 21 tasks listed in SECTION A, I would guesstimate 15 substantial jobs are involved in developing this part of Permasnap Client T2. At just 160 DAI per job that takes the total to 160*15 =  2,400 DAI. I have also bartered a rock-bottom 200 DAI deal for the UI/UX.

Grand total 160*15+200 = **2,600 DAI**

I would suggest individual bounties to be taken out on extra features in SECTION B, especially "On the Permaweb".

DPost server is to be spun out into its own project, as outlined in SECTION C.
