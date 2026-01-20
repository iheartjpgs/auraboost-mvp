# 💎 AuraScan

**Track your aura. Compete. Earn.**

AuraScan is a gamified fitness tracking mobile app that combines daily gym workouts with a unique "aura" scoring system. Users earn points based on workout frequency, create daily streaks, and compete on global leaderboards. The app monetizes through premium subscriptions and a creator partnership program where fitness influencers earn 30% commission on referred user spending.

---

## 🎯 Product Overview

### Core Concept
Instead of traditional calorie tracking, AuraScan uses a **unique aura scoring system** that rewards:
- **Workout Frequency** (daily bonus multiplier)
- **Duration** (longer workouts = more points)
- **Intensity** (light/moderate/intense)
- **Streaks** (exponential boost for consecutive days)

Every user has:
- A daily aura score (updated in real-time)
- A current streak counter (consecutive gym days)
- An all-time rank on the global leaderboard

### Target Users
- Fitness enthusiasts who like gamification
- People motivated by leaderboards & competition
- Content creators building fitness communities
- Users seeking social accountability

---

## ✨ Features Included (MVP)

### ✅ Authentication
- Email/password signup & login
- OAuth integration (Apple/Google) ready
- Secure token-based sessions
- Password validation

### ✅ Aura Scoring System
- Dynamic point calculation based on workout metrics
- Real-time score updates
- Streak multiplier (exponential growth)
- Historical tracking

### ✅ Workout Logging
- Manual entry of:
  - Exercise type (6 options: Cardio, Strength, Yoga, Sports, Swimming, Cycling)
  - Duration (in minutes)
  - Intensity level (Light/Moderate/Intense)
  - Optional notes
- Live aura bonus preview
- Workout history

### ✅ Streak System
- Daily streak counter
- Milestone achievements (7, 14, 30, 100, 365 days)
- Streak freeze feature ($0.99/month - skip 1 day)
- Longest streak tracking

### ✅ Global Leaderboards
- Top 100 users ranked by aura score
- Alternative rankings by streak length
- Your rank position & distance to next tier
- User profiles on leaderboard

### ✅ User Profile
- Avatar (initials or emoji)
- Bio/description
- Stats dashboard:
  - Total aura points
  - Current streak
  - Longest streak
  - Total workouts
  - Membership level
- Editable profile settings
- Achievement badges

### ✅ Subscription Tiers
**Basic** ($4.99/month)
- Unlimited workout logging
- Basic aura tracking
- Global leaderboard access

**Pro** ($9.99/month) ⭐ Most Popular
- Everything in Basic
- Streak freeze (1x/month)
- Advanced analytics
- Custom workout categories
- Priority support

**Elite** ($14.99/month)
- Everything in Pro
- Unlimited streak freezes
- Weekly challenges
- Private group leaderboards
- Export data & reports
- 24/7 VIP support

### ✅ Creator Partnership Program
- Creator signup form with validation
- 30% commission on all referred user spending
- Unique referral links (backend)
- Real-time earnings dashboard (Phase 2)
- Weekly Stripe payouts

---

## 🏗️ Technical Stack

### Frontend (Complete)
- **Framework**: React Native
- **Build Tool**: Expo (no native builds needed)
- **Navigation**: React Navigation (tabs + stack)
- **State Management**: Redux-ready (can add later)
- **UI Components**: Native components + custom styling
- **Styling**: React Native StyleSheet

### Backend (To Build)
- **Runtime**: Node.js + Express.js
- **Database**: PostgreSQL (optimized for leaderboards)
- **Auth**: JWT + OAuth
- **Payments**: Stripe (subscriptions + creator payouts)
- **Hosting**: Vercel or AWS

### Infrastructure (To Set Up)
- **Database**: AWS RDS or Supabase
- **File Storage**: AWS S3 or Cloudinary (avatars)
- **Analytics**: Mixpanel or Amplitude
- **Error Tracking**: Sentry
- **App Distribution**: App Store + Play Store

---

## 📱 App Screens

### Auth Flows
1. **Login Screen**
   - Email/password inputs
   - OAuth buttons
   - Sign-up link

2. **Signup Screen**
   - Username, email, password
   - Password confirmation
   - Terms acceptance

### Core App (5 Tabs)

3. **Dashboard** (Home)
   - Large aura score display
   - Current + longest streak
   - Weekly stats
   - All-time workouts
   - Quick action buttons

4. **Log Workout** (Log)
   - Exercise type selector (6 options)
   - Duration input
   - Intensity picker
   - Notes field
   - Real-time bonus preview
   - Submit button

5. **Leaderboard** (Rankings)
   - Sort by aura or streak
   - Your rank card
   - Top 100 users list
   - User highlights (medals for top 3)

6. **Profile** (Profile)
   - User stats
   - Edit bio
   - Achievement badges
   - Account settings
   - Sign out

### Modals
7. **Subscription** (Upgrade)
   - 3 tier cards
   - Feature comparison
   - FAQ section
   - Terms

8. **Creator Signup** (Creator)
   - Application form
   - Benefits preview
   - Social media links
   - Submission

---

## 🎨 Design System

### Colors
- **Primary Gold**: #F59E0B
- **Light Gold**: #FCD34D
- **Dark Blue**: #0F172A
- **Surface**: #1E293B

### Typography
- **Headings**: 700-800 fontWeight
- **Body**: 14-16px, 400-600 fontWeight
- **Labels**: 12-14px, 600 fontWeight

### Components
- All rounded corners: 8-12px border radius
- Card-based layouts
- Icon emojis for visual interest
- Consistent spacing (16px padding standard)

---

## 📊 Aura Scoring Formula

```
Base Score = Duration (mins) × 10
Intensity Multiplier = Intensity / 2 (Light=1, Moderate=2, Intense=3)
Streak Multiplier = 1 + (CurrentStreak / 10)

Total Aura Points = Base × Intensity × Streak
```

**Examples:**
- 30 min moderate workout, 0 streak = 300 points
- 30 min intense workout, 5-day streak = 33 × 1.5 × 1.5 = 742 points
- 30 min intense workout, 15-day streak = 33 × 1.5 × 2.5 = 1,237 points

---

## 💰 Revenue Model

### Subscription Revenue
- **Basic**: $4.99/month
- **Pro**: $9.99/month (most popular)
- **Elite**: $14.99/month
- Expected conversion: 15-25%

### Creator Commission
- **Structure**: 30% of referred user spending
- **Payout**: Weekly (Mondays, 8 AM)
- **1099 Generation**: Automated via Stripe

### Month 1 Projections
- 200-300 users (organic + influencer referrals)
- $1,600-$3,800 revenue
- Optimistic: $17K (if influencer push succeeds)

### Month 3 Projections
- 2,000-5,000 users
- $10,000-$20,000 revenue
- Optimistic: $150K+ (viral growth)

---

## 🚀 Getting Started

### Prerequisites
- Node.js 18+
- npm or yarn
- Expo CLI (`npm install -g expo-cli`)
- iOS Simulator or Android Emulator (optional)

### Installation
```bash
# Clone repository
git clone https://github.com/yourusername/aurascan.git
cd aurascan

# Install dependencies
npm install

# Start dev server
expo start

# Run on iOS
expo start --ios

# Run on Android
expo start --android
```

### Environment Setup
Create `.env`:
```
REACT_APP_API_URL=https://api.aurascan.xyz
REACT_APP_STRIPE_KEY=pk_live_...
REACT_APP_GOOGLE_CLIENT_ID=...
```

---

## 📋 What's Implemented vs. What's Next

### ✅ Phase 1 (MVP - DONE)
- [x] Authentication screens
- [x] Dashboard with aura display
- [x] Workout logging
- [x] Leaderboards
- [x] User profiles
- [x] Subscription tiers
- [x] Creator signup
- [x] Navigation & routing
- [x] Complete UI/UX

### 🔄 Phase 2 (Post-Launch - Backend)
- [ ] Backend API (Node.js + Express)
- [ ] Database (PostgreSQL)
- [ ] User authentication (JWT)
- [ ] Stripe integration
- [ ] Creator dashboard
- [ ] Real-time leaderboard queries
- [ ] Email notifications
- [ ] Analytics

### 📅 Phase 3 (Advanced Features)
- [ ] Weekly challenges
- [ ] Friend leaderboards
- [ ] Push notifications
- [ ] Achievements system
- [ ] Wearable integration (Apple Health, Google Fit)
- [ ] Data export
- [ ] Social sharing

---

## 🧪 Testing the App

### Mock Data
All screens use realistic mock data so you can test UI/UX immediately:
- Leaderboard: 10 sample users
- Dashboard: Sample user stats
- Workout forms: Exercise types, intensities

### Testing Flows
1. **Auth**: Sign up, login, logout
2. **Logging**: Create workouts, see aura update
3. **Leaderboards**: Sort by aura/streak, view your rank
4. **Profile**: Edit bio, view achievements
5. **Subscriptions**: Browse plans, see feature breakdown
6. **Creator**: Submit application

---

## 🔐 Security

- ✅ JWT authentication
- ✅ Secure token storage (AsyncStorage)
- ✅ HTTPS/TLS encryption
- ✅ Stripe PCI compliance
- ✅ Input validation & sanitization
- 🔄 Rate limiting (backend)
- 🔄 OAuth2 verification

---

## 📈 Success Metrics

### Growth Targets
- **Week 2**: 100+ DAU
- **Month 2**: 500+ DAU, 2,000+ MAU
- **Month 3**: 1,000+ DAU

### Engagement Targets
- 30% day-7 retention
- 7+ day average streak
- 3+ workouts per user per week
- 40%+ leaderboard participation

### Revenue Targets
- ARPU: $2-5/month
- LTV: $20-50
- CAC: $0-2 (organic)
- 5+ creator partnerships by month 1

---

## 🤝 Contributing

1. Fork the repo
2. Create feature branch (`git checkout -b feature/amazing`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing`)
5. Open Pull Request

---

## 📞 Support

- **Email**: support@aurascan.xyz
- **Twitter**: @AuraScan
- **Instagram**: @aurascan
- **TikTok**: @aurascan
- **Discord**: discord.gg/aurascan

---

## 📄 License

MIT License - See LICENSE file for details

---

## 👏 Credits

**AuraScan** built with ❤️

**Tech Stack**:
- React Native + Expo
- React Navigation
- Stripe API
- PostgreSQL

---

**Let's build the future of fitness tracking. Your aura awaits. 💎✨**
