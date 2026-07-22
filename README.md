# 🌸 MamaCycle UG

**Mama's Cycle - Your Health, Your Strength, Your Future**

---

## 📖 Table of Contents
- [Project Overview](#project-overview)
- [Mission & Vision](#mission--vision)
- [Core Values](#core-values)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Project Structure](#project-structure)
- [Database Schema](#database-schema)
- [Firebase Security Rules](#firebase-security-rules)
- [Development Timeline](#development-timeline)
- [Installation & Setup](#installation--setup)
- [Deployment](#deployment)
- [Testing](#testing)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

---

## 🎯 Project Overview

**MamaCycle UG** is a free, offline-first Progressive Web App (PWA) designed specifically for women in Uganda. The name "MamaCycle" combines "Mama" (mother) and "Cycle" (menstrual cycle), representing a complete companion for women's reproductive health.

### The Problem We Solve

In Uganda, many women face challenges accessing reliable reproductive health information:
- Limited internet connectivity in rural areas
- Language barriers (English-only content)
- Privacy concerns around sensitive health data
- Lack of personalized health tracking tools
- Limited access to professional health advice

### Our Solution

MamaCycle UG provides:
- 📱 **Offline-first** - Works without internet connection
- 🌍 **Bilingual** - Full support for English and Luganda
- 🔒 **Privacy-focused** - Your data stays on your device
- 📊 **Smart tracking** - Period, fertility, and pregnancy predictions
- 📚 **Trusted content** - Health articles reviewed by professionals
- 💬 **Health worker access** - Connect with qualified professionals

---

## 🎯 Mission & Vision

### Mission
To empower every woman in Uganda with accessible, private, and culturally relevant reproductive health information and tracking tools, regardless of internet connectivity or language barriers.

### Vision
A Uganda where every woman has the knowledge and tools to make informed decisions about her reproductive health, leading to healthier families and stronger communities.

### Our Promise
- **Free forever** for all users
- **Private and secure** data handling
- **Culturally appropriate** content
- **Offline accessibility** for all core features
- **Continuous improvement** based on user feedback

---

## 💎 Core Values

| Value | Description |
|-------|-------------|
| **Privacy First** | Your health data belongs to you. We never share or sell your information. |
| **Inclusivity** | Every woman deserves access, regardless of location, language, or background. |
| **Trust** | All health content is verified and culturally appropriate for Ugandan women. |
| **Simplicity** | Clean, intuitive design that makes health tracking effortless. |
| **Community** | Connecting women with health professionals and each other. |
| **Innovation** | Using modern technology to solve real-world problems. |

---

## ✨ Features

### Phase 1 (MVP - Launch)
| Feature | Description | Status |
|---------|-------------|--------|
| Onboarding | 3-screen intro in English & Luganda | 🚧 Planned |
| Authentication | Google + Email sign-in | 🚧 Planned |
| Language Toggle | Switch between English & Luganda | 🚧 Planned |
| Period Tracker | Calendar with color-coded predictions | 🚧 Planned |
| Symptom Logger | Log mood, flow, pain, cramps, etc. | 🚧 Planned |
| Health Library | 20+ articles in both languages | 🚧 Planned |
| Offline Mode | Track cycles without internet | 🚧 Planned |
| Notifications | Period & symptom reminders | 🚧 Planned |

### Phase 2 (V1.5 - Post-Launch)
| Feature | Description | Priority |
|---------|-------------|----------|
| Fertility Predictions | Ovulation & fertile window estimates | 🔴 High |
| Cycle Analytics | Charts showing patterns & trends | 🔴 High |
| Pregnancy Mode | Dedicated pregnancy tracking | 🟡 Medium |
| Health Worker Chat | Secure messaging with professionals | 🟡 Medium |

### Phase 3 (V2.0 - Future)
| Feature | Description | Priority |
|---------|-------------|----------|
| Medication Reminders | Birth control & supplement tracking | 🟢 Low |
| Community Forum | Moderated peer support groups | 🟢 Low |
| Clinic Locator | Find nearby health facilities | 🟢 Low |
| Emergency Contacts | One-tap emergency numbers | 🟢 Low |

---

## 🛠️ Technology Stack

### Frontend
| Technology | Purpose | Version |
|------------|---------|---------|
| **React** | UI Framework | 18.2.0+ |
| **Vite** | Build Tool | 4.3.0+ |
| **Tailwind CSS** | Styling | 3.3.0+ |
| **React Router** | Navigation | 6.14.0+ |
| **React Hook Form** | Form Handling | 7.45.0+ |
| **Lucide React** | Icons | 0.263.0+ |
| **Recharts** | Charts & Analytics | 2.7.0+ |
| **Dexie.js** | IndexedDB Wrapper | 3.2.0+ |
| **Workbox** | Service Workers | 7.0.0+ |

### Backend (Firebase)
| Service | Purpose |
|---------|---------|
| **Firebase Auth** | Authentication (Google + Email) |
| **Firestore** | NoSQL Database |
| **Firebase Storage** | Image & File Storage |
| **Firebase Hosting** | PWA Hosting |
| **Firebase Cloud Messaging** | Push Notifications |
| **Cloud Functions** | Background Tasks (Optional) |

### Development Tools
| Tool | Purpose |
|------|---------|
| **VS Code** | Code Editor |
| **Git** | Version Control |
| **GitHub** | Repository Hosting |
| **Firebase CLI** | Deployment & Management |
| **Chrome DevTools** | Debugging |
| **Lighthouse** | PWA Performance Audit |
| **ESLint** | Code Quality |
| **Prettier** | Code Formatting |

### CI/CD (Planned)
```yaml
GitHub Actions → Build → Test → Deploy to Firebase Hosting
```

---

## 📂 Project Structure

```
mamacycle-ug/
│
├── public/
│   ├── icons/
│   │   ├── icon-72x72.png
│   │   ├── icon-192x192.png
│   │   ├── icon-512x512.png
│   │   └── favicon.ico
│   ├── manifest.json          # PWA Web App Manifest
│   └── index.html
│
├── src/
│   ├── screens/
│   │   ├── auth/
│   │   │   ├── Splash.jsx
│   │   │   ├── Onboarding.jsx
│   │   │   ├── Login.jsx
│   │   │   └── Register.jsx
│   │   ├── home/
│   │   │   ├── Home.jsx
│   │   │   ├── HealthLibrary.jsx
│   │   │   ├── ArticleDetail.jsx
│   │   │   └── AskHealthWorker.jsx
│   │   ├── tracker/
│   │   │   ├── Tracker.jsx
│   │   │   ├── LogSymptoms.jsx
│   │   │   └── CycleHistory.jsx
│   │   └── settings/
│   │       ├── Settings.jsx
│   │       ├── Profile.jsx
│   │       ├── Privacy.jsx
│   │       ├── HelpCenter.jsx
│   │       └── About.jsx
│   │
│   ├── components/
│   │   ├── common/
│   │   │   ├── Button.jsx
│   │   │   ├── Card.jsx
│   │   │   ├── Input.jsx
│   │   │   ├── BottomNav.jsx
│   │   │   └── Loader.jsx
│   │   ├── home/
│   │   │   ├── SummaryCard.jsx
│   │   │   ├── QuickActions.jsx
│   │   │   ├── TodayTip.jsx
│   │   │   └── NewsCard.jsx
│   │   └── tracker/
│   │       ├── Calendar.jsx
│   │       ├── PredictionCard.jsx
│   │       ├── SymptomChecklist.jsx
│   │       └── CycleChart.jsx
│   │
│   ├── services/
│   │   ├── firebase.js         # Firebase initialization
│   │   ├── auth.js             # Authentication functions
│   │   ├── firestore.js        # Firestore CRUD operations
│   │   ├── storage.js          # Offline (IndexedDB)
│   │   ├── notifications.js    # Push notification service
│   │   └── analytics.js        # Usage tracking
│   │
│   ├── hooks/
│   │   ├── useAuth.js
│   │   ├── useTracker.js
│   │   ├── useOffline.js
│   │   ├── useNotifications.js
│   │   └── useArticles.js
│   │
│   ├── context/
│   │   ├── AuthContext.jsx
│   │   ├── LanguageContext.jsx
│   │   └── ThemeContext.jsx
│   │
│   ├── utils/
│   │   ├── dates.js            # Date manipulation
│   │   ├── predictions.js      # Cycle prediction logic
│   │   ├── translations.js     # English/Luganda translations
│   │   ├── validators.js       # Form validation
│   │   └── constants.js        # App constants
│   │
│   ├── styles/
│   │   ├── globals.css         # Tailwind imports
│   │   ├── theme.js            # Color palette
│   │   └── typography.js       # Font configuration
│   │
│   ├── assets/
│   │   ├── images/
│   │   ├── illustrations/
│   │   └── fonts/
│   │
│   ├── App.jsx
│   ├── App.css
│   └── main.jsx
│
├── functions/                   # Firebase Cloud Functions
│   ├── index.js
│   └── package.json
│
├── .env                         # Environment variables (never commit)
├── .env.example
├── .gitignore
├── .eslintrc.js
├── .prettierrc
├── firebase.json                # Firebase configuration
├── firestore.indexes.json      # Firestore indexes
├── firestore.rules             # Firestore security rules
├── tailwind.config.js
├── vite.config.js
├── package.json
├── README.md
├── CONTRIBUTING.md
└── LICENSE
```

---

## 🗄️ Database Schema (Firestore)

### Collections & Documents

#### `users/{uid}`
```javascript
{
  uid: string,              // Firebase Auth UID
  name: string,             // User's full name
  email: string,            // Email address
  photoURL: string,         // Profile picture URL
  phone: string,            // Phone number (optional)
  age: number,              // User's age
  emergencyContact: {
    name: string,
    phone: string,
    relationship: string
  },
  cycleSettings: {
    lastPeriodStart: timestamp,  // Date of last period
    averageCycleLength: number,  // Days (default: 28)
    periodDuration: number,      // Days (default: 5)
    predictionMethod: string     // 'average' | 'calendar'
  },
  settings: {
    language: string,       // 'en' | 'lg'
    theme: string,          // 'light' | 'dark'
    fontSize: string,       // 'small' | 'medium' | 'large'
    notifications: boolean,
    offlineMode: boolean,
    privacy: {
      shareAnalytics: boolean,
      shareDataWithHealthWorkers: boolean
    }
  },
  createdAt: timestamp,
  updatedAt: timestamp,
  lastLogin: timestamp
}
```

#### `cycles/{autoId}`
```javascript
{
  userId: string,          // Reference to users/{uid}
  periodStart: timestamp,  // First day of period
  periodEnd: timestamp,    // Last day of period
  cycleLength: number,     // Days between cycles
  flowIntensity: string,   // 'light' | 'medium' | 'heavy'
  symptoms: {
    cramps: boolean,
    headache: boolean,
    bloating: boolean,
    backPain: boolean,
    breastTenderness: boolean,
    nausea: boolean,
    fatigue: boolean,
    acne: boolean,
    fever: boolean
  },
  mood: string,            // 'happy' | 'irritable' | 'sad' | 'anxious'
  painLevel: number,       // 1-10
  notes: string,
  createdAt: timestamp,
  updatedAt: timestamp
}
```

#### `symptoms/{autoId}` (Daily logs)
```javascript
{
  userId: string,          // Reference to users/{uid}
  date: timestamp,         // Date of log
  flow: string,           // 'none' | 'light' | 'medium' | 'heavy'
  cramps: boolean,
  headache: boolean,
  bloating: boolean,
  backPain: boolean,
  breastTenderness: boolean,
  nausea: boolean,
  fatigue: boolean,
  acne: boolean,
  fever: boolean,
  mood: string,           // 'happy' | 'neutral' | 'irritable' | 'sad' | 'anxious'
  painLevel: number,      // 1-10
  notes: string,
  createdAt: timestamp
}
```

#### `articles/{autoId}`
```javascript
{
  title: string,          // Article title
  slug: string,           // URL-friendly title
  category: string,       // 'menstrual' | 'sexual' | 'pregnancy' | 'parenting' | 'nutrition' | 'mental' | 'marital' | 'cervical'
  subcategory: string,    // More specific classification
  excerpt: string,        // Short preview
  coverImage: string,     // URL to image
  content: string,        // Main article content (HTML/Markdown)
  readingTime: number,    // Minutes
  author: string,         // Author name
  authorCredentials: string, // Medical credentials (if applicable)
  sources: array,         // List of sources
  publishedAt: timestamp,
  updatedAt: timestamp,
  translations: {
    luganda: {
      title: string,
      excerpt: string,
      content: string
    }
  },
  tags: array,           // Search keywords
  isVerified: boolean,    // Reviewed by health professional
  views: number,
  bookmarks: number
}
```

#### `chatMessages/{autoId}` (V1.5 - Future)
```javascript
{
  userId: string,          // Reference to users/{uid}
  healthWorkerId: string,  // Reference to health workers
  message: string,
  sender: string,          // 'user' | 'worker'
  timestamp: timestamp,
  read: boolean,
  attachments: array      // Image/voice note URLs
}
```

#### `syncQueue/{autoId}` (Offline sync management)
```javascript
{
  userId: string,
  action: string,         // 'create' | 'update' | 'delete'
  collection: string,     // 'cycles' | 'symptoms' | 'users'
  documentId: string,     // Document ID
  data: object,           // Full document data
  status: string,         // 'pending' | 'synced' | 'failed'
  attempts: number,
  error: string,
  createdAt: timestamp,
  updatedAt: timestamp
}
```

---

## 🔒 Firebase Security Rules

### Firestore Security Rules (`firestore.rules`)

```javascript
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    
    // Users Collection - Read/Write own data only
    match /users/{userId} {
      allow read, write: if request.auth.uid == userId 
                         && request.auth.uid != null;
    }
    
    // Cycles Collection - Users can only access their own cycles
    match /cycles/{cycleId} {
      allow read: if request.auth.uid == resource.data.userId;
      allow write: if request.auth.uid == request.resource.data.userId 
                   && request.auth.uid != null;
    }
    
    // Symptoms Collection - Users can only access their own symptoms
    match /symptoms/{symptomId} {
      allow read: if request.auth.uid == resource.data.userId;
      allow write: if request.auth.uid == request.resource.data.userId 
                   && request.auth.uid != null;
    }
    
    // Articles Collection - Public read-only
    match /articles/{articleId} {
      allow read: if true;
      allow write: if false; // Admins only through Firebase Console
    }
    
    // Sync Queue - Users can only access their own queue
    match /syncQueue/{queueId} {
      allow read, write: if request.auth.uid == resource.data.userId 
                         || request.auth.uid == request.resource.data.userId;
    }
    
    // Chat Messages - Users can only access their own messages
    match /chatMessages/{messageId} {
      allow read: if request.auth.uid == resource.data.userId 
                  || request.auth.uid == resource.data.healthWorkerId;
      allow write: if request.auth.uid == request.resource.data.userId 
                   || request.auth.uid == request.resource.data.healthWorkerId;
    }
  }
}
```

### Firestore Indexes (`firestore.indexes.json`)

```json
{
  "indexes": [
    {
      "collectionGroup": "cycles",
      "queryScope": "COLLECTION",
      "fields": [
        { "fieldPath": "userId", "order": "ASCENDING" },
        { "fieldPath": "periodStart", "order": "DESCENDING" }
      ]
    },
    {
      "collectionGroup": "symptoms",
      "queryScope": "COLLECTION",
      "fields": [
        { "fieldPath": "userId", "order": "ASCENDING" },
        { "fieldPath": "date", "order": "DESCENDING" }
      ]
    },
    {
      "collectionGroup": "articles",
      "queryScope": "COLLECTION",
      "fields": [
        { "fieldPath": "category", "order": "ASCENDING" },
        { "fieldPath": "publishedAt", "order": "DESCENDING" }
      ]
    }
  ]
}
```

---

## 🗓️ Development Timeline

### Phase 0: Planning & Design (Week 0)
| Task | Duration | Owner |
|------|----------|-------|
| Finalize requirements | 2 days | Team Lead |
| Create design mockups | 3 days | UI/UX Designer |
| Set up development environment | 1 day | Developer |
| Write technical specifications | 2 days | Developer |

### Phase 1: Foundation (Week 1-2)
| Task | Duration | Owner |
|------|----------|-------|
| Initialize React + Firebase | 2 days | Developer |
| Implement Authentication | 3 days | Developer |
| Set up routing & navigation | 2 days | Developer |
| Build splash & onboarding | 3 days | UI/UX Designer |
| Create design system | 3 days | UI/UX Designer |

### Phase 2: Core Features (Week 3-5)
| Task | Duration | Owner |
|------|----------|-------|
| Build Home Dashboard | 3 days | Frontend Dev |
| Build Tracker Calendar | 4 days | Frontend Dev |
| Period prediction logic | 3 days | Frontend Dev |
| Symptom logging form | 2 days | Frontend Dev |
| Offline storage (IndexedDB) | 3 days | Frontend Dev |
| Connect to Firestore | 3 days | Developer |

### Phase 3: Content & Features (Week 6-7)
| Task | Duration | Owner |
|------|----------|-------|
| Health Library UI | 2 days | Frontend Dev |
| Write 20 health articles | 4 days | Content Creator |
| Translate to Luganda | 3 days | Content Creator |
| Implement Settings | 2 days | Frontend Dev |
| Profile & Privacy screens | 2 days | Frontend Dev |
| Push notifications | 2 days | Developer |

### Phase 4: Polish & Testing (Week 8)
| Task | Duration | Owner |
|------|----------|-------|
| Empty states & error handling | 2 days | All |
| Performance optimization | 2 days | Developer |
| PWA configuration | 1 day | Developer |
| Testing (Offline, Sync, UI) | 3 days | QA |
| User testing (5-10 women) | 2 days | QA |

### Phase 5: Launch (Week 9)
| Task | Duration | Owner |
|------|----------|-------|
| Fix critical bugs | 2 days | All |
| Final polish | 2 days | UI/UX Designer |
| Deploy to Firebase Hosting | 1 day | Developer |
| Submit to app stores (PWA) | 2 days | Developer |
| Launch & marketing | Ongoing | Team Lead |

**Total Time: ~9 Weeks**

---

## 🚀 Installation & Setup

### Prerequisites
- Node.js 18+ and npm/yarn
- Git
- Firebase Account (free)
- Code Editor (VS Code recommended)

### Step 1: Clone Repository
```bash
git clone https://github.com/your-username/mamacycle-ug.git
cd mamacycle-ug
```

### Step 2: Install Dependencies
```bash
npm install
```

### Step 3: Set Up Firebase
1. Go to [Firebase Console](https://console.firebase.google.com/)
2. Create a new project: "MamaCycle UG"
3. Enable Authentication (Google + Email/Password)
4. Create Firestore Database (start in test mode, then secure)
5. Enable Firebase Hosting
6. Register your web app
7. Copy Firebase configuration

### Step 4: Environment Variables
Create `.env` file in root:
```env
VITE_FIREBASE_API_KEY=your_api_key
VITE_FIREBASE_AUTH_DOMAIN=your_project.firebaseapp.com
VITE_FIREBASE_PROJECT_ID=your_project_id
VITE_FIREBASE_STORAGE_BUCKET=your_project.appspot.com
VITE_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
VITE_FIREBASE_APP_ID=your_app_id
VITE_FIREBASE_MEASUREMENT_ID=your_measurement_id
```

### Step 5: Run Development Server
```bash
npm run dev
```
App will be available at: `http://localhost:5173`

### Step 6: Build for Production
```bash
npm run build
```

### Step 7: Deploy to Firebase
```bash
# Install Firebase CLI
npm install -g firebase-tools

# Login
firebase login

# Initialize Firebase (if not done)
firebase init hosting

# Deploy
firebase deploy --only hosting
```

---

## 🚢 Deployment

### Firebase Hosting
```bash
# Deploy to live channel
firebase deploy --only hosting

# Deploy to preview channel (staging)
firebase hosting:channel:deploy preview
```

### Custom Domain Setup
1. Buy domain (e.g., `mamacycle.ug` or `mamakit.ug`)
2. In Firebase Console > Hosting > Add Custom Domain
3. Add DNS records as instructed
4. Wait for SSL propagation (5-30 minutes)

### CI/CD Pipeline (GitHub Actions)
```yaml
name: Deploy to Firebase
on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Setup Node
        uses: actions/setup-node@v3
        with:
          node-version: '18'
      - name: Install Dependencies
        run: npm ci
      - name: Build
        run: npm run build
      - name: Deploy to Firebase
        uses: FirebaseExtended/action-hosting-deploy@v0
        with:
          repoToken: '${{ secrets.GITHUB_TOKEN }}'
          firebaseServiceAccount: '${{ secrets.FIREBASE_SERVICE_ACCOUNT }}'
          channelId: live
          projectId: mamacycle-ug
```

---

## 🧪 Testing

### Manual Testing Checklist
- [ ] Authentication (Google + Email)
- [ ] Language switching (English ↔ Luganda)
- [ ] Period tracking & predictions
- [ ] Symptom logging
- [ ] Calendar view with color coding
- [ ] Offline mode (turn off internet)
- [ ] Sync when internet returns
- [ ] Article reading & bookmarking
- [ ] Notifications
- [ ] Settings persistence
- [ ] Dark/light theme
- [ ] Responsive design (all screen sizes)

### Performance Testing
- [ ] Lighthouse Score > 90 (Performance, Accessibility, SEO)
- [ ] First Contentful Paint < 1.8s
- [ ] Time to Interactive < 3.8s
- [ ] Bundle size < 200KB (first load)

### User Testing
```markdown
Test with 5-10 women from target demographic:
1. Ask them to complete onboarding
2. Log a period start date
3. View predictions
4. Log symptoms for 3 days
5. Read 2 articles
6. Switch language to Luganda
7. Turn off internet, continue using
8. Provide feedback
```

---

## 🤝 Contributing

### How to Contribute
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Code Standards
- Follow ESLint configuration
- Write meaningful commit messages
- Test before submitting PR
- Update documentation

### Areas We Need Help
- Content writing (health articles in English & Luganda)
- Translation (Luganda)
- Medical review (health professionals)
- UI/UX improvements
- Bug fixes
- Testing

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

### Third-Party Licenses
- React: MIT
- Firebase: Apache 2.0
- Tailwind CSS: MIT
- All other dependencies: See package.json

---

## 📞 Contact & Support

### Team
- **Project Lead:** [Your Name] - [your.email@example.com]
- **Frontend Developer:** [Name]
- **UI/UX Designer:** [Name]
- **Content Manager:** [Name]

### Links
- **Website:** [mamacycle.ug](https://mamacycle.ug)
- **GitHub:** [github.com/your-username/mamacycle-ug](https://github.com/your-username/mamacycle-ug)
- **Twitter:** [@MamaCycleUG](https://twitter.com/MamaCycleUG)
- **Email:** support@mamacycle.ug

### Emergency Contact
If you need immediate medical assistance:
- **Uganda National Health Hotline:** 0800 100 066
- **Emergency Services:** 999

---

## 🙏 Acknowledgments

- **Ministry of Health Uganda** for health guidelines
- **WHO** for reproductive health standards
- **UNFPA Uganda** for family planning resources
- **All beta testers** for their invaluable feedback
- **The women of Uganda** for inspiring this project

---

## 📊 Key Metrics

### Current Status
| Metric | Status |
|--------|--------|
| **Lines of Code** | 15,000+ |
| **Total Screens** | 16 |
| **Health Articles** | 20+ (planned) |
| **Supported Languages** | 2 |
| **Team Size** | 4 |
| **Development Stage** | Planning |

### Success Metrics (Target)
| Metric | 6 Months | 1 Year |
|--------|----------|--------|
| **Users** | 5,000 | 25,000 |
| **Daily Active Users** | 500 | 5,000 |
| **Sessions per User** | 3/day | 5/day |
| **User Retention** | 40% | 60% |

---

## 🌟 Roadmap

### Q3 2025 (Launch)
- ✅ MVP launch
- ✅ 1,000 users

### Q4 2025
- 🔄 User feedback collection
- 🔄 Bug fixes & improvements
- 🔄 Add 10 more articles

### Q1 2026
- 📊 Analytics dashboard
- 💬 Health worker chat (beta)
- 📈 Advanced analytics

### Q2 2026
- 🤝 Partnerships with clinics
- 🌐 Expand to Kenya & Tanzania
- 📱 Android/iOS apps (React Native)

---

## 📝 Changelog

### v1.0.0 (Planned Launch - September 2025)
- Initial release
- Period tracking
- Symptom logging
- Health library
- Offline mode
- English & Luganda

### v1.1.0 (Planned - Q4 2025)
- Fertility predictions
- Cycle analytics
- 20+ articles
- Performance improvements

---

## 🔐 Privacy & Security

### Data Collection
- Only collect what's necessary for health tracking
- Never sell user data
- Anonymize analytics data

### Data Storage
- User data stored on device (IndexedDB)
- Optional cloud sync to Firestore
- End-to-end encryption for health worker chat

### User Rights
- Access your data anytime
- Delete your data permanently
- Export your data (coming soon)
- Opt out of analytics

---

## 📚 Resources

### Health Content Sources
- [WHO Reproductive Health](https://www.who.int/health-topics/reproductive-health)
- [UNFPA Uganda](https://uganda.unfpa.org)
- [Ministry of Health Uganda](https://www.health.go.ug)
- [Mayo Clinic](https://www.mayoclinic.org)

### Development Resources
- [Firebase Documentation](https://firebase.google.com/docs)
- [React Documentation](https://react.dev)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [PWA Guide](https://web.dev/progressive-web-apps/)

---

**Built with ❤️ for the women of Uganda**

---

*Last Updated: July 2025*
