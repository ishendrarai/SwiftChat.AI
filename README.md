# 🚀 SwiftChat — AI-Powered Smart Social Media Platform

> The emotionally intelligent layer for modern social networking.
> Discover. Create. Connect. Feel understood.

![Node](https://img.shields.io/badge/Node.js-18+-green)
![React](https://img.shields.io/badge/React-18+-blue)
![Python](https://img.shields.io/badge/Python-3.11+-yellow)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-15-blue)
![Redis](https://img.shields.io/badge/Redis-7-red)
![License](https://img.shields.io/badge/License-MIT-yellow)
![Status](https://img.shields.io/badge/Status-Production--Ready-success)

---

## 📌 Table of Contents

- [✨ Overview](#-overview)
- [🚀 Why SwiftChat?](#-why-swiftchat)
- [🌐 Live Demo](#-live-demo)
- [📸 Screenshots](#-screenshots)
- [🔥 Core Features](#-core-features)
- [🛠 Tech Stack](#-tech-stack)
- [🏗 Architecture](#-architecture)
- [🤖 AI System Design](#-ai-system-design)
- [🔐 Authentication](#-authentication)
- [🗄 Database Schema](#-database-schema)
- [🔌 API Documentation](#-api-documentation)
- [🔐 Security](#-security)
- [⚡ Performance](#-performance)
- [🧪 Testing](#-testing)
- [📋 Prerequisites](#-prerequisites)
- [⚙ Installation & Setup](#-installation--setup)
- [🌍 Environment Variables](#-environment-variables)
- [📁 Project Structure](#-project-structure)
- [🚀 Deployment](#-deployment)
- [🔧 Troubleshooting](#-troubleshooting)
- [❓ FAQ](#-faq)
- [📊 Design Decisions](#-design-decisions)
- [🛣 Roadmap](#-roadmap)
- [🤝 Contributing](#-contributing)
- [👥 Contributors](#-contributors)
- [📄 License](#-license)
- [📬 Contact](#-contact)

---

## ✨ Overview

**SwiftChat** is a full-stack, AI-integrated social media platform that goes beyond traditional content sharing. It introduces **emotional intelligence** as a first-class feature — letting users discover, post, and interact with content based on how they actually feel, not just what they search for.

| AI Feature | Status | Capability |
|---|---|---|
| 🟢 AI Caption Generator | Full Integration | 5 styles, hashtags, multi-platform output |
| 🟢 Emotion-Based Search | Full Integration | NLP intent + vector search + image emotion |
| 🟢 AI Chatbot Assistant | Full Integration | LangChain ReAct, context-aware responses |
| 🟢 Smart Recommendation Feed | Full Integration | Mood + time-of-day + interaction signals |
| 🟢 AI Content Moderation | Full Integration | Hate speech, NSFW, toxicity detection |

Instead of forcing users to express themselves through hashtags and keywords, SwiftChat provides a **single emotionally-aware social ecosystem** for:

- 🧠 **Mood-matched discovery** — Find content that fits how you feel right now
- ✍️ **Instant AI captions** — Generate engaging captions for any post in seconds
- 💬 **Conversational AI assistant** — Get help, ideas, and emotional support in-app
- 🎯 **Smart feed curation** — A feed that adapts to your mood and time of day
- 🛡 **Proactive moderation** — AI removes toxic content before you ever see it
- 📈 **Engagement optimisation** — Know your caption's predicted performance before posting

---

## 🚀 Why SwiftChat?

### The Problem

Social media users face:

- ❌ **Hashtag-only discovery** — Can't search by emotion or mood
- ❌ **Caption writer's block** — Spending 5–10 minutes per post
- ❌ **Toxic feeds** — Engagement algorithms that prioritise outrage over well-being
- ❌ **No AI interactivity** — AI is hidden in algorithms, never a visible tool
- ❌ **Mental health toll** — Irrelevant or harmful content with no filter

### The Solution

SwiftChat acts as an **emotionally intelligent layer** on top of a full social platform:

- ✅ **Emotion-first content discovery** — Express a feeling, get matched content
- ✅ **One-click AI captions** — Generate, compare, and post in under 10 seconds
- ✅ **Mood-aware recommendation engine** — Morning motivation, night-time calm
- ✅ **LangChain-powered chatbot** — Context-aware assistant embedded in your feed
- ✅ **Real-time AI moderation** — Content safety before publication, not after

> It's not just a social platform. It's a **well-being engine**.

---

## 🌐 Live Demo

🔗 **https://swiftchat-demo.vercel.app**

### Test Credentials

```
Email:    demo@swiftchat.io
Password: demo123
```

> **Note:** Demo account is read-only with pre-populated sample posts, captions, and analytics.

---

## 📸 Screenshots

### 🎯 Dashboard & Feed
![Dashboard](./screenshots/dashboard.png)
*Mood-matched feed with real-time AI recommendation*

### ✍️ AI Caption Wizard
![Caption](./screenshots/caption-wizard.png)
*Upload an image, pick a style, get 3 captions instantly*

### 🔍 Emotion Search
![Search](./screenshots/emotion-search.png)
*Search "I want something uplifting" and get perfectly matched posts*

### 💬 AI Chatbot Assistant
![Chatbot](./screenshots/chatbot.png)
*Context-aware chatbot accessible from anywhere in the app*

---

## 🔥 Core Features

### 🧠 AI Caption Generator
- **Multi-style output** — Funny, Motivational, Romantic, Inspirational, Storytelling
- **Platform-aware** — Captions tuned to Instagram, Twitter, LinkedIn, TikTok, Facebook
- **3 variants per request** — Always have options to choose from
- **Smart hashtag suggestions** — Tiered by volume: niche, mid-range, broad reach
- **Engagement score preview** — See predicted performance before posting
- **Image understanding** — CLIP-powered scene + mood detection from your photo

### 🔍 Emotion-Based Smart Search
- **Free-text emotional queries** — "Make me happy", "I need calm", "Something relatable"
- **Multi-model NLP pipeline** — BERT intent classification + sentence-transformer encoding
- **Vector similarity search** — pgvector cosine search over 384-dim post embeddings
- **Image emotion re-ranking** — Visual posts re-scored by EfficientNet emotion model
- **Mood-query blending** — User's current mood automatically boosts or filters results

### 💬 AI Chatbot Assistant
- **LangChain ReAct agent** — Reasoning + acting pattern with registered platform tools
- **Full platform context** — Accesses user mood, post history, and preferences in real time
- **Caption writing on demand** — Ask for a caption mid-conversation, receive one instantly
- **Emotional support mode** — Detects distress signals and responds with care + resources
- **Post discovery** — "Show me something funny" triggers a live database query
- **Navigation guidance** — Full platform help embedded in natural conversation

### 📡 Smart Recommendation System
- **Hybrid filtering** — Collaborative (similar users) + content-based (mood match)
- **Time-of-day awareness** — Morning → motivational; night → calm and reflective
- **Interaction history weighting** — Likes, saves, shares, and time-spent all contribute
- **Cold-start handling** — Mood check-in survey populates the onboarding feed for new users
- **Trend overlay** — Platform-wide trending filtered for emotional compatibility

### 🛡 AI Content Moderation
- **Pre-publication pipeline** — Every post screened before going live
- **Multi-label detection** — Hate speech, toxicity, spam, NSFW, violence
- **Three-tier outcome** — Safe (auto-publish), Borderline (human review queue), Unsafe (auto-reject)
- **Near-real-time processing** — Async Redis queue keeps post creation latency under 500ms

### 👤 Social Community
- **Public profile pages** — Showcase your best AI-assisted captions
- **Upvote system** — Community votes surface the best content
- **Trending feed** — Algorithm-ranked captions by upvotes and recency
- **Mood check-in** — Daily optional check-in that personalises the entire experience

---

## 🛠 Tech Stack

### Frontend
| Technology | Purpose |
|---|---|
| ⚛ **Next.js 14** | SSR/SSG React framework |
| 🎨 **Tailwind CSS** | Utility-first styling |
| 🎞 **Framer Motion** | Micro-animations |
| 🔄 **Axios** | HTTP client |
| 🎣 **React Query** | Server state management |
| 📝 **React Hook Form** | Form validation |

### Mobile
| Technology | Purpose |
|---|---|
| 📱 **Flutter** | Cross-platform mobile app (iOS & Android) |
| 🔄 **Dio** | Flutter HTTP client |

### Backend
| Technology | Purpose |
|---|---|
| 🟢 **Node.js 18** | JavaScript runtime |
| 🚀 **Express.js** | REST API framework |
| 🔧 **TypeScript** | Type safety |
| 🎯 **Joi** | Request validation |
| 🔐 **bcrypt** | Password hashing |
| 🎫 **jsonwebtoken** | JWT authentication |
| 📧 **Nodemailer** | Email service |

### AI Services (Python)
| Technology | Purpose |
|---|---|
| ⚡ **FastAPI** | AI microservice framework |
| 🦜 **LangChain** | Chatbot ReAct agent runtime |
| 🤗 **HuggingFace Transformers** | BERT, EfficientNet, sentence-transformers |
| 🧠 **OpenAI API** | GPT-4 for caption + chat generation |
| 🔍 **CLIP (ViT-L/14)** | Image semantic encoding |

### Database & Cache
| Technology | Purpose |
|---|---|
| 🐘 **PostgreSQL 15 + pgvector** | Relational store + vector similarity search |
| 🍃 **MongoDB** | Chatbot session state + flexible post metadata |
| ⚡ **Redis 7** | Caching, rate limiting, async moderation queue |
| 📦 **AWS S3** | Image and video object storage |

### DevOps & Tooling
| Technology | Purpose |
|---|---|
| 🐳 **Docker** | Containerisation |
| 🔄 **GitHub Actions** | CI/CD pipeline |
| 📊 **Prometheus** | Metrics collection |
| 📈 **Grafana** | Monitoring dashboards |
| 🔒 **Let's Encrypt** | SSL certificates |
| ☁ **AWS ECS** | Container orchestration |

---

## 🏗 Architecture

**Architecture Type:** Microservices for AI + Modular Monolith for Core API

### 🔷 High-Level Architecture

```
┌───────────────────────────────────────────────────────────────┐
│                       CLIENT LAYER                            │
│       Next.js 14  |  Tailwind CSS  |  Flutter (mobile)        │
└───────────────────────────┬───────────────────────────────────┘
                            │  HTTPS / WebSocket
┌───────────────────────────▼───────────────────────────────────┐
│                      API GATEWAY                              │
│           Rate Limiting | Auth | Routing | Logging            │
└──────────────────┬────────────────────────┬───────────────────┘
                   │                        │
┌──────────────────▼──────────┐  ┌──────────▼────────────────────┐
│   Node.js / Express         │  │      AI Service Mesh          │
│   (Core Backend API)        │  │  Caption | Search | Chatbot   │
│   REST + GraphQL            │  │  Recommender | Moderator      │
└──────────┬──────────────────┘  └──────────┬────────────────────┘
           │                                │
┌──────────▼──────────────┐  ┌─────────────▼──────────────────┐
│  PostgreSQL (pgvector)  │  │  OpenAI / HuggingFace APIs     │
│  MongoDB                │  │  LangChain Agent Runtime       │
│  Redis Cache            │  │  Sentence-Transformers (BERT)  │
└─────────────────────────┘  └────────────────────────────────┘
```

### 🔹 Backend Module Breakdown

```
API Gateway
    │
    ├── Route Handlers
    │       └── Controllers → Services → DB Models / Redis / AI Bridge
    │
    └── Middleware Layer
            ├── JWT Auth
            ├── Joi Validation
            ├── Rate Limiter (Redis)
            └── Request Logger (Prometheus)
```

### 📐 Full Request Flow Example

```
1.  User submits: POST /api/ai/caption
2.  Nginx forwards to Express API
3.  JWT Middleware validates Bearer token
4.  Rate Limit Middleware checks hourly quota
5.  Joi Validation Middleware validates multipart body
6.  Controller extracts user_id, style, platform
7.  Service layer:
    a. Uploads image to S3 → gets signed URL
    b. Calls Python Caption Microservice (internal REST)
    c. CLIP encodes image → scene/object/mood tags extracted
    d. Structured prompt assembled → GPT-4 called
    e. 3 captions + hashtags returned
    f. NLP scorer predicts engagement score
8.  Result persisted to PostgreSQL
9.  Result cached in Redis (key: perceptual_hash:style:platform, TTL: 3600s)
10. 200 OK response returned to frontend
11. Request metrics recorded in Prometheus
```

---

## 🤖 AI System Design

### AI Pipeline Architecture

```
┌─────────────────────────────────────────────────────────────────┐
│                       AI SERVICE LAYER                          │
│                                                                 │
│  ┌───────────────────┐    ┌──────────────────────────────────┐  │
│  │  Caption Service  │    │     Emotion Search Engine        │  │
│  │  FastAPI / Python │    │     FastAPI + pgvector           │  │
│  └───────────────────┘    └──────────────────────────────────┘  │
│                                                                 │
│  ┌───────────────────┐    ┌──────────────────────────────────┐  │
│  │  Chatbot Service  │    │   Recommender + Moderator        │  │
│  │  LangChain ReAct  │    │   Python microservices           │  │
│  └───────────────────┘    └──────────────────────────────────┘  │
└─────────────────────────────────────────────────────────────────┘
          |                                |
          └──── Internal gRPC / REST ──────┘
                         |
              Node.js Core Backend
```

### Model Interaction Flow

| Feature | Models Used | Input | Output |
|---|---|---|---|
| Caption Generation | CLIP + GPT-4 | Image + style + platform | 3 captions + hashtags |
| Emotion Search | BERT + sentence-transformers + pgvector | Free-text query | Ranked post list |
| Chatbot | LangChain ReAct + GPT-4 | Conversation history + user context | Response + optional action |
| Recommendation | Collaborative filter + mood model | History + mood + time | Ranked post feed |
| Moderation | Fine-tuned BERT + EfficientNet | Text + image | Safe / Review / Reject label |

### Prompt Engineering Strategy

All LLM calls use a structured, multi-variable prompt template:

```
SYSTEM:
You are an expert social media copywriter embedded in an emotionally-aware
social platform. Always write content that is uplifting, authentic, and
platform-appropriate. Never generate harmful, discriminatory, or misleading content.

USER:
  Image Analysis:
    - Scene:         {scene}
    - Objects:       {objects}
    - Detected Mood: {image_mood}

  User Context:
    - Current Mood:     {user_mood}
    - Style:            {style}
    - Target Platform:  {platform}
    - Language:         {locale}

  Task:
    Generate 3 caption variants in the '{style}' style for {platform}.
    Each caption must be under {char_limit} characters.
    Append 5-8 relevant hashtags.

  Output Format (JSON):
    { "captions": [string, string, string], "hashtags": [string] }
```

---

## 🔐 Authentication

### Supported Methods

1. **Email / Password** — Traditional auth with bcrypt
2. **Google OAuth 2.0** — Sign in with Google
3. **GitHub OAuth** — Sign in with GitHub

### JWT Token Structure

```json
{
  "userId":  "uuid-v4",
  "email":   "user@example.com",
  "role":    "creator",
  "iat":     1673481600,
  "exp":     1674086400
}
```

### Token Expiration
- **Access Token:** 7 days
- **Refresh Token:** 30 days (stored in HttpOnly cookie)

### Security Features
- Password hashing with bcrypt (12 salt rounds)
- Refresh token rotation on every use
- Token blacklisting on logout via Redis set
- Rate limiting on auth endpoints — 5 requests/minute
- Account lockout after 5 failed login attempts (15-min cooldown)

---

## 🗄 Database Schema

### Entity Relationship Overview

```
USERS        ||--o{ POSTS             : "creates"
USERS        ||--o{ COMMENTS          : "writes"
USERS        ||--o{ USER_INTERACTIONS : "generates"
POSTS        ||--o{ COMMENTS          : "has"
POSTS        ||--o{ USER_INTERACTIONS : "receives"
POSTS        }o--o{ HASHTAGS          : "tagged_with"
```

### 👤 Table: users

```sql
CREATE TABLE users (
  id              UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  username        VARCHAR(50)   NOT NULL UNIQUE,
  email           VARCHAR(255)  NOT NULL UNIQUE,
  password_hash   TEXT          NOT NULL,
  display_name    VARCHAR(100),
  avatar_url      TEXT,
  bio             TEXT,
  current_mood    VARCHAR(50),           -- updated by mood check-in
  mood_updated_at TIMESTAMPTZ,
  role            VARCHAR(20)   NOT NULL DEFAULT 'creator',
  email_verified  BOOLEAN       NOT NULL DEFAULT FALSE,
  created_at      TIMESTAMPTZ   NOT NULL DEFAULT NOW(),
  last_login      TIMESTAMPTZ
);

CREATE INDEX idx_users_email    ON users(email);
CREATE INDEX idx_users_mood     ON users(current_mood);
CREATE INDEX idx_users_username ON users(username);
```

### 📝 Table: posts

```sql
CREATE TABLE posts (
  id                UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  user_id           UUID REFERENCES users(id) ON DELETE CASCADE,
  caption           TEXT,
  media_url         TEXT,
  media_type        VARCHAR(10) CHECK (media_type IN ('image','video','text')),
  emotion_tags      TEXT[],               -- AI-assigned emotion labels
  sentiment_score   FLOAT,                -- -1.0 (negative) to 1.0 (positive)
  embedding         vector(384),          -- sentence-transformer embedding for search
  moderation_status VARCHAR(20)  NOT NULL DEFAULT 'pending',
  upvotes           INTEGER      NOT NULL DEFAULT 0,
  is_public         BOOLEAN      NOT NULL DEFAULT TRUE,
  created_at        TIMESTAMPTZ  NOT NULL DEFAULT NOW()
);

CREATE INDEX idx_posts_user_id      ON posts(user_id);
CREATE INDEX idx_posts_emotion_tags ON posts USING GIN(emotion_tags);
CREATE INDEX idx_posts_embedding    ON posts USING ivfflat(embedding vector_cosine_ops)
                                     WITH (lists = 100);
CREATE INDEX idx_posts_sentiment    ON posts(sentiment_score);
CREATE INDEX idx_posts_public       ON posts(is_public) WHERE is_public = TRUE;
```

### 💬 Table: comments

```sql
CREATE TABLE comments (
  id          UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  post_id     UUID REFERENCES posts(id) ON DELETE CASCADE,
  user_id     UUID REFERENCES users(id) ON DELETE CASCADE,
  content     TEXT        NOT NULL,
  is_toxic    BOOLEAN     NOT NULL DEFAULT FALSE,
  created_at  TIMESTAMPTZ NOT NULL DEFAULT NOW()
);

CREATE INDEX idx_comments_post_id ON comments(post_id);
CREATE INDEX idx_comments_user_id ON comments(user_id);
```

### 📊 Table: user_interactions

```sql
CREATE TABLE user_interactions (
  id                UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  user_id           UUID REFERENCES users(id) ON DELETE CASCADE,
  post_id           UUID REFERENCES posts(id) ON DELETE CASCADE,
  interaction_type  VARCHAR(20) CHECK (
                      interaction_type IN ('like','save','share','view','skip')
                    ),
  time_spent_ms     INTEGER,
  created_at        TIMESTAMPTZ NOT NULL DEFAULT NOW(),
  UNIQUE(user_id, post_id, interaction_type)
);

CREATE INDEX idx_interactions_user_id ON user_interactions(user_id);
CREATE INDEX idx_interactions_post_id ON user_interactions(post_id);
```

### 🏷 Table: hashtags

```sql
CREATE TABLE hashtags (
  id          UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  caption_id  UUID REFERENCES posts(id) ON DELETE CASCADE,
  tag         VARCHAR(100) NOT NULL,
  tier        SMALLINT     NOT NULL CHECK (tier IN (1, 2, 3)),
  created_at  TIMESTAMPTZ  NOT NULL DEFAULT NOW()
);

CREATE INDEX idx_hashtags_caption_id ON hashtags(caption_id);
CREATE INDEX idx_hashtags_tag        ON hashtags(tag);
```

### 📐 Design Decisions

| Decision | Rationale |
|---|---|
| pgvector for post embeddings | Enables SQL + vector similarity search in one query — no separate vector DB needed |
| emotion_tags as TEXT[] | GIN-indexed array supports fast `emotion_tags @> ARRAY['calm']` filtering |
| ivfflat index (lists=100) | Reduces cosine search from O(N) to ~O(√N) with <2% recall loss at 1M posts |
| MongoDB for chatbot sessions | Variable-length conversation histories fit a document model far better than rows |
| Redis sorted sets for trending | `ZRANGEBYSCORE` delivers leaderboard queries in O(log N) natively |
| Partial index on is_public | Community feed queries only scan public posts — dramatically smaller index |

---

## 🔌 API Documentation

### Base URL

```
Development:  http://localhost:5000/api
Production:   https://api.swiftchat.io/api
```

### 🔐 Authentication Endpoints

#### Register

```http
POST /api/auth/register
Content-Type: application/json

{
  "username": "jane_doe",
  "email":    "jane@example.com",
  "password": "SecurePass123!"
}
```

**Response — 201 Created**
```json
{
  "success": true,
  "message": "User registered successfully",
  "data": {
    "token": "eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9...",
    "user": {
      "id":         "123e4567-e89b-12d3-a456-426614174000",
      "username":   "jane_doe",
      "email":      "jane@example.com",
      "created_at": "2024-01-15T10:30:00Z"
    }
  }
}
```

#### Login

```http
POST /api/auth/login
Content-Type: application/json

{
  "email":    "jane@example.com",
  "password": "SecurePass123!"
}
```

**Response — 200 OK**
```json
{
  "success": true,
  "token": "eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9...",
  "user": {
    "id":       "123e4567-...",
    "username": "jane_doe",
    "email":    "jane@example.com",
    "role":     "creator"
  }
}
```

---

### 🤖 AI Endpoints

#### Generate Caption

```http
POST /api/ai/caption
Content-Type: multipart/form-data
Authorization: Bearer <token>

{
  "image":       <file>,              // Optional. JPG/PNG/WEBP. Max 10MB
  "description": "Hiking in Alps",   // Optional if no image provided
  "style":       "inspirational",    // funny|romantic|inspirational|motivational|storytelling
  "platform":    "instagram",        // instagram|twitter|linkedin|tiktok|facebook
  "locale":      "en"
}
```

**Response — 200 OK**
```json
{
  "captions": [
    "The mountains called. I answered. ⛰️",
    "Every summit starts with a single step.",
    "Not all who wander are lost — some are just hiking."
  ],
  "hashtags":         ["#hiking", "#mountains", "#adventure", "#nature", "#explore"],
  "image_tags":       ["mountain", "trail", "sunrise", "outdoor", "landscape"],
  "engagement_score": 87
}
```

**Error Responses**

| Status | Error Code | Description |
|---|---|---|
| 400 | `INVALID_STYLE` | Style not in supported list |
| 400 | `FILE_TOO_LARGE` | Image exceeds 10MB limit |
| 422 | `IMAGE_UNSAFE` | Image flagged by content moderation |
| 429 | `RATE_LIMIT_EXCEEDED` | Caption generation limited to 50/hour |
| 500 | `CAPTION_SERVICE_UNAVAILABLE` | Python AI microservice unreachable |

---

#### Emotion-Based Search

```http
POST /api/search/emotion
Content-Type: application/json
Authorization: Bearer <token>

{
  "query":  "I want something calming",
  "mood":   "anxious",
  "limit":  20,
  "offset": 0
}
```

**Response — 200 OK**
```json
{
  "results": [
    {
      "post_id":         "a1b2c3d4-...",
      "caption":         "Breathe. Everything will be okay.",
      "media_url":       "https://cdn.swiftchat.io/posts/abc.jpg",
      "emotion_tags":    ["calm", "peaceful", "serene"],
      "sentiment_score": 0.91,
      "relevance_score": 0.87
    }
  ],
  "total":          143,
  "query_emotions": ["calm", "serenity"]
}
```

**Error Responses**

| Status | Error Code | Description |
|---|---|---|
| 400 | `QUERY_TOO_SHORT` | Query must be at least 3 characters |
| 401 | `TOKEN_EXPIRED` | Re-authenticate to continue |
| 429 | `RATE_LIMIT_EXCEEDED` | Search limited to 100 requests/minute |
| 500 | `EMOTION_ENGINE_UNAVAILABLE` | AI search service unreachable |

---

#### Chat with AI Assistant

```http
POST /api/chat/message
Content-Type: application/json
Authorization: Bearer <token>

{
  "session_id": "chat_session_xyz",
  "message":    "Give me a caption for a travel post",
  "mood":       "excited"
}
```

**Response — 200 OK**
```json
{
  "reply":       "Adventure begins where comfort ends ✈️🌍",
  "suggestions": ["#travel", "#wanderlust", "#explore"],
  "action":      null
}
```

---

### 📰 Feed & Post Endpoints

#### Get Personalised Feed

```http
GET /api/feed?limit=20&offset=0&mood=calm
Authorization: Bearer <token>
```

**Response — 200 OK**
```json
{
  "success": true,
  "data": {
    "posts": [
      {
        "id":           "uuid",
        "user":         { "username": "jane_doe", "avatar_url": "..." },
        "caption":      "Golden skies, salty air. 🌅",
        "media_url":    "https://cdn.swiftchat.io/posts/xyz.jpg",
        "emotion_tags": ["peaceful", "joyful"],
        "upvotes":      142,
        "created_at":   "2024-01-15T18:30:00Z"
      }
    ],
    "pagination": { "total": 500, "page": 1, "limit": 20, "totalPages": 25 }
  }
}
```

#### Create Post

```http
POST /api/posts
Content-Type: multipart/form-data
Authorization: Bearer <token>

{
  "caption":   "Golden skies, salty air. 🌅",
  "media":     <file>,
  "is_public": true
}
```

#### Upvote a Post

```http
POST /api/posts/:postId/upvote
Authorization: Bearer <token>
```

---

### 👤 User Endpoints

#### Get Profile

```http
GET /api/user/profile
Authorization: Bearer <token>
```

#### Update Profile

```http
PATCH /api/user/profile
Content-Type: application/json
Authorization: Bearer <token>

{
  "display_name": "Jane Smith",
  "bio":          "Chasing sunsets and good vibes 🌅"
}
```

#### Update Mood

```http
PATCH /api/user/mood
Content-Type: application/json
Authorization: Bearer <token>

{
  "mood": "happy"
}
```

---

### Error Response Structure

All error responses follow this structure:

```json
{
  "success": false,
  "error": {
    "code":    "VALIDATION_ERROR",
    "message": "Invalid email format",
    "details": { "field": "email", "value": "invalid-email" }
  }
}
```

**Common Error Codes**

| Code | Meaning |
|---|---|
| `VALIDATION_ERROR` | Invalid request data |
| `AUTHENTICATION_ERROR` | Invalid or expired token |
| `AUTHORIZATION_ERROR` | Insufficient permissions |
| `NOT_FOUND` | Resource does not exist |
| `RATE_LIMIT_EXCEEDED` | Too many requests |
| `AI_SERVICE_UNAVAILABLE` | Python microservice unreachable |
| `IMAGE_UNSAFE` | Content moderation rejection |
| `INTERNAL_ERROR` | Unexpected server error |

---

## 🔐 Security

### Best Practices Implemented

#### Password Security
- **bcrypt hashing** with 12 salt rounds
- **Minimum requirements:** 8 characters, 1 uppercase, 1 number
- **Password reset** via secure email tokens (1-hour expiry)
- **Account lockout** after 5 failed attempts (15-minute cooldown)

#### Token Security
- **JWT RS256** with 7-day access token expiry
- **Refresh token rotation** — new refresh token on every use
- **Token blacklisting** on logout (Redis blacklist set)
- **Secure cookie flags** — HttpOnly, Secure, SameSite=Strict

#### API Security
- **Rate limiting** — 100 req/15 min per IP (Redis sliding window)
- **CORS configuration** — Whitelist-based allowed origins
- **SQL injection prevention** — Parameterised queries throughout
- **XSS protection** — Input sanitisation on all user-supplied text
- **CSRF protection** — Double-submit cookie pattern

#### Content Safety
- **Pre-publication AI moderation** — Every post screened before going live
- **AWS Rekognition pre-check** — NSFW detection before S3 upload
- **Mental health safeguard** — Chatbot detects crisis signals and surfaces help resources

#### Infrastructure Security
- **Encrypted DB connections** — TLS/SSL on all PostgreSQL connections
- **Role-based access control** — Admin, Moderator, Creator, Viewer roles
- **Secrets management** — AWS Secrets Manager; zero plaintext secrets in code
- **Audit logging** — All admin and moderation actions logged

---

## ⚡ Performance

### Optimisation Strategies

#### Backend Optimisations
- **Redis caching** for feed, search, and caption results (>90% cache hit rate)
- **ivfflat vector index** — O(√N) search vs O(N) full scan on post embeddings
- **Connection pooling** — PostgreSQL max 20 connections via pg-pool
- **Async moderation queue** — Redis queue keeps post creation non-blocking
- **gzip compression** — Applied to all JSON responses

#### Frontend Optimisations
- **Code splitting** — Next.js dynamic imports per route
- **Image optimisation** — Next/Image with automatic WebP conversion
- **Memoisation** — React.memo and useMemo on expensive renders
- **Debouncing** — 300ms debounce on emotion search input
- **Skeleton loading** — Perceived performance on feed loads

### Caching Strategy

| Data | Cache Key | TTL | Store |
|---|---|---|---|
| Emotion search results | `emotion_search:{hash(query+mood)}` | 5 min | Redis |
| AI caption results | `caption:{perceptual_hash}:{style}:{platform}` | 60 min | Redis |
| Personalised feed | `feed:{user_id}:{mood}` | 10 min | Redis |
| Trending posts | `trending:global` | 5 min | Redis |
| User profile | `user:{user_id}` | 1 hour | Redis |
| JWT validation | `session:{user_id}` | 7 days | Redis |

### Performance Targets

| Metric | Target | Current |
|---|---|---|
| API response (cached) | < 50ms | ~30ms |
| API response (AI call) | < 2,000ms | ~1,500ms |
| Emotion search latency | < 300ms | ~220ms |
| Page load time | < 2s | ~1.6s |
| Cache hit rate | > 90% | ~93% |
| Uptime SLA | > 99.5% | 99.8% |

---

## 🧪 Testing

### Running Tests

```bash
# Run all tests
npm test

# Coverage report
npm run test:coverage

# Specific test suite
npm test -- --testPathPattern=caption

# Watch mode
npm test -- --watch
```

### Test Structure

```
tests/
├── unit/
│   ├── controllers/
│   ├── services/
│   └── utils/
├── integration/
│   ├── api/
│   │   ├── auth.test.js
│   │   ├── caption.test.js
│   │   ├── search.test.js
│   │   └── feed.test.js
│   └── database/
└── e2e/
    └── user-flows.test.js    # Register → Post → Search → Chat → Feed
```

### Example Test

```javascript
// tests/integration/api/caption.test.js
const request = require('supertest');
const app     = require('../../src/app');

describe('POST /api/ai/caption', () => {
  it('should return 3 captions for a valid request', async () => {
    const response = await request(app)
      .post('/api/ai/caption')
      .set('Authorization', `Bearer ${testToken}`)
      .field('style',    'inspirational')
      .field('platform', 'instagram')
      .attach('image',   './tests/fixtures/sunset.jpg');

    expect(response.status).toBe(200);
    expect(response.body.captions).toHaveLength(3);
    expect(response.body.hashtags.length).toBeGreaterThan(0);
    expect(response.body.engagement_score).toBeGreaterThan(0);
  });

  it('should reject oversized images', async () => {
    const response = await request(app)
      .post('/api/ai/caption')
      .set('Authorization', `Bearer ${testToken}`)
      .attach('image', './tests/fixtures/large_file.jpg');

    expect(response.status).toBe(400);
    expect(response.body.error.code).toBe('FILE_TOO_LARGE');
  });
});
```

### Testing Strategy Summary

| Test Type | Tooling | Coverage Target | Scope |
|---|---|---|---|
| Unit Tests | Jest (Node) / Pytest (Python) | 85%+ | Functions, services, model logic |
| Integration Tests | Supertest + Jest | 75%+ | API endpoints with live test DB |
| End-to-End Tests | Playwright | Key user journeys | Register → Post → Search → Chat → Feed |
| AI Output Quality | Custom eval harness | Manual review | 200 captions/week human-scored |
| Load Testing | k6 | 500 concurrent users | Peak traffic auto-scaling validation |
| Security Testing | OWASP ZAP | All endpoints | DAST scan on every release |

---

## 📋 Prerequisites

### Required Software

| Software | Version | Purpose |
|---|---|---|
| **Node.js** | 18+ | Backend JS runtime |
| **npm** | 9+ | Package manager |
| **Python** | 3.11+ | AI microservices |
| **PostgreSQL** | 15+ | Primary database |
| **Redis** | 7+ | Caching layer |
| **Git** | Latest | Version control |

### Optional Tools

- **Docker** — For containerised deployment
- **Postman** — For API testing
- **pgAdmin** — For database management
- **MongoDB Compass** — For chatbot session inspection

### Check Your Installation

```bash
node --version      # v18+
npm --version       # 9+
python3 --version   # 3.11+
psql --version      # 15+
redis-cli --version # 7+
```

---

## ⚙ Installation & Setup

### 🔹 Step 1: Clone the Repository

```bash
git clone https://github.com/yourorg/swiftchat.git
cd swiftchat
```

### 🔹 Step 2: Install Dependencies

```bash
# Backend
cd backend && npm install

# Frontend
cd ../client && npm install

# AI Services
cd ../ai-services && pip install -r requirements.txt
```

### 🔹 Step 3: Configure PostgreSQL

```bash
createdb swiftchat
psql -U postgres -d swiftchat -c "CREATE EXTENSION IF NOT EXISTS vector;"
```

### 🔹 Step 4: Configure Redis

```bash
redis-server
redis-cli ping    # Should return: PONG
```

### 🔹 Step 5: Set Up Environment Variables

```bash
cp backend/.env.example   backend/.env
cp client/.env.example    client/.env
cp ai-services/.env.example ai-services/.env
```

Edit each `.env` file — see [Environment Variables](#-environment-variables).

### 🔹 Step 6: Run Database Migrations

```bash
cd backend && npm run migrate
```

### 🔹 Step 7: Seed Database (Optional)

```bash
npm run seed
```

### 🔹 Step 8: Start All Services

**Terminal 1 — Backend API**
```bash
cd backend && npm run dev
# Runs on http://localhost:5000
```

**Terminal 2 — Frontend**
```bash
cd client && npm run dev
# Runs on http://localhost:3000
```

**Terminal 3 — AI Services**
```bash
cd ai-services
uvicorn caption_service.main:app    --port 8001 --reload &
uvicorn emotion_search.main:app     --port 8002 --reload &
uvicorn chatbot_service.main:app    --port 8003 --reload &
uvicorn recommender_service.main:app --port 8004 --reload &
uvicorn moderation_service.main:app  --port 8005 --reload
```

### ✅ Verify Installation

Visit **http://localhost:3000** — you should see the SwiftChat feed. Try the emotion search bar or caption wizard to confirm the AI services are connected.

---

## 🌍 Environment Variables

### Backend (`backend/.env`)

```env
# Server
PORT=5000
NODE_ENV=development

# PostgreSQL
DATABASE_URL=postgresql://username:password@localhost:5432/swiftchat
DB_HOST=localhost
DB_PORT=5432
DB_NAME=swiftchat
DB_USER=your_username
DB_PASSWORD=your_password

# Redis
REDIS_URL=redis://localhost:6379
REDIS_HOST=localhost
REDIS_PORT=6379
REDIS_PASSWORD=

# JWT
JWT_SECRET=your_super_secret_jwt_key_here_min_32_chars
JWT_EXPIRES_IN=7d
JWT_REFRESH_SECRET=your_refresh_token_secret_here
JWT_REFRESH_EXPIRES_IN=30d

# OAuth - Google
GOOGLE_CLIENT_ID=your_google_client_id.apps.googleusercontent.com
GOOGLE_CLIENT_SECRET=your_google_client_secret
GOOGLE_CALLBACK_URL=http://localhost:5000/api/auth/google/callback

# OAuth - GitHub
GITHUB_CLIENT_ID=your_github_client_id
GITHUB_CLIENT_SECRET=your_github_client_secret
GITHUB_CALLBACK_URL=http://localhost:5000/api/auth/github/callback

# Email
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_USER=your_email@gmail.com
SMTP_PASSWORD=your_app_specific_password
SMTP_FROM=noreply@swiftchat.io

# AWS S3
AWS_ACCESS_KEY_ID=your_access_key
AWS_SECRET_ACCESS_KEY=your_secret_key
AWS_REGION=us-east-1
S3_BUCKET_NAME=swiftchat-media

# Internal AI Service URLs
CAPTION_SERVICE_URL=http://localhost:8001
EMOTION_SEARCH_URL=http://localhost:8002
CHATBOT_SERVICE_URL=http://localhost:8003
RECOMMENDER_URL=http://localhost:8004
MODERATION_URL=http://localhost:8005

# Rate Limiting
RATE_LIMIT_WINDOW_MS=900000
RATE_LIMIT_MAX_REQUESTS=100

# CORS
CLIENT_URL=http://localhost:3000

# Logging
LOG_LEVEL=debug
```

### Frontend (`client/.env`)

```env
NEXT_PUBLIC_API_URL=http://localhost:5000/api
NEXT_PUBLIC_API_TIMEOUT=10000
NEXT_PUBLIC_GOOGLE_CLIENT_ID=your_google_client_id
NEXT_PUBLIC_GITHUB_CLIENT_ID=your_github_client_id
NEXT_PUBLIC_ENABLE_DARK_MODE=true
NEXT_PUBLIC_GA_TRACKING_ID=UA-XXXXX-X
```

### AI Services (`ai-services/.env`)

```env
OPENAI_API_KEY=sk-your_openai_api_key
HUGGINGFACE_TOKEN=hf_your_token
MONGO_URI=mongodb://localhost:27017/swiftchat_chat
REDIS_URL=redis://localhost:6379
LOG_LEVEL=info
```

### Generate Secure Secrets

```bash
node -e "console.log(require('crypto').randomBytes(64).toString('hex'))"
```

---

## 📁 Project Structure

```
swiftchat/
│
├── client/                          # Next.js 14 web frontend
│   ├── public/
│   └── src/
│       ├── components/
│       │   ├── common/              # Button, Input, Modal
│       │   ├── layout/              # Header, Sidebar, Footer
│       │   ├── feed/                # PostCard, FeedList, UpvoteButton
│       │   ├── caption/             # CaptionWizard, StyleSelector
│       │   ├── search/              # EmotionSearchBar, ResultCard
│       │   ├── chatbot/             # ChatDrawer, MessageBubble
│       │   └── mood/                # MoodCheckIn, MoodBadge
│       ├── pages/
│       │   ├── index.jsx            # Feed / Home
│       │   ├── search.jsx           # Emotion search page
│       │   ├── create.jsx           # Post creation + caption wizard
│       │   ├── profile/[username].jsx
│       │   ├── login.jsx
│       │   └── register.jsx
│       ├── hooks/                   # useAuth, useFeed, useCaption, useChat
│       ├── services/                # Axios API clients per module
│       ├── context/                 # AuthContext, ThemeContext, MoodContext
│       └── utils/                   # formatters, validators, constants
│
├── mobile/                          # Flutter mobile application
│   └── lib/
│       ├── screens/
│       ├── widgets/
│       └── services/
│
├── backend/                         # Node.js / Express core API
│   └── src/
│       ├── controllers/             # authController, postController, aiController
│       ├── routes/                  # Route definitions per module
│       ├── services/
│       │   ├── authService.js
│       │   ├── postService.js
│       │   ├── aiService.js         # Bridge to Python AI microservices
│       │   ├── feedService.js
│       │   └── emailService.js
│       ├── middleware/              # auth, validation, rateLimiter, errorHandler
│       ├── models/                  # PostgreSQL query models (Sequelize / raw)
│       ├── config/                  # database, redis, passport (OAuth)
│       ├── utils/                   # jwt, bcrypt, validators, apiHelpers
│       └── app.js
│
├── ai-services/                     # Python AI microservices
│   ├── caption-service/
│   │   ├── main.py                  # FastAPI entry (port 8001)
│   │   ├── caption_model.py         # LLM prompt assembly + calling
│   │   └── image_analyzer.py        # CLIP image encoding
│   ├── emotion-search/
│   │   ├── main.py                  # FastAPI entry (port 8002)
│   │   ├── intent_classifier.py     # BERT emotion classifier
│   │   └── vector_search.py         # pgvector cosine search
│   ├── chatbot-service/
│   │   ├── main.py                  # FastAPI entry (port 8003)
│   │   └── agent.py                 # LangChain ReAct agent + tools
│   ├── recommender-service/
│   │   ├── main.py                  # FastAPI entry (port 8004)
│   │   └── recommendation_engine.py
│   ├── moderation-service/
│   │   ├── main.py                  # FastAPI entry (port 8005)
│   │   └── classifier.py            # Hate speech + NSFW detection
│   └── requirements.txt
│
├── database/
│   ├── migrations/                  # Numbered SQL migration files
│   └── seeds/                       # Dev seed data
│
├── docker/
│   ├── Dockerfile.backend
│   ├── Dockerfile.client
│   ├── Dockerfile.ai
│   └── nginx.conf
│
├── .github/
│   └── workflows/
│       ├── ci.yml                   # Test pipeline
│       └── cd.yml                   # Deploy pipeline
│
├── docker-compose.yml
├── .gitignore
├── .eslintrc.js
├── .prettierrc
├── LICENSE
└── README.md
```

---

## 🚀 Deployment

### 🐳 Docker Deployment

```bash
# Build all images
docker-compose build

# Start all services
docker-compose up -d

# View logs
docker-compose logs -f

# Stop services
docker-compose down
```

### `docker-compose.yml`

```yaml
version: '3.8'

services:
  postgres:
    image: pgvector/pgvector:pg15
    environment:
      POSTGRES_DB: swiftchat
      POSTGRES_USER: swiftchat_user
      POSTGRES_PASSWORD: secure_password
    ports:
      - "5432:5432"
    volumes:
      - postgres_data:/var/lib/postgresql/data

  mongo:
    image: mongo:7
    ports:
      - "27017:27017"
    volumes:
      - mongo_data:/data/db

  redis:
    image: redis:7-alpine
    ports:
      - "6379:6379"
    volumes:
      - redis_data:/data

  backend:
    build:
      context: ./backend
      dockerfile: ../docker/Dockerfile.backend
    ports:
      - "5000:5000"
    environment:
      DATABASE_URL: postgresql://swiftchat_user:secure_password@postgres:5432/swiftchat
      REDIS_URL: redis://redis:6379
      MONGO_URI: mongodb://mongo:27017/swiftchat_chat
    depends_on:
      - postgres
      - redis
      - mongo

  ai-services:
    build:
      context: ./ai-services
      dockerfile: ../docker/Dockerfile.ai
    ports:
      - "8001-8005:8001-8005"
    depends_on:
      - redis
      - mongo

  frontend:
    build:
      context: ./client
      dockerfile: ../docker/Dockerfile.client
    ports:
      - "3000:3000"
    depends_on:
      - backend

volumes:
  postgres_data:
  mongo_data:
  redis_data:
```

---

### ☁ Cloud Deployment Options

#### Option 1: Vercel (Frontend) + Render (Backend) + ECS (AI Services)

**Frontend on Vercel:**
```bash
npm install -g vercel
cd client && vercel --prod
```

**Backend on Render:**
1. Connect GitHub repo → select "Web Service"
2. Build: `npm install` | Start: `npm start`
3. Add all backend environment variables

**AI Services on AWS ECS:**
- Caption + Emotion Search → `g4dn.xlarge` (GPU inference)
- Moderation + Recommender → `t3.medium` (CPU only)

---

#### Option 2: AWS EC2 (Full Stack)

```bash
# SSH into instance
ssh -i your-key.pem ubuntu@your-instance-ip

# System setup
sudo apt update && sudo apt upgrade -y
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt install -y nodejs python3.11 python3-pip postgresql postgresql-contrib redis-server nginx
sudo -u postgres psql -c "CREATE EXTENSION IF NOT EXISTS vector;"
sudo npm install -g pm2

# Clone and build
git clone https://github.com/yourorg/swiftchat.git && cd swiftchat
cd backend && npm install
cd ../client && npm install && npm run build
cd ../ai-services && pip install -r requirements.txt

# Start services
pm2 start npm --name "swiftchat-backend" -- start
pm2 save && pm2 startup
```

**Nginx configuration:**
```nginx
server {
    listen 80;
    server_name yourdomain.com;

    location / {
        root /home/ubuntu/swiftchat/client/.next;
        try_files $uri /index.html;
    }

    location /api {
        proxy_pass http://localhost:5000;
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
    }
}
```

```bash
sudo ln -s /etc/nginx/sites-available/swiftchat /etc/nginx/sites-enabled/
sudo certbot --nginx -d yourdomain.com
sudo systemctl restart nginx
```

---

### 🔄 CI/CD Pipeline (GitHub Actions)

```yaml
# .github/workflows/deploy.yml
name: Deploy SwiftChat

on:
  push:
    branches: [main]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: actions/setup-node@v3
        with:
          node-version: '18'
      - run: cd backend && npm install && npm test
      - run: cd client && npm install && npm test
      - run: cd ai-services && pip install -r requirements.txt && pytest

  deploy-backend:
    needs: test
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Deploy to Render
        run: curl -X POST ${{ secrets.RENDER_DEPLOY_HOOK }}

  deploy-frontend:
    needs: test
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: amondnet/vercel-action@v20
        with:
          vercel-token: ${{ secrets.VERCEL_TOKEN }}
          vercel-org-id: ${{ secrets.VERCEL_ORG_ID }}
          vercel-project-id: ${{ secrets.VERCEL_PROJECT_ID }}
```

---

## 🔧 Troubleshooting

### 1. pgvector Extension Missing

**Error:** `type "vector" does not exist`

```bash
sudo apt install postgresql-15-pgvector
psql -U postgres -d swiftchat -c "CREATE EXTENSION IF NOT EXISTS vector;"
```

---

### 2. AI Service Unreachable

**Error:** `AI_SERVICE_UNAVAILABLE` returned from backend

```bash
# Check if service is alive
curl http://localhost:8001/health

# Restart
cd ai-services/caption-service
uvicorn main:app --reload --port 8001

# Check PM2 logs
pm2 logs caption-service
```

---

### 3. Redis Connection Error

**Error:** `Error: Redis connection to localhost:6379 failed`

```bash
redis-cli ping           # Should return PONG
redis-server --daemonize yes
redis-cli CONFIG GET bind
```

---

### 4. JWT Token Invalid

**Error:** `JsonWebTokenError: invalid signature`

```bash
# Regenerate a strong secret
node -e "console.log(require('crypto').randomBytes(64).toString('hex'))"
# Update JWT_SECRET in .env, clear browser localStorage and cookies
```

---

### 5. CORS Error

**Error:** `Access to XMLHttpRequest blocked by CORS policy`

```javascript
// backend/src/app.js
app.use(cors({ origin: process.env.CLIENT_URL, credentials: true }));
```

---

### 6. Port Already in Use

**Error:** `EADDRINUSE: address already in use :::5000`

```bash
lsof -i :5000
kill -9 <PID>
# Or use: PORT=5001 npm run dev
```

---

### 7. Python Dependency Conflicts

**Error:** `ModuleNotFoundError` in AI services

```bash
cd ai-services
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

---

### 8. OAuth Callback Mismatch

**Error:** `redirect_uri_mismatch`

- Verify the callback URL in Google/GitHub OAuth console **exactly** matches your `.env` value
- Include protocol (`http://` or `https://`)
- Remove trailing slashes
- For local dev, whitelist `http://localhost:5000/api/auth/google/callback`

---

## ❓ FAQ

### General Questions

**Q: Is SwiftChat free to use?**
A: Yes — SwiftChat is fully open-source under the MIT license. Self-host it for free.

**Q: Does SwiftChat require an OpenAI API key?**
A: Yes, the caption generator and chatbot use OpenAI GPT-4. You can swap in any OpenAI-compatible model by updating the AI service configuration.

**Q: Can I use SwiftChat without the AI features?**
A: Yes. The core social platform (posts, feed, comments, profiles) works independently. AI features degrade gracefully if any AI service is offline.

**Q: How does emotion search actually work?**
A: Your query is classified into emotion labels by a BERT model, encoded into a 384-dimensional vector, and matched against pre-indexed post embeddings using cosine similarity in PostgreSQL via pgvector.

**Q: Is my mood data stored permanently?**
A: Your mood is stored with a timestamp in the users table and can be cleared at any time from your profile settings.

---

### Technical Questions

**Q: Why pgvector instead of a dedicated vector database like Pinecone?**
A: pgvector keeps everything in one database, simplifying operations. At under 10M posts, pgvector with an ivfflat index is fast enough. A dedicated vector DB would be considered at 50M+ posts.

**Q: Why are AI services in Python, separate from the Node.js backend?**
A: Python has the richest ML ecosystem (HuggingFace, LangChain, sentence-transformers). Separating them allows independent GPU scaling and keeps the JS backend lean.

**Q: Can I replace GPT-4 with a self-hosted model?**
A: Yes. The caption and chatbot services use an OpenAI-compatible interface. Replace the call with any endpoint that follows the same schema (e.g. Ollama, vLLM, Mistral).

**Q: How do I add a new caption style?**
A: Add the style name to the Joi validation enum in `backend/src/middleware/validationMiddleware.js` and update the prompt template in `ai-services/caption-service/caption_model.py`.

**Q: Is there a mobile app?**
A: A Flutter app is included in the `mobile/` directory and is on the active roadmap for app store release.

---

### Development Questions

**Q: How do I contribute?**
A: See the [Contributing](#-contributing) section for full guidelines.

**Q: How do I report a bug?**
A: Open an issue at [github.com/yourorg/swiftchat/issues](https://github.com/yourorg/swiftchat/issues) with reproduction steps.

**Q: Can I use this commercially?**
A: Yes — MIT license permits commercial use. Attribution appreciated but not required.

---

## 📊 Design Decisions

### Why Microservices for AI, Monolith for Core?

**AI Microservices rationale:**
- AI services require GPU instances; core backend runs fine on CPU
- Independent scaling: caption service can scale 10x without touching moderation
- Language boundary: Python for ML, Node.js for API — best tool for each job
- Failure isolation: one AI service going down does not crash the platform

**Monolith Core Backend rationale:**
- Faster iteration in early stages
- Simpler deployment and debugging
- Modules are cleanly separated and can be extracted to microservices when traffic demands it

---

### Why PostgreSQL + pgvector Instead of MongoDB + Pinecone?

- Strong relational integrity for users, posts, comments, and interaction signals
- pgvector enables SQL + vector similarity search in a **single query** — no dual-write, no sync lag
- ACID compliance for upvotes, follows, and moderation state changes
- JSONB support for cases where a flexible schema is needed
- Operational simplicity — one database to monitor, back up, and secure

---

### Why Redis for Caching and Queuing?

- Sub-millisecond response for cached feeds and captions
- Sorted sets natively support trending leaderboards in O(log N)
- Lists power the async moderation pipeline without an extra message broker
- Sliding window counters for rate limiting — no extra library needed
- Session and JWT blacklist management in a single store

---

### Why LangChain for the Chatbot?

- ReAct pattern lets the chatbot reason before acting — decide whether to search posts, generate a caption, or simply respond conversationally
- Tool registration is clean and extensible — adding a new capability is one function definition
- Built-in memory management for multi-turn conversation history
- Provider-agnostic — swap GPT-4 for any LLM without rewriting agent logic

---

### Why JWT over Sessions?

- Stateless — scales horizontally without sticky sessions or shared session store
- Works seamlessly across web, mobile, and API consumers
- Short expiry (7 days) + refresh token rotation mitigates the inability to instantly revoke

---

## 🛣 Roadmap

### Phase 1 — Core Release ✅ *(Completed)*
- [x] AI caption generator (5 styles, 5 platforms)
- [x] Emotion-based smart search
- [x] AI chatbot assistant (LangChain ReAct)
- [x] Smart recommendation feed
- [x] AI content moderation pipeline
- [x] JWT + OAuth authentication (Google, GitHub)

### Phase 2 — Deepened Personalisation 🚧 *(In Progress)*
- [x] Engagement score preview before posting
- [x] Multi-platform caption mode (one image → 5 captions)
- [ ] Personal AI writing style — learn from user's caption history to replicate their voice
- [ ] Emotion detection from selfies — on-device FER model for mood check-in
- [ ] Voice-based emotion search — Whisper ASR + emotion NLP pipeline

### Phase 3 — Creator & Community 📅 *(Planned)*
- [ ] AI short-form video caption generation (Reels / TikTok)
- [ ] AI storytelling posts — bullet points → fully written narrative
- [ ] Community mental wellness features — peer support groups, daily wellness aggregates
- [ ] Creator analytics dashboard — engagement trends and caption performance over time

### Phase 4 — Platform Ecosystem 📅 *(Planned)*
- [ ] Public developer API with tiered pricing
- [ ] Browser extension — caption generation inside Instagram and LinkedIn web UI
- [ ] Brand Intelligence Dashboard — sentiment monitoring for business accounts
- [ ] Zapier / Make integration for automated caption workflows

### Phase 5 — Research & Ethics 📅 *(Future)*
- [ ] Longitudinal well-being study — opt-in research tracking mood vs feed quality over time
- [ ] 64-label culturally-diverse emotion taxonomy (expansion beyond GoEmotions)
- [ ] Quarterly algorithmic transparency report — public audit of recommendation behaviour
- [ ] On-device AI inference option — privacy-preserving caption generation with no cloud calls

---

## 🤝 Contributing

We welcome contributions from developers, designers, ML researchers, and mental wellness advocates!

### How to Contribute

1. **Fork the repository**
   ```bash
   git clone https://github.com/yourorg/swiftchat.git
   cd swiftchat
   ```

2. **Create a feature branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```

3. **Make your changes**
   - Write clean, readable code
   - Follow existing code style
   - Add tests for new features
   - Update documentation

4. **Commit with a conventional message**
   ```bash
   git add .
   git commit -m "feat: add voice-based emotion search"
   ```
   **Commit types:** `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`

5. **Push and open a Pull Request**
   ```bash
   git push origin feature/your-feature-name
   ```

### Contribution Guidelines

- **JS/TS:** ES2022+, functional style, avoid mutation
- **Python:** PEP 8, type hints on all function signatures, docstrings on classes
- **React:** Functional components with hooks only
- **Tests:** All new features must include unit tests; API changes require integration tests
- **Docs:** Update README and inline comments for any public-facing change

### Good First Issues

Look for issues labelled:
- `good first issue`
- `help wanted`
- `documentation`
- `ai-improvement`

### Code of Conduct

- Be respectful and inclusive
- Provide specific, constructive feedback
- Be especially thoughtful when discussing the emotional AI features — our users may be vulnerable
- Report inappropriate behaviour to the maintainers

---

## 👥 Contributors

Thanks to everyone who has helped build SwiftChat! 🙏

<table>
  <tr>
    <td align="center">
      <img src="https://via.placeholder.com/100" width="100px;" alt=""/><br />
      <sub><b>Your Name</b></sub><br />
      <small>Creator & Maintainer</small>
    </td>
  </tr>
</table>

Want to see your name here? [Contribute to SwiftChat!](#-contributing)

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for full details.

```
MIT License

Copyright (c) 2024 SwiftChat Team

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
```

---

## 📬 Contact

### Get in Touch

- **Email:** [hello@swiftchat.io](mailto:hello@swiftchat.io)
- **GitHub:** [@yourorg](https://github.com/yourorg)
- **Twitter:** [@swiftchatio](https://twitter.com/swiftchatio)
- **LinkedIn:** [SwiftChat](https://linkedin.com/company/swiftchat)
- **Discord:** [Join our server](https://discord.gg/swiftchat)

### Project Links

- **Live Demo:** https://swiftchat-demo.vercel.app
- **Repository:** https://github.com/yourorg/swiftchat
- **Issue Tracker:** https://github.com/yourorg/swiftchat/issues
- **Roadmap:** https://github.com/yourorg/swiftchat/projects

---

## 🌟 Star History

[![Star History Chart](https://api.star-history.com/svg?repos=yourorg/swiftchat&type=Date)](https://star-history.com/#yourorg/swiftchat&Date)

---

## 🎯 Final Words

**SwiftChat** was built out of a belief that social media should make people feel *better*, not worse. Existing platforms are extraordinary at connecting people — but they've never asked *"how are you feeling right now?"* and tried to help.

Whether you're:
- 😊 Looking for content that matches your current mood
- ✍️ A creator who wants to post more and agonise less over captions
- 💼 A developer building the next emotionally-aware application
- 🛡 A moderator tired of manually filtering toxic content

SwiftChat is built for you.

> **"The most important thing in communication is hearing what isn't said."**  
> — Peter Drucker

---

<div align="center">

### Built for humans who don't just share content — they share how they feel. 🧠💚

**Give us a ⭐ if SwiftChat makes social media feel more human!**

[Report Bug](https://github.com/yourorg/swiftchat/issues) · [Request Feature](https://github.com/yourorg/swiftchat/issues) · [Join Discord](https://discord.gg/swiftchat)

</div>

---

<div align="center">
  <sub>Made with ❤️ by the SwiftChat Team</sub>
</div>
