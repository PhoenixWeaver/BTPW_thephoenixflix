# 🐦 ::: PhoenixFlix - Multi-Purpose Movies & Christian Streaming Platform :::  🔥

🎬 PhoenixFlix - Multi-Purpose Movies & Christian Streaming Platform & CEXs Concurrencies 

> **🚀 Ready to Deploy V2?** Start here: **[START_HERE.md](START_HERE.md)** - Quick deployment guide
> 
> **📚 Deployment Guides:** Comprehensive deployment documentation available in project documentation
> 
> **⭐ Recommended:** Fresh Repository deployment (Option A) for clean V2

## 🌟 **Vision & Inspiration**

**PhoenixFlix** represents a groundbreaking fusion of entertainment and spirituality - a platform where families can enjoy both secular entertainment and uplifting Christian content under one roof. Born from the vision of creating a platform where faith and entertainment coexist harmoniously.

### **🎯 Core Mission**
To provide a **family-friendly streaming experience** that combines:
- **Entertainment**: Access to quality movies and content
- **Spirituality**: Uplifting Christian content including Bible videos, Christian songs, and LDS content
- **Financial Tools**: Real-time currency exchange, cryptocurrency, and stock market data
- **Community**: A platform where faith and entertainment coexist harmoniously

### **💡 The Inspiration**
In a world where streaming platforms often compromise family values, PhoenixFlix was created to offer an alternative - a platform where parents can confidently let their children explore content, knowing that both entertainment and spiritual nourishment are available in equal measure.

## 🏆 **Scope & Work Accomplished**

### **🎯 Project Scope**
This is a **full-stack, production-ready application** that demonstrates mastery of:
- **Modern Web Architecture**: Clean Architecture with Repository Pattern
- **Dual Database Design**: Innovative approach to separate movies and Christian content
- **Advanced Authentication**: WebAuthn/Passkeys + JWT security
- **Cross-Platform Integration**: TMDB + YouTube APIs
- **Enterprise-Level Security**: Admin systems, middleware, validation
- **Financial Data Integration**: Real-time CEXs (Currency, Crypto, Stocks) with advanced Go concurrency

### **💪 Technical Achievements**

#### **🏗️ Architecture Excellence**
- ✅ **Clean Architecture Implementation**: Repository Pattern with dependency injection
- ✅ **Dual Database System**: Separate PostgreSQL instances for movies and Christian content
- ✅ **Cross-Database User Management**: Unified user experience across content types
- ✅ **Middleware Pattern**: Authentication, admin, and logging middleware
- ✅ **Handler Pattern**: Clean HTTP request processing

#### **🔐 Security & Authentication**
- ✅ **Modern Passwordless Auth**: WebAuthn/Passkeys implementation
- ✅ **JWT Token System**: Secure session management with 72-hour expiration
- ✅ **Email Verification**: Token-based email confirmation with 24-hour expiry
- ✅ **Password Reset**: Secure password reset via email tokens with 1-hour expiry
- ✅ **SMTP Integration**: Production-grade email delivery via Vercel CDN
- ✅ **Admin Role System**: Complete admin middleware with database-level permissions
- ✅ **SQL Injection Prevention**: Parameterized queries throughout
- ✅ **Input Validation**: Comprehensive data validation and sanitization
- ✅ **Rate Limiting**: Email bombing and brute force protection
- ✅ **Race Condition Prevention**: Optimistic locking with version control

#### **📊 Database Engineering**
- ✅ **Dual PostgreSQL Setup**: Movies database (Neon) + Christian content database (Aiven)
- ✅ **Primary/Backup Database Architecture**: Dual-write pattern with automatic read fallback
- ✅ **Automatic Read Fallback**: All read operations automatically fallback to BACKUP if PRIMARY fails
- ✅ **Health Check System**: Periodic health checks (every 4 minutes) to keep BACKUP databases warm
- ✅ **Optimistic Locking**: Version-based concurrency control for race condition prevention
- ✅ **Cross-Database Relationships**: Bridge tables for unified user collections
- ✅ **Data Import Systems**: Automated TMDB and YouTube content integration
- ✅ **User Management**: Complete CRUD operations with soft deletes
- ✅ **Guestbook System**: Full moderation and approval workflow
- ✅ **Transaction Safety**: ACID-compliant operations with rollback support

#### **🎨 Frontend Development**
- ✅ **Vanilla JavaScript SPA**: Modern single-page application
- ✅ **Server-Side Rendering**: SEO-friendly movie detail pages
- ✅ **Responsive Design**: Mobile-first approach
- ✅ **Progressive Web App**: PWA capabilities with service workers
- ✅ **Financial Data**: Real-time Currency, Crypto, and Stock (CEXs) data visualization.
- ✅ **Component Architecture**: Modular JavaScript components

#### **🔌 API Integration**
- ✅ **TMDB Integration**: Complete movie database with 70,000+ entries
- ✅ **YouTube API**: Christian content including Bible videos, Christian songs, LDS content
- ✅ **Financial APIs**: CoinGecko, ExchangeRate-API, Massive.com (Polygon) for currency, crypto, stocks
- ✅ **RESTful API Design**: Clean, consistent endpoint structure
- ✅ **Error Handling**: Comprehensive error responses and logging

#### **🛠️ DevOps & Deployment**
- ✅ **Go Module Management**: Clean dependency management
- ✅ **Environment Configuration**: Secure environment variable handling
- ✅ **Logging System**: Custom structured logging for movies and LDS
- ✅ **Build System**: Single binary deployment ready
- ✅ **Git Integration**: Version control with comprehensive .gitignore
- ✅ **Cloud Deployment**: Render (Backend) + Vercel (Frontend/CDN)
- ✅ **Database Hosting**: Neon + Aiven PostgreSQL with auto-scaling
- ✅ **CI/CD Pipeline**: Automatic deployment on git push

#### **🎛️ Admin Features & Content Management**
- ✅ **Admin Delete Feature**: Secure content deletion with audit trail
  - Soft delete for movies and LDS content (preserves data)
  - Complete deletion tracking in `deleted_content` table
  - Admin-only access with JWT authentication
  - Optional deletion reason logging
  - ✅ **Restore Functionality**: Restore deleted movies and LDS content via deletion tracking page
    - Restore buttons on `/admin/deletion-tracking` page
    - Confirmation dialog before restoration
    - Graceful handling of missing `is_active` column in LDS database
    - Helpful error messages with migration instructions
    - Auto-refresh after restore
    - Content appears in listings again
  - ✅ **Deletion Tracking Admin Page**: View deletion history with filtering and pagination
    - Admin page at `/admin/deletion-tracking`
    - Filter by content type (movie/LDS) and admin email
    - Sort by date, title, or admin
    - Paginated results with statistics
    - Accessible from GuestbookAdminPage via "View Deletion Tracking" button
- ✅ **Weekly Featured Content Refresh**: Admin-controlled content curation
  - Refresh weekly top movies by popularity or score
  - Refresh weekly LDS content by views, likes, or random shuffle
  - Fast refresh (existing data) or full refresh (TMDB update)
  - `weekly_top_movies` and `weekly_top_lds` cache tables
  - Admin dashboard buttons for easy refresh
  - Strict content filtering (LDS-only for LDS Features)
- ✅ **Dynamic Era-Based Filtering & Admin Controls**: 🧬
  - **Independent Homepage Filters**: Separate era-filtering dropdowns (1980s to present) for "Top Movies" and "Random Movies" sections.
  - **Admin Default Eras**: New admin panel settings to control the default era displayed for both "Top Movies" and "Random Movies" for all users.
  - **Era-Aware Search**: Search queries now respect the selected era from the "Top Movies" filter, allowing for more precise content discovery.
  - **New Admin Endpoints**: Added APIs for getting and setting the default eras.
  - **Robust Fallback**: The "Top Movies" section now gracefully falls back to "All Time" if the weekly list is unavailable.
  - **New DB Table**: `admin_settings` table added to persist admin choices.

- ✅ **Christmas Theme Filtering & Admin Controls**: 🎄
  - **Themed Movie Filtering**: Christmas-themed movie filtering with keyword search in title and overview
  - **Admin Default Theme**: Admins can set "christmas" as the global default theme for both Top Movies and Random Movies
  - **Dual Section Support**: Christmas theme available for both homepage sections
  - **Public Theme API**: Frontend can check current default theme via public endpoint
  - **Consistent Pattern**: Follows the same implementation pattern as era-based filtering

![Christmas Edition](PhoenixFlix_OutputSamples/Christmas/ChristmasEdition.png)
*Christmas Edition feature with admin controls for Top Movies and Random Movies sections*

### **📈 Project Statistics**
- **📁 Files**: 50+ Go files, 20+ JavaScript components
- **🗄️ Databases**: 2 PostgreSQL instances with 15+ tables
- **🔗 API Endpoints**: 25+ RESTful endpoints
- **🔐 Security Features**: JWT + WebAuthn + Admin middleware
- **📊 Content**: 70,000+ movies + Christian content (Bible videos, Christian songs, LDS content)
- **👥 User Features**: Registration, authentication, favorites, guestbook

### **🎖️ Technical Innovation**
This project showcases several **innovative approaches**:
1. **Dual Database Architecture**: Unique separation of secular movies and Christian content (Neon + Aiven)
2. **Cross-Database User Collections**: Users can favorite content from both databases
3. **Modern Authentication**: WebAuthn implementation for passwordless login
4. **Hybrid Rendering**: SSR for SEO + SPA for modern UX
5. **Admin Moderation System**: Complete content management workflow
6. **Optimistic Locking**: Race condition prevention with version-based concurrency control
7. **Advanced Account Management**: Comprehensive email verification and password reset system
8. **Distributed Infrastructure**: Render (Backend) + Vercel (Frontend/Email CDN) architecture
9. **Go Routines**: Efficient concurrent request handling with safe database operations
10. **Automatic Read Fallback & Recovery**: Intelligent failover system with automatic database fallback and health checks
11. **CEXs Module**: Real-time financial data with advanced Go concurrency patterns (channels, mutexes, worker pools)

## ✨ Features

### 🎬 Movies Section
- **Movie Database**: Integration with TMDB (The Movie Database)
- **Search & Filtering**: Advanced movie search with genre filtering
- **Language Support**: Multi-language content (English, Japanese, Spanish, Italian, French, Korean, German, Portuguese, Vietnamese, Arabic, Greek, Thai, Russian, Chinese)
- **User Collections**: Favorites and watchlist functionality
- **Server-Side Rendering**: SEO-friendly movie detail pages

### ⛪ Christian Content Section
- **Bible Videos**: Scripture-based video content and teachings
- **Christian Songs**: Uplifting Christian music and hymns
- **LDS Content**: Conference talks and LDS-specific content
- **YouTube Integration**: Seamless video playback for all Christian content
- **Spiritual Rating**: 1-5 scale rating system
- **Family-Friendly**: Content filtering and age-appropriate content
- **Featured Content**: Daily highlights and recommendations

### 💱 CEXs Section (Currency Exchange & Market Data)
- **Currency Rates**: Real-time fiat exchange rates (USD, EUR, JPY, VND, etc.)
- **Cryptocurrencies**: Top crypto prices with multi-currency support
- **Stocks**: Stock market data from major exchanges
- **Concurrency Demo**: Educational showcase of Go concurrency patterns
- **Rate Limit Modal**: Friendly reminder for API usage

### 👤 User Management
- **Modern Authentication**: WebAuthn/Passkey (passwordless)
- **JWT Tokens**: Secure session management with 72-hour validity
- **Email Verification**: Token-based email confirmation with 24-hour expiry
- **Password Reset**: Secure password reset via email tokens with 1-hour expiry
- **Cross-Database Collections**: Users can favorite both movies and Christian content
- **Admin System**: Full admin panel with moderation capabilities
- **Guestbook**: Community interaction features

## 🏗️ Technical Architecture

### **Backend**
- **Language**: Go 1.25+
- **Architecture**: Clean Architecture with Repository Pattern
- **Database**: Dual PostgreSQL (NEON + AIVEN) - Movies + Christian Content
- **Hosting**: Render (Backend API)
- **Authentication**: JWT + WebAuthn/Passkeys
- **APIs**: TMDB, YouTube, CoinGecko, ExchangeRate-API, Massive.com (Polygon)
- **Concurrency**: Go Routines with Optimistic Locking for race condition prevention

### **Frontend**
- **Technology**: Vanilla JavaScript SPA
- **Hosting**: Vercel.com
- **Framework**: Vanilla JavaScript SPA
- **CDN**: Global edge network
- **SSL**: Automatic HTTPS

### **Database Providers**
- **Neon PostgreSQL**: Modern serverless PostgreSQL
  - Auto-scaling
  - Branch-based development
  - Built-in connection pooling
  
- **Aiven PostgreSQL**: Enterprise-grade database hosting
  - High availability
  - Automatic backups
  - Cross-region replication

## ⚡ Quick Status Check

### **Your App Already Has Advanced Features:**
- ✅ **Automatic Database Failover** - App continues working if PRIMARY fails
- ✅ **Health Check System** - Keeps BACKUP databases warm (every 4 minutes)  
- ✅ **Crash-Proof Email** - 3-tier fallback system (never crashes)
- ✅ **Enterprise Security** - JWT + WebAuthn + Admin middleware
- ✅ **Production Ready** - Zero-downtime deployment capability

### **Current Architecture Status**
| Feature | Status | Benefit |
|---------|--------|----------|
| **Read Fallback** | ✅ **ACTIVE** | App works even if PRIMARY fails |
| **Health Checks** | ✅ **ACTIVE** | Prevents cold starts (~50ms vs ~500ms) |
| **Dual-Write** | ✅ **ACTIVE** | Data safety across databases |
| **Admin Features** | ✅ **ACTIVE** | Content management & moderation |
| **Email System** | ✅ **CRASH-PROOF** | Never fails (3-tier fallback) |

> **💡 The PhoenixFlix app is running the most advanced failover system possible for free-tier databases!**

## 🚀 Quick Start

> **📘 For Production Deployment:** See deployment documentation for complete deployment guide (Option A recommended)

> **⚡ Quick Environment Switch:** Use `.\switch-environment.ps1 local` or `.\switch-environment.ps1 production` to toggle configurations

### Prerequisites
- Go 1.25+
- PostgreSQL (Neon + Aiven recommended)
- TMDB API Key
- YouTube API Key (for Christian content)
- Air (for local development with live reload)

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/phoenixflix.git
cd phoenixflix
```

2. **Install dependencies**
```bash
go mod download
```

3. **Setup environment variables**
Create a `.env` file:
```env
# PRIMARY Databases (Required)
DATABASE_URL=postgres://username:password@host:port/database?sslmode=require
DATABASE_URL_LDS=postgres://username:password@host:port/database?sslmode=require

# BACKUP Databases (Optional - for automatic read fallback)
DATABASE_URL_BACKUP=postgres://username:password@host:port/database?sslmode=require
DATABASE_URL_LDS_BACKUP=postgres://username:password@host:port/database?sslmode=require

# API Keys
TMDB_API_KEY=your_tmdb_api_key
YOUTUBE_API_KEY=your_youtube_api_key

# Security
JWT_SECRET=your-super-secret-jwt-key-change-this-in-production
ENVIRONMENT=production

# SMTP / Email (for verification and password reset)
SMTP_HOST=smtp.example.com
SMTP_PORT=587
SMTP_USER=apikey_or_username
SMTP_PASS=your_smtp_password
SMTP_FROM=PhoenixFlix <no-reply@phoenixflix.app>
SMTP_TLS=true

# Server Port (defaults to 8080 if not set)
PORT=8080
```

4. **Run the application**
```bash
go run .
```

5. **Access the application**
Open your browser to `http://localhost:8080`

## 📁 Project Structure

```
PhoenixFlix/
├── BTPF.go                 # Main application entry point
├── data/                   # Repository layer (data access)
│   ├── interfaces.go       # Repository contracts
│   ├── movie_repository.go
│   ├── account_repository.go
│   ├── lds_repository.go
│   └── passkey_repository.go
├── handlers/               # HTTP handlers (business logic)
│   ├── movie_handlers.go
│   ├── account_handlers.go
│   ├── lds_handlers.go
│   └── passkey_handlers.go
├── models/                 # Data structures
│   ├── movie.go
│   ├── lds.go
│   ├── user.go
│   └── passkeyuser.go
├── public/                 # Frontend SPA
│   ├── index.html
│   ├── app.js
│   ├── styles.css
│   └── components/
├── logger/                  # Custom logging system
├── token/                   # JWT authentication
└── import/                  # Database import utilities
```

## 🔧 API Endpoints

### Movies
- `GET /api/movies/top` - Top movies
- `GET /api/movies/random` - Random movies
- `GET /api/movies/search/?q=query` - Search movies
- `GET /api/movies/language/{lang}` - Movies by language
- `GET /api/movies/{id}` - Movie details

### Christian Content
- `GET /api/LDS/top` - LDS content
- `GET /api/LDS/random` - Christian content
- `GET /api/LDS/search` - Christian database search
- `GET /api/LDS/{id}` - Christian content details
- `GET /api/LDS/bible-videos` - Bible video content
- `GET /api/LDS/christian-songs` - Christian music content

### CEXs (Currency, Crypto, Stocks)
- `GET /api/currency/rates?currencies=USD,EUR,GBP,JPY,VND,AUD` - Fiat currency rates
- `GET /api/crypto/multi-currency?per_page=50&currencies=usd,eur,jpy,vnd,aud` - Cryptocurrency prices
- `GET /api/stocks?symbols=AAPL,MSFT,GOOGL` - Stock market data

### Authentication
- `POST /api/account/register` - User registration
- `POST /api/account/authenticate` - User login
- `GET /api/account/confirm?token=...` - Email verification
- `POST /api/account/forgot-password` - Request password reset
- `POST /api/account/reset-password` - Reset password with token
- `POST /api/account/resend-verification` - Resend verification email (auth required)
- `POST /api/passkey/authentication-begin` - Passkey login start
- `POST /api/passkey/authentication-end` - Passkey login complete

### Admin (Protected)
- `GET /api/admin/guestbook` - All guestbook entries
- `DELETE /api/admin/guestbook/delete/{id}` - Delete entry
- `PUT /api/admin/guestbook/approve/{id}` - Approve entry
- `DELETE /api/admin/delete-movie/{id}` - Delete movie (admin only)
- `DELETE /api/admin/delete-lds/{id}` - Delete LDS content (admin only)
- `GET /api/admin/deleted-content` - Get deletion tracking records (admin only)
- `PUT /api/admin/restore-movie/{id}` - Restore deleted movie (admin only)
- `PUT /api/admin/restore-lds/{id}` - Restore deleted LDS content (admin only)

- `POST /api/admin/set-default-theme` - Set the global default theme (e.g., 'christmas')
- `GET /api/admin/default-theme` - Get the current default theme (public)

## 📧 Advanced Account Management

PhoenixFlix implements a comprehensive account management system with enterprise-level security features.

![Account Management Architecture](PhoenixFlix_OutputSamples/Structures/Architecture_AccountManagement.png)
*Figure 3: Complete account management architecture diagram*

### **Email Verification Flow**
1. **User Registration**: User registers with email and password
2. **Verification Token**: System creates a secure token (24-hour expiry)
3. **Email Sent**: Verification email sent via Vercel CDN with confirmation link
4. **Email Confirmation**: User clicks link to verify email address
5. **Account Activated**: User account is fully activated

### **Password Reset Flow**
1. **Reset Request**: User requests password reset via email
2. **Reset Token**: System creates a secure token (1-hour expiry)
3. **Reset Email**: Password reset email sent with secure link via Vercel CDN
4. **Password Update**: User sets new password via token
5. **Account Secured**: Password is updated and token invalidated

![Authentication Flow](PhoenixFlix_OutputSamples/Structures/Authentication_Flow.png)
*Figure 4: Full authentication flow including email verification and password reset*

### **Crash-Proof Email Infrastructure**
- **Multi-Provider Fallback**: SendGrid → Resend → SMTP automatic switching
- **Zero-Downtime Design**: App never crashes when email services expire
- **Professional Templates**: Consistent HTML design across all providers
- **Graceful Degradation**: Continues working even without email functionality
- **Production-Ready**: Handles SendGrid expiration (Dec 23, 2025) seamlessly
- **Error Handling**: Comprehensive error management with detailed logging

### **Security Features**
- **Token Expiry**: Verification tokens expire in 24 hours, reset tokens in 1 hour
- **Single Use**: Tokens are invalidated after use
- **Email Enumeration Protection**: Always returns success to prevent email discovery
- **Secure Generation**: Cryptographically secure random tokens (32+ bytes)
- **Database Storage**: Tokens stored securely with user association
- **Rate Limiting**: Protection against email bombing attacks
- **HTTPS Only**: All email links use secure HTTPS protocol

### **Additional Account Features**
- **Email Re-verification**: Users can request new verification emails
- **Account Recovery**: Multi-step password recovery process
- **Session Management**: JWT-based session with 72-hour validity
- **Device Tracking**: Last login timestamp for security monitoring
- **Soft Deletes**: Account data preserved for recovery

For detailed implementation, see account management architecture diagrams in `PhoenixFlix_OutputSamples/Structures/`

## 🚀 Deployment

### **Production Infrastructure**

PhoenixFlix uses a modern, distributed deployment architecture:

#### **Backend Deployment (Render)**
- **Platform**: Render.com
- **Service Type**: Web Service
- **Runtime**: Go 1.25+
- **Database**: PostgreSQL (Neon + Aiven)
- **Auto-Deploy**: Automatic deployment from main branch

**Deployment Steps:**
1. Push code to GitHub repository
2. Connect repository to Render
3. Configure environment variables (see `.env` template)
4. Set build command: `go build -o main .`
5. Set start command: `./main`
6. Deploy automatically

#### **Frontend Deployment (Vercel)**
- **Platform**: Vercel.com
- **Framework**: Vanilla JavaScript SPA
- **CDN**: Global edge network
- **Email Templates**: Served via Vercel CDN
- **SSL**: Automatic HTTPS

**Deployment Steps:**
1. Push frontend code to GitHub
2. Import project to Vercel
3. Configure build settings
4. Add environment variables
5. Deploy to production

#### **Database Providers**
- **Neon PostgreSQL**: Modern serverless PostgreSQL
  - Auto-scaling
  - Branch-based development
  - Built-in connection pooling
  
- **Aiven PostgreSQL**: Enterprise-grade database hosting
  - High availability
  - Automatic backups
  - Cross-region replication

### Docker
```dockerfile
FROM golang:1.25-alpine AS builder
WORKDIR /app
COPY . .
RUN go build -o main .

FROM alpine:latest
RUN apk --no-cache add ca-certificates
WORKDIR /root/
COPY --from=builder /app/main .
CMD ["./main"]
```

## 📊 Database Schema

### Users Table
- `id` (Primary Key)
- `name`, `email`, `password_hashed`
- `is_admin` (Boolean)
- `time_created`, `last_login`, `time_deleted`

### Movies Table
- `id`, `tmdb_id`, `title`, `release_year`
- `genres`, `overview`, `score`, `popularity`
- `poster_url`, `trailer_url`

### Christian Content Table
- `id`, `title`, `description`, `content_type`
- `youtube_id`, `speaker`, `conference_session`
- `spiritual_rating`, `family_friendly`
- **Content Types**: Bible videos, Christian songs, LDS content

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

### **🌟 Inspiration & Vision**
This project was born from a desire to create a **family-friendly alternative** to mainstream streaming platforms, where entertainment and spiritual growth can coexist. The vision of **"Netflix for the faithful"** drives every technical decision and feature implementation.

### **🤝 Technical Partners**
- **TMDB (The Movie Database)**: Providing comprehensive movie metadata and API access
- **YouTube API**: Enabling seamless integration of Christian content including Bible videos, Christian songs, and LDS content
- **CoinGecko**: Reliable cryptocurrency data provider
- **ExchangeRate-API**: Accurate fiat currency exchange rates
- **Massive.com (Polygon)**: Comprehensive stock market data
- **YouTube Content Creators**: For providing uplifting Christian content, Bible teachings, and inspirational music
- **Christian Community**: For inspiring content that strengthens faith and family values
- **Neon**: Modern serverless PostgreSQL with auto-scaling and branch-based development
- **Aiven**: Enterprise-grade PostgreSQL hosting with high availability and automatic backups
- **Render**: Reliable backend hosting platform with automatic deployment
- **Vercel**: Frontend and Email CDN hosting with global edge network
- **Go Community**: For excellent libraries and frameworks that made this possible

### **💡 Special Recognition**
- **WebAuthn Consortium**: For pioneering passwordless authentication standards
- **PostgreSQL Community**: For robust database technology
- **Open Source Contributors**: Whose work enables modern web development
- **Faith-Based Communities**: For inspiring the need for wholesome entertainment platforms

## 📚 Feature Documentation & Visual Guides

PhoenixFlix includes comprehensive documentation and visual demonstrations of all major features. Below are the key features with their implementation details and visual demonstrations.

### **🏗️ Major Features**

#### **1. Dual Database Architecture** 📊

**Features:**
- Primary/Backup database synchronization
- Dual-write helper pattern
- Graceful degradation when backup unavailable
- Cross-database fallback mechanism

**Visual Demonstrations:**

![Dual Write Pattern](PhoenixFlix_OutputSamples/DualDatabases/Dual_write.png)
*Dual-write pattern: Writes go to both primary and backup databases simultaneously*

![Read from Primary](PhoenixFlix_OutputSamples/DualDatabases/Read_Prime.png)
*Read operations use primary database only for optimal performance*

![Cross-Database Fallback](PhoenixFlix_OutputSamples/DualDatabases/Cross_db_Fallback.png)
*Cross-database fallback mechanism when primary is unavailable*

#### **2. Admin Content Management** 🗑️

**Features:**
- Soft delete for movies and LDS content
- Deletion tracking with audit trail
- Admin-only deletion with JWT authentication
- Optional deletion reason logging
- Restore functionality for deleted content
- Deletion tracking admin page with filtering

**Visual Demonstrations:**

![Admin Soft Delete](PhoenixFlix_OutputSamples/AdminRights/Admin_SoftDelete.png)
*Admin soft delete interface with deletion reason*

![Deletion Tracker](PhoenixFlix_OutputSamples/AdminRights/Deletion_Tracker.png)
*Deletion tracking admin page showing all deleted content with filtering*

![Content Restoration](PhoenixFlix_OutputSamples/AdminRights/Content_Restoration_by_Admin.png)
*Admin content restoration interface*

![Content Refresh](PhoenixFlix_OutputSamples/AdminRights/Content_Refresh_Admin.png)
*Weekly content refresh admin controls*

![Admin Removal Reason](PhoenixFlix_OutputSamples/AdminRights/Admin_Removal_Reason.png)
*Admin deletion reason prompt for audit trail*

![Comment Pending Approval](PhoenixFlix_OutputSamples/AdminRights/Comment_Pending_Approval.png)
*Admin guestbook moderation interface*

#### **3. Account Management System** 👤

**Features:**
- User registration with email verification
- Password reset with secure tokens
- JWT authentication
- WebAuthn/Passkey support
- Admin role management
- Collection management (favorites/watchlist)

**Visual Demonstrations:**

![Architecture Overview](PhoenixFlix_OutputSamples/Structures/Architecture_AccountManagement.png)
*Complete account management architecture diagram*

![Authentication Flow](PhoenixFlix_OutputSamples/Structures/Authentication_Flow.png)
*Full authentication flow including email verification and password reset*

![Optimistic Locking Sequence](PhoenixFlix_OutputSamples/Structures/Optimistic_Locking_Sequence_Diagram.png)
*Sequence diagram for concurrent operations with optimistic locking*

![Optimistic Locking Flowchart](PhoenixFlix_OutputSamples/Structures/Optimistic_Locking_Flowchart.png)
*Flowchart showing version-based conflict resolution*

#### **4. Password Reset System** 🔐

**Features:**
- Secure token-based password reset
- Email delivery via SMTP/SendGrid
- 1-hour token expiration
- Professional email templates

**Visual Demonstrations ˖°📷 ༘ :**

<img src="PhoenixFlix_OutputSamples/Reset_Password_Email/PhoenixFlix_RequestPassword_Reset.jpg" alt="Password Reset Request" width="400"/>
*Password reset request interface*

<img src="PhoenixFlix_OutputSamples/Reset_Password_Email/PhoenixFlix_ResetPasswords_Email.jpg" alt="Password Reset Email" width="400"/>
*Password reset email template*

<img src="PhoenixFlix_OutputSamples/Reset_Password_Email/Password_Reset_Sent.png" alt="Password Reset Sent" width="600"/>
*Confirmation message after password reset email is sent*

<img src="PhoenixFlix_OutputSamples/Reset_Password_Email/Password_Reset_Email_Inbox.png" alt="Password Reset Email Inbox" width="600"/>
*Password reset email as received in inbox*

#### **5. Crash-Proof Email System** 📧

**Features:**
- **Automatic Fallback Chain**: SendGrid → Resend → SMTP
- **Zero-Downtime Email**: App never crashes when email services expire
- **Professional Templates**: Consistent HTML design across all email types
- **Graceful Degradation**: Continues working even if primary email service fails
- **Production-Ready**: Handles SendGrid expiration on Dec 23, 2025

**Email Types:**
- **Welcome Email**: Professional onboarding with green "Verify Email (Optional)" button
- **Password Reset**: Secure reset with red "Reset Password" button  
- **Email Verification**: Resend verification with green "Verify Email" button

**Crash-Proof Implementation:**
```go
// Mailer priority: SendGrid → Resend → SMTP
func FromEnv() (EmailSender, error) {
    if sendGridKey := os.Getenv("SENDGRID_API_KEY"); sendGridKey != "" {
        return NewSendGridMailer() // Primary
    }
    if resendKey := os.Getenv("RESEND_API_KEY"); resendKey != "" {
        return NewResendMailer() // Backup
    }
    return NewSMTPMailer() // Final fallback
}

// Nil-safe email handling
if h.mailer != nil {
    go h.sendWelcomeEmail(email, name)
} else {
    h.logger.Error("Mailer disabled - emails unavailable", nil)
    // App continues working without emails
}
```

**Visual Demonstrations:**

<img src="PhoenixFlix_OutputSamples/Reset_Password_Email/WelcomeVerificationEmail.png" alt="Welcome Verification Email" width="600"/>
*Welcome verification email sent automatically during user registration*

**Key Benefits:**
- ✅ **Never Crashes**: App works even when all email services fail
- ✅ **Automatic Failover**: Seamless switching between providers
- ✅ **SendGrid Expiration Ready**: Prepared for Dec 23, 2025 expiration
- ✅ **Production Tested**: Handles real-world email service failures

#### 5. 🎄 Christmas Theme & Interactive Story Page ❄️

To celebrate the holiday season, a special Christmas theme was introduced, featuring an interactive story page that blends the classic tale of "The Little Match Girl" with the Phoenix's theme of hope and rebirth.

**Features:**
- **Interactive Homepage Postcard**: The homepage includes a festive, clickable postcard with hover effects that reveals thematic transformations and links to the full story. It also embeds a Christmas-themed video within a retro TV frame.
- **Dedicated Story Page (`Christmas.html`)**: A beautifully styled, standalone page that tells "The Phoenix and The Little Match Girl" story.
- **Immersive Experience**: The page includes a falling snow animation, custom typography, and themed visuals to create a magical and hopeful holiday atmosphere.

<img src="PhoenixFlix_OutputSamples/Christmas/Homepage_Christmas_theme.png" alt="Christmas Postcard on Homepage" width="800"/>
*The homepage features an interactive Christmas postcard with hover effects and a link to the story.*

<img src="PhoenixFlix_OutputSamples/Christmas/Phoenix_and_MatchGirl.png" alt="Christmas Story Page" width="800"/>
*The dedicated Christmas story page, telling a tale of hope and rebirth.*

#### **6. Automatic Read Fallback & Recovery System** 🔄

**Features:**
- **Automatic Read Fallback**: Intelligent failover from PRIMARY to BACKUP databases
- **Zero-Downtime Reads**: Users continue to see content even when PRIMARY database is down
- **Health Check System**: Background health checks (every 4 minutes) keep BACKUP databases warm
- **Neon Cold Start Prevention**: Health checks prevent auto-suspend on free tier databases
- **Transparent Operation**: No user-visible errors, automatic recovery
- **Comprehensive Coverage**: All read operations (movies, LDS, search, genres, etc.) support fallback

#### **7. 💰 Centralized Exchanges CEXs with Goroutines 🔀
While our final production code uses an efficient batch API (Massive.com), many real-world scenarios involve APIs that are slow or strictly rate-limited (e.g., one request per symbol). The `_DemoOnly` functions within `exchanges/CEXs_stocks.go` provide a practical playbook for handling these challenging situations using Go's powerful concurrency features.

##### Pattern 1: Channels for Asynchronous Operations

**Problem:** You need to fetch data from a slow API without blocking the main application thread.

**Solution:** Use a channel. A function can immediately return a channel and start the slow network operation in a separate goroutine. The main thread can continue its work and read the result from the channel whenever it's ready.

**Example:** `FetchStockWithChannel_DemoOnly`

```go
func FetchStockWithChannel_DemoOnly(ctx context.Context, symbol string, demoKey string) <-chan StockResult {
	resultChan := make(chan StockResult, 1)
	go func() {
		resultChan <- StockResult{ ... }
		close(resultChan)
	}()
	return resultChan 
}
```
**Timeouts are Critical:** A simple channel fetch can block forever if the API never responds. This leads to our next pattern.

**Pattern 1: Channels for Asynchronous Operations**

This pattern allows a function to return immediately while a slow operation (like a network request) runs in the background. The result is delivered back through a channel.

graph TD
    subgraph "Main Goroutine"
        A[Start: Call FetchStockWithSelect] --> B{Create resultChan}
        B --> C{Launch Worker Goroutine}
        C --> D{Enter 'select' block}
        D --> E{Wait for first channel to respond}
        E -->|Result received| F[Process successful result]
        E -->|Timeout reached| G[Return timeout error]
        F --> H[End]
        G --> H
    end

    subgraph "Worker Goroutine"
        I[Make HTTP Request to API] --> J[Receive API Response]
        J --> K{Send result into resultChan}
    end

    subgraph "Timeout"
        T[time.After(timeout) starts timer]
    end

    C --> I
    K --> E
    D --> T
    T --> E

![Pattern 1: Async Channel](PhoenixFlix_OutputSamples/CEXs_GoRoutines/Pattern1_Async_Channel.png)

##### Pattern 2: `select` for Handling Timeouts

**Problem:** An API call might hang indefinitely. You need to enforce a timeout to prevent your application from becoming unresponsive.

**Solution:** Use the `select` statement. It allows a goroutine to wait on multiple channel operations. We can combine our result channel with a timeout channel from `time.After`.

**Example:** `FetchStockWithSelect_DemoOnly`

```go
func FetchStockWithSelect_DemoOnly(ctx context.Context, symbol string, demoKey string, timeout time.Duration) (Stock, error) {
	resultChan := make(chan StockResult, 1)
	go func() {
		resultChan <- result
	}()
	select {
	case result := <-resultChan:
		return Stock{...}, nil
	case <-time.After(timeout):
		return Stock{}, fmt.Errorf("timeout after %v", timeout)	}
}
```
**Pattern 2: `select` for Handling Timeouts**

This pattern prevents a slow API call from hanging the application by "racing" the operation against a timeout. The `select` statement proceeds with whichever case finishes first.

graph TD
    subgraph Main Goroutine
        A[Start: Call FetchStockWithSelect] --> B{Create resultChan};
        B --> C{Launch Worker Goroutine};
        C --> D{Enter 'select' block};
        D --> E{Wait for first channel to respond};
        E -->|Result received| F[Process successful result];
        E -->|Timeout reached| G[Return timeout error];
        F --> H[End];
        G --> H;
    end
    subgraph Worker Goroutine
        C --> W1[Make HTTP Request to API];
        W1 --> W2[Receive API Response];
        W2 --> W3{Send result into resultChan};
    end
   
    subgraph Timeout
        D --> T1[time.After(timeout) starts timer];
    end
    W3 -- Data --> E;
    T1 -- Timer Fires --> E;

![Pattern 2: Timeout](PhoenixFlix_OutputSamples/CEXs_GoRoutines/Pattern2_Select_Timeout.png)

##### Pattern 3: Worker Pools for Rate Limiting and Concurrency Control

**Problem:** You need to fetch data for 200 stocks, but the API only allows 5 calls per minute. Making 200 sequential calls would take 40 minutes. Making 200 concurrent calls would instantly get you blocked by the rate limiter.

**Solution:** A worker pool. This pattern involves creating a fixed number of "worker" goroutines that pull tasks from a shared "jobs" channel. This allows you to process multiple requests in parallel while a central rate limiter controls how quickly new jobs are added to the queue.

**Example:** `FetchStocksWithWorkerPool_DemoOnly`

```go
func FetchStocksWithWorkerPool_DemoOnly(ctx context.Context, symbols []string, numWorkers int, demoKey string) map[string]Stock {
    symbolChan := make(chan string, len(symbols))
    resultChan := make(chan StockResult, len(symbols))
    for i := 0; i < numWorkers; i++ {
        go RunStockWorker_DemoOnly(ctx, i+1, symbolChan, resultChan, demoKey)    }
    rateLimiter := time.NewTicker(12 * time.Second) 
    defer rateLimiter.Stop()
    for _, symbol := range symbols {
        <-rateLimiter.C 
        symbolChan <- symbol    }
    close(symbolChan) 
    results := make(map[string]Stock)
    for i := 0; i < len(symbols); i++ {
        result := <-resultChan    }
    return results
}
```
**Pattern 3: Worker Pool for Rate Limiting**

This pattern controls concurrency and respects API rate limits. A "Feeder" adds jobs to a queue at a controlled rate, and a fixed number of "Workers" process those jobs in parallel.

graph TD
    subgraph Main Goroutine
        A[Start: Call FetchStocksWithWorkerPool] --> B{Create jobsChan & resultsChan};
        B --> C{Launch N Worker Goroutines};
        B --> D{Launch Feeder Goroutine};
        D --> E{Collect all results from resultsChan};
        E --> F[End];
    end
    subgraph Feeder Goroutine
        D --> F1{Loop through all symbols};
        F1 --> F2{Wait for Rate Limiter Tick};
        F2 --> F3{Send symbol to jobsChan};
        F3 --> F1;
        F1 -- All symbols sent --> F4[Close jobsChan];
    end
    subgraph Worker Goroutine 1
        C --> W1_1{Wait for job from jobsChan};
        W1_1 --> W1_2[Fetch API for symbol];
        W1_2 --> W1_3{Send result to resultsChan};
        W1_3 --> W1_1;
    end
   
    subgraph Worker Goroutine 2
        C --> W2_1{Wait for job from jobsChan};
        W2_1 --> W2_2[Fetch API for symbol];
        W2_2 --> W2_3{Send result to resultsChan};
        W2_3 --> W2_1;
    end
    subgraph "..."
        C --> WN_1["..."];
    end
    F3 -- Job --> W1_1;
    F3 -- Job --> W2_1;
    W1_3 -- Result --> E;
    W2_3 -- Result --> E;

![Pattern 3: Worker Pool](PhoenixFlix_OutputSamples/CEXs_GoRoutines/Pattern3_Worker_Pool.png)

**Visual Demonstrations:**

![System Architecture Diagram](PhoenixFlix_OutputSamples/Auto_Recovery/System_Diagram_AutoRecovery.png)
*High-level system architecture showing PRIMARY/BACKUP databases and health check system*

![Read Fallback Decision Tree](PhoenixFlix_OutputSamples/Auto_Recovery/Read_FallBack_Decision_AutoRecovery.png)
*Decision tree showing automatic fallback logic when PRIMARY database fails*

![Application Startup Flow](PhoenixFlix_OutputSamples/Auto_Recovery/App_StartUp_AutoRecovery.png)
*Application startup sequence with database connection setup and health check initialization*

**📚 Comprehensive Documentation:**

For detailed implementation guides, see the AutoRecovery documentation in `BT_AutoRecover/`:

- **[Analysis_Report_AutoRecovery.md](Analysis_Report_AutoRecovery.md)** - Complete technical analysis with architecture overview, implementation details, and code references
- **[BUILD_ORDER_AutoRecovery.md](BUILD_ORDER_AutoRecovery.md)** - Step-by-step implementation checklist with 8 phases and testing strategies
- **[FLOWCHARTS_AutoRecovery.md](FLOWCHARTS_AutoRecovery.md)** - Visual architecture diagrams, data flow diagrams, and implementation patterns

**Key Benefits:**
- ✅ **High Availability**: Application continues working even when PRIMARY database is down
- ✅ **No Manual Intervention**: Automatic failover requires no administrator action
- ✅ **Better User Experience**: Users see content instead of error messages
- ✅ **Free Tier Compatible**: Health checks prevent Neon cold starts on free tier
- ✅ **Production Ready**: Comprehensive error handling and logging for all scenarios
- ✅ **Optimized Performance**: 34% smaller bundle size with automated build pipeline

**📈 Performance Metrics:**

| Component | Before | After | Savings |
|-----------|--------|-------|---------|
| **Go Binary** | ~15MB | ~10MB | **33%** |
| **CSS Files** | ~50KB | ~25KB | **50%** |
| **JS Files** | ~100KB | ~60KB | **40%** |
| **Transfer (Gzip)** | 100% | ~30% | **70%** |
| **Total Bundle** | ~15.2MB | ~10.1MB | **34%** |

**🔧 Optimization Features:**
- ✅ **Route Consolidation**: Single handler for static pages (80% code reduction)
- ✅ **Database Pooling**: Optimal connection settings (25 max, 5 idle, 5min lifetime)
- ✅ **Gzip Compression**: Automatic compression middleware (70% transfer reduction)
- ✅ **Asset Minification**: CSS/JS optimization with fallback support
- ✅ **Build Automation**: One-command production builds

**Automation Tools** (in root directory):
- **[switch-environment.ps1](switch-environment.ps1)**: Automated environment switcher
  - Usage: `.\switch-environment.ps1 production` or `.\switch-environment.ps1 local`
  - Automatically updates all necessary files
  - No manual editing required!

- **[check-changes.ps1](check-changes.ps1)**: See all your changes
  - Shows modified files by category
  - Checks current configuration
  - Provides recommendations

**🚀 Production Optimization Tools:**
- **[build-optimized.ps1](build-optimized.ps1)**: Complete production build
  - Optimizes Go binary (30% size reduction)
  - Minifies CSS/JS assets (50% size reduction)
  - Creates `phoenixflix-min.exe` and `public/min/` assets
  - Usage: `.\build-optimized.ps1`

- **[minify-manual.ps1](minify-manual.ps1)**: Frontend-only minification
  - Manual CSS/JS minification (no npm dependencies)
  - Basic but effective compression
  - Usage: `.\minify-manual.ps1`

**📦 Deployment Workflow:**
```bash
# 1. Optimize for production
.\build-optimized.ps1

# 2. Test optimized build
.\phoenixflix-min.exe

# 3. Deploy to GitHub (Render + Vercel auto-deploy)
git add .
git commit -m "Optimized production build"
git push origin main
```

**🎯 File Structure After Optimization:**
```
PhoenixflixChristmas/
├── main.go                    # Source code
├── phoenixflix-min.exe        # Optimized binary (34% smaller)
├── public/
│   ├── app.js                # Original assets
│   ├── styles.css            # (for development)
│   └── min/                  # Minified assets
│       ├── app.min.js        # (for production)
│       └── styles.min.css    # 50% smaller
├── build-optimized.ps1        # Build automation
└── .gitignore                # Allows minified assets
```

### **Architecture Diagrams**

All architecture diagrams and flowcharts are located in `PhoenixFlix_OutputSamples/`:

#### **Structures/** (`PhoenixFlix_OutputSamples/Structures/`)
- **Optimistic_Locking_Sequence_Diagram.png**: Detailed sequence diagram for concurrent operations
- **Optimistic_Locking_Flowchart.png**: Visual flowchart of race condition prevention
- **Architecture_AccountManagement.png**: Complete account management architecture
- **Authentication_Flow.png**: Full authentication flow including email verification

#### **Auto_Recovery/** (`PhoenixFlix_OutputSamples/Auto_Recovery/`)
- **System_Diagram_AutoRecovery.png**: High-level system architecture with PRIMARY/BACKUP databases
- **Read_FallBack_Decision_AutoRecovery.png**: Decision tree for automatic read fallback logic
- **App_StartUp_AutoRecovery.png**: Application startup sequence with health check system

### **Application Screenshots**
Located in `PhoenixFlix_OutputSamples/`:

#### **Desktop (PC)**
- Homepage and navigation
- Movie browsing and search
- LDS content section
- Authentication flows (login, registration, passkeys)
- Admin moderation panel
- Guestbook features
- Favorites and watchlist

#### **Mobile (iOS & Android)**
- Responsive design on mobile devices
- Touch-optimized interface
- Biometric authentication (Face ID, Touch ID)
- Progressive Web App installation
- Cross-platform consistency

#### **Email Features**
- Password reset email templates
- Email verification confirmations
- Professional SMTP integration

All diagrams and screenshots demonstrate production-ready features with enterprise-level polish.

## 📞 Support

For support and questions:
- Create an issue on GitHub
- Contact: [thephoenixflix@gmail.com](mailto:thephoenixflix@gmail.com)

---

## 🌟 **Final Thoughts**

**PhoenixFlix** represents more than just a technical achievement - it's a **vision realized**. In a digital age where content often compromises values, this platform stands as a testament to what's possible when technology serves faith, family, and community.

**Built with ❤️, faith, and cutting-edge technology**  
*Go • PostgreSQL (Neon + Aiven) • Render • Vercel • WebAuthn • Clean Architecture • Family Values*

---

### **🚀 Ready to Launch**
This project is **production-ready** and demonstrates enterprise-level software development skills. From dual-database architecture to modern authentication systems, PhoenixFlix showcases the full spectrum of full-stack development mastery.

**The future of family-friendly streaming starts here.** 🎬✨#

# PhoenixflixChristmasBundle
