<div align="center">

<img src="./assets/profile-card.svg" width="100%" alt="GitHub profile card: Deependra Kashyap, @deependrakashya, Node.js Backend & Flutter Engineer, 16 public repos, 9 followers, 16 following, 4 pinned; achievements Pull Shark and YOLO; pinned MY-Docs-Releases, infinite_wallpapers, my_doctor_buddy, sonnetSync"/>

<p>
  <a href="https://www.linkedin.com/in/deependra-kashyap-08aa74268"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <a href="https://x.com/CodeByDeependra"><img src="https://img.shields.io/badge/X-000000?style=flat-square&logo=x&logoColor=white" alt="X"/></a>
  <a href="https://www.instagram.com/crashed_deependra"><img src="https://img.shields.io/badge/Instagram-E4405F?style=flat-square&logo=instagram&logoColor=white" alt="Instagram"/></a>
  <a href="mailto:deependrakashyapp@gmail.com"><img src="https://img.shields.io/badge/Gmail-EA4335?style=flat-square&logo=gmail&logoColor=white" alt="Gmail"/></a>
  <a href="https://play.google.com/store/apps/details?id=com.dtools.allfileviewer"><img src="https://img.shields.io/badge/Play_Store-My_Docs_is_live-34A853?style=flat-square&logo=google-play&logoColor=white" alt="Play Store"/></a>
  <img src="https://komarev.com/ghpvc/?username=deependrakashya&color=F59E0B&style=flat-square&label=views" alt="Profile views"/>
</p>

</div>

### `$ cat ~/about.yaml`

```yaml
name:      Deependra Kashyap
role:      Node.js Backend & Flutter Engineer
shipped:   10+ apps — Android, iOS and desktop, published on Google Play
backend:   REST APIs on Node.js + Express — auth, data modelling, file pipelines
mobile:    Flutter for Android & iOS, Kotlin when native speed matters
desktop:   Flutter on macOS, Windows & Linux
design:    API contracts, token auth, schema & index design, read-path performance
stores_in: [PostgreSQL, MongoDB, Firebase]
cares_about:
  - clean architecture that survives the next feature
  - performance you can measure, not just feel
  - code someone else can read in six months
learning:  [distributed systems, system design at scale, DSA]
goal:      "Build software that is fast, maintainable, and scalable."
```

<br/>

### `$ open system-design.svg`

<div align="center">
<img src="./assets/pipeline.svg" width="100%" alt="Flutter apps on Android, iOS and desktop with two outgoing paths: native path MethodChannel → Kotlin background thread → ML Kit OCR and SAF; backend path Express API (/api/v1, REST) → middleware (JWT, bcrypt) → PostgreSQL and MongoDB (indexes, aggregation)"/>
</div>

Half of my work is the client, half is the server it talks to. The top path is what makes **My Docs** fast on-device; the bottom path is the Node.js side: API design, auth and data modelling.

<br/>

### `$ cat design.md`

```text
api/        versioned REST (/api/v1) · one response + error envelope · async handler wrapper
auth/       short-lived JWT access token + refresh token · httpOnly, secure cookies · bcrypt
data/       schema and indexes designed first · aggregation pipelines for read-heavy views
files/      Multer → temp storage → Cloudinary · the database stores URLs, not blobs
clients/    offline-first on device · paginated, retry-safe calls over the network
scale/      stateless API instances · scale out behind a load balancer · cache hot reads
```

<br/>

### `$ ./stack --tree`

```text
.
├── backend/        Node.js · Express.js · REST · JWT · Mongoose · Multer · Cloudinary
├── data/           PostgreSQL · MongoDB · Firestore · Firebase Auth
├── system-design/  API design · auth flows · schema & indexing · caching · scaling
├── mobile/         Flutter · Dart · Kotlin · iOS · MethodChannels · Android SAF · ML Kit
├── desktop/        Flutter on macOS · Windows · Linux
├── state/          GetX · Provider · BLoC
├── patterns/       Clean Architecture · MVC · MVVM · Repository
└── tools/          Git · GitHub · Linux · VS Code · Postman · Google Play Console
```

<div align="center">
  <img src="https://skillicons.dev/icons?i=nodejs,express,js,ts,postgres,mongodb,firebase,postman,flutter,dart,kotlin,androidstudio,apple,linux,git,vscode,cpp,c&theme=dark&perline=9" alt="Stack icons"/>
</div>

<br/>

### `$ git log --oneline projects/`

```text
f2b6a90  feat(youtube-backend):     Node.js + Express video platform API with JWT auth
a1f3e2d  feat(my-docs):             document viewer for Android, macOS, Windows & Linux
b7c9d41  feat(my-doctor-buddy):     patient–doctor healthcare app on Firebase
c3e8f05  feat(sonnet-sync):         API-driven poetry app with offline bookmarks
d9a2b16  feat(ai-chatbot):          multi-model Gemini assistant
e5f7c38  feat(infinite-wallpapers): infinite-scroll gallery with native wallpaper setting
```

<table>
<tr>
<td width="50%" valign="top">

#### 🎬 YouTube Backend — Video Platform API
[![GitHub](https://img.shields.io/badge/GitHub-View_Repo-181717?style=flat-square&logo=github)](https://github.com/Deependrakashya/youtube_backend)

`Node.js` `Express 5` `MongoDB` `Mongoose` `JWT` `Cloudinary`

- Versioned REST API (`/api/v1`) with a shared response/error envelope
- **Access + refresh token auth** in httpOnly cookies, bcrypt-hashed passwords
- Avatar and cover uploads: **Multer → Cloudinary**
- Channel profiles and watch history built with **MongoDB aggregation**

</td>
<td width="50%" valign="top">

#### 📄 My Docs — Document & File Viewer
[![Play Store](https://img.shields.io/badge/Google_Play-Live-34A853?style=flat-square&logo=google-play&logoColor=white)](https://play.google.com/store/apps/details?id=com.dtools.allfileviewer)
[![Website](https://img.shields.io/badge/Website-My_Docs-F59E0B?style=flat-square&logo=googlechrome&logoColor=white)](https://deependrakashya.github.io/MY-Docs-Releases/)

`Flutter` `Kotlin` `MethodChannels` `ML Kit` `Provider`

- Ships on **Android, macOS, Windows and Linux** from one codebase
- Excel/PDF processing offloaded to **background threads over MethodChannels**
- **On-device OCR** with Google ML Kit · **Android SAF** for policy-compliant file access
- UI stays responsive while the heavy work runs elsewhere

</td>
</tr>
<tr>
<td width="50%" valign="top">

#### 🩺 My Doctor Buddy
[![GitHub](https://img.shields.io/badge/GitHub-View_Repo-181717?style=flat-square&logo=github)](https://github.com/Deependrakashya/my_doctor_buddy)

`Flutter` `Dart` `Firebase Auth` `Firestore`

- Patient–doctor interaction layer on clean Flutter architecture
- **Firebase Auth + Firestore** for real-time, secure data flows
- Accessible, healthcare-oriented UI on Android & iOS
- Data model built to grow with new features

</td>
<td width="50%" valign="top">

#### 🎵 Sonnet Sync — Poetry App
[![GitHub](https://img.shields.io/badge/GitHub-View_Repo-181717?style=flat-square&logo=github)](https://github.com/Deependrakashya/sonnetSync)

`Flutter` `REST APIs` `GetX` `AdMob` `MVVM`

- API-driven architecture with **GetX** state management
- Dynamic search & filtering
- **Offline-first bookmarks** stored locally
- AdMob placed so it never gets in the way

</td>
</tr>
<tr>
<td width="50%" valign="top">

#### 🤖 AI ChatBot
![Status](https://img.shields.io/badge/Status-Private-6B7280?style=flat-square)

`Flutter` `Gemini API` `REST APIs`

- **Multi-model Gemini** integration with context-aware responses
- API calls and rendering tuned for sub-100ms perceived latency
- Clean conversation state, responsive layout
- Modular, so new models slot in without rewrites

</td>
<td width="50%" valign="top">

#### 🖼️ Infinite Wallpapers
[![GitHub](https://img.shields.io/badge/GitHub-View_Repo-181717?style=flat-square&logo=github)](https://github.com/Deependrakashya/infinite_wallpapers)
[![APK](https://img.shields.io/badge/Download-APK-3DDC84?style=flat-square&logo=android&logoColor=white)](https://github.com/Deependrakashya/infinite_wallpapers/releases/download/Release/app-release.apk)

`Flutter` `Dart` `GetX` `REST APIs` `MVVM`

- Infinite-scroll gallery across categorized collections (Anime, Nature, Abstract…)
- Home & lock-screen wallpaper setting through native integrations
- Optimized image loading, caching, and rendering

</td>
</tr>
</table>

<br/>

### `$ gh stats --user deependrakashya`

<div align="center">

<img width="50%" src="https://github-readme-streak-stats2-eta.vercel.app?user=deependrakashya&theme=tokyonight&hide_border=true&background=0D1117&ring=F59E0B&fire=F59E0B&currStreakLabel=F59E0B&date_format=j%20M%5B%20Y%5D" alt="GitHub streak"/>
<img width="49%" src="https://github-readme-stats.vercel.app/api/top-langs/?username=deependrakashya&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=F59E0B&text_color=C9D1D9&langs_count=8" alt="Top languages"/>

<br/><br/>

<img width="100%" src="https://activity-graph.vercel.app/graph?username=deependrakashya&theme=tokyo-night&bg_color=0D1117&color=C9D1D9&line=F59E0B&point=F8FAFC&area=true&area_color=F59E0B&hide_border=true&custom_title=Daily%20contributions%20%E2%80%94%20last%2031%20days" alt="Line chart of daily GitHub contributions over the last 31 days"/>
<sub>Each point is one day's commits, PRs, issues and reviews · bottom axis is the day of the month, oldest on the left, today on the right</sub>

<br/>

<img src="https://trophygithubreadmelang.cybee.dpdns.org/?username=deependrakashya&theme=onedark&no-frame=true&no-bg=true&column=7&margin-w=8&margin-h=8" alt="GitHub trophies"/>

</div>

<br/>

### `$ node philosophy.js`

```js
class DeependraKashyap extends SoftwareEngineer {
  role = 'Node.js Backend & Flutter Engineer';

  async build(problem) {
    const understanding = await this.understand(problem); // first, solve the problem
    const design = this.architect(understanding);         // then design the system
    const product = await this.implement(design);         // then write the code
    return this.measure(product).optimize();              // then make it fast
  }
}
```

<br/>

### `$ cat contact.json`

<pre>
{
  "linkedin":  "<a href="https://www.linkedin.com/in/deependra-kashyap-08aa74268">https://www.linkedin.com/in/deependra-kashyap-08aa74268</a>",
  "x":         "<a href="https://x.com/CodeByDeependra">https://x.com/CodeByDeependra</a>",
  "instagram": "<a href="https://www.instagram.com/crashed_deependra">https://www.instagram.com/crashed_deependra</a>",
  "email":     "<a href="mailto:deependrakashyapp@gmail.com">deependrakashyapp@gmail.com</a>",
  "status":    "open to Node.js backend &amp; Flutter work"   // say hi
}
</pre>

<img src="./assets/terminal.svg" width="100%" alt="deependra@dev terminal: whoami → Node.js Backend & Flutter Engineer, 10+ apps shipped; node server.js → Express on :3000 with /api/v1 and JWT, Postgres, Mongo and Cloudinary ready; flutter run --release → MethodChannel Kotlin bridge and ML Kit OCR; cat design.md → versioned REST, stateless JWT auth, schema and indexes first"/>

<div align="center">

<br/>

> *"First, solve the problem. Then, write the code."* — John Johnson

</div>
