# SwiftChat
## AI-Powered Smart Social Media Platform

> **Production-Grade Technical Documentation | v1.0.0**
> Open Source · MIT License · Built for Developers, Contributors & Reviewers

---

| | | |
|:---:|:---:|:---:|
| 🧠 **Emotion-Aware AI** | 🎯 **Smart Recommendations** | 💚 **Mental-Wellness First** |

---

## 📌 Table of Contents

1. [Project Overview](#1-project-overview)
2. [Problem Statement](#2-problem-statement)
3. [Proposed Solution](#3-proposed-solution)
4. [Key Feature Breakdown](#4-key-feature-breakdown)
5. [AI System Design](#5-ai-system-design)
6. [System Architecture](#6-system-architecture)
7. [Request Flow Examples](#7-request-flow-examples)
8. [Database Design](#8-database-design)
9. [API Documentation](#9-api-documentation)
10. [Project Folder Structure](#10-project-folder-structure)
11. [Performance Considerations](#11-performance-considerations)
12. [Security Design](#12-security-design)
13. [Deployment Architecture](#13-deployment-architecture)
14. [Testing Strategy](#14-testing-strategy)
15. [Future Roadmap](#15-future-roadmap)

---

## 1. Project Overview

### 1.1 Concept & Product Vision

SwiftChat is an AI-integrated social networking platform that redefines how people discover, share, and interact with content online. Unlike traditional platforms that rely solely on hashtags, follower graphs, or engagement-driven algorithms, SwiftChat introduces a fourth dimension to content discovery: **human emotion**.

The platform embeds four distinct AI systems — a caption generator, a conversational chatbot assistant, an emotion-based search engine, and a personalised recommendation engine — directly into the core social experience. The result is a platform that does not just serve content, but understands *why* a user wants it and *how* it might make them feel.

The product vision is to build the **first truly emotionally intelligent social media ecosystem**: one that reduces doomscrolling, supports mental well-being, and empowers users to create better content with less effort.

---

### 1.2 Target Users

| User Segment | Primary Need | How SwiftChat Helps |
|---|---|---|
| Everyday Social Users | Relevant, mood-matched content | Emotion-based search & smart feed |
| Content Creators | Engaging captions quickly | AI caption & hashtag generator |
| Mental Wellness Seekers | Uplifting, curated content | Mood-aware recommendation engine |
| Developers / API Consumers | Programmatic AI features | REST / GraphQL API access |
| Community Moderators | Safe, toxic-free spaces | AI content moderation layer |

---

### 1.3 Real-World Problem Being Solved

Social media reaches over **5 billion people** globally. Yet despite this scale, the platforms most people use daily were not designed with emotional intelligence in mind. The core discovery mechanisms — hashtags, engagement loops, and popularity signals — optimise for *time-on-platform* rather than *user well-being*.

SwiftChat proposes an architectural shift: **emotion and context should be first-class inputs to content delivery.**

---

## 2. Problem Statement

### 2.1 Limitations of Current Social Platforms

#### 🔍 Hashtag-Dependent Discovery
Content discovery is almost entirely dependent on hashtags and keyword matching. A user who opens an app feeling anxious and wanting calming content cannot simply express that need — they must know and type the right hashtag. This creates a friction-filled, imprecise experience that rarely surfaces the content most relevant to the user's emotional state.

#### ✍️ Caption Creativity Barrier
Creating high-quality, engaging captions requires copywriting skill that most users do not have. Studies show the average user spends **5–10 minutes** deliberating over a single post caption. This friction reduces posting frequency and content quality, especially for non-native language speakers.

#### 😔 Mental Health Impact
Algorithmic feeds prioritise content that maximises engagement — which frequently means emotionally polarising, anxiety-inducing, or outrage-driven material. There is no mechanism for users to express *"I need something uplifting right now"* and receive a curated, contextually appropriate response.

#### 🤖 Lack of AI Interactivity
Despite billions of dollars of AI investment in the industry, most social platforms offer no interactive AI assistance to the average user. AI operates silently in recommendation algorithms but is never exposed as a collaborative tool.

---

### 2.2 Pain Point Comparison

| Pain Point | Current Platform Behaviour | SwiftChat Solution |
|---|---|---|
| Content discovery | Keyword/hashtag only | Emotion + intent-aware NLP search |
| Caption creation | Manual, time-consuming | One-click AI caption generation |
| Mental health impact | Engagement-maximising feeds | Mood-matched, wellness-aware curation |
| Toxic content | Reactive human moderation | Proactive AI moderation pipeline |
| User assistance | No AI interaction layer | Embedded conversational AI chatbot |

---

## 3. Proposed Solution

### 3.1 System Overview

SwiftChat is an AI-integrated social networking platform built on a **microservices architecture**. The core backend orchestrates four independently deployable AI services, each responsible for a distinct intelligent behaviour. All AI services communicate with the main backend via an internal service mesh, keeping concerns cleanly separated and independently scalable.

---

### 3.2 How the System Solves Each Problem

| Problem | AI Module | Mechanism |
|---|---|---|
| Hashtag-only discovery | Emotion Search Engine | NLP + sentiment analysis on post content + image emotion recognition |
| Caption writer's block | AI Caption Generator | LLM prompt engineering with image CLIP encoding |
| Engagement-toxic feeds | Smart Recommendation Engine | Mood + time-of-day + interaction history weighting |
| Toxic / harmful content | AI Content Moderator | Multi-model classifier: hate speech, toxicity, NSFW detection |
| No AI interactivity | AI Chatbot Assistant | LangChain-powered conversational agent with platform-aware context |

---

### 3.3 High-Level Workflow

1. User opens the app; ambient mood detection prompts optional mood check-in
2. User's mood state is stored in session context and influences all downstream AI decisions
3. Feed is populated by the recommendation engine using mood + interaction history
4. User uploads a post; AI caption generator offers real-time suggestions
5. All incoming posts pass through the AI content moderation pipeline before publication
6. User performs an emotion-based search; NLP engine returns mood-matched results
7. AI chatbot is available throughout for assistance, creative ideas, or conversation

---

## 4. Key Feature Breakdown

### 4.1 AI Caption Generator

#### Overview
The caption generator removes creative friction from the posting experience. A user uploads an image or describes a post, selects a tone/style, and receives multiple professionally written caption options with suggested hashtags — in under two seconds.

#### Supported Caption Styles

| Style | Description | Ideal Use Case |
|---|---|---|
| Funny | Humorous, playful, light-hearted | Pet photos, food fails, candid moments |
| Motivational | Achievement-forward, empowering | Fitness, work milestones, personal growth |
| Romantic | Warm, emotional, love-forward language | Couple photos, anniversaries, sunsets |
| Inspirational | Reflective, philosophical, uplifting | Nature, travel, quiet moments |
| Storytelling | Narrative arc, hooks the reader | Travel journals, personal experiences |

#### Internal Mechanism

1. Image is encoded via a **CLIP** vision model to produce a semantic embedding
2. Top scene/object/mood tags are extracted from the embedding
3. A structured prompt is assembled with image tags + user-selected style
4. LLM (GPT-4 / equivalent) generates 3 caption variants + hashtag suggestions
5. Output is post-processed, sanitised, and returned to the frontend

#### Example

```
Input:   Sunset beach photo  |  Style: Inspirational

Output 1: "Chasing sunsets and peaceful moments 🌅"
Output 2: "The sky painted poetry tonight."
Output 3: "Every sunset is a reminder that endings can be beautiful."

Hashtags: #sunset #goldenhour #peace #travel #nature
```

#### Edge Cases
- **Blurry / unrecognisable images** → fallback to text-only prompt asking user for a brief description
- **Sensitive image content** → flagged by moderation layer before caption generation begins
- **Non-English language preference** → style prompt adapted to user's locale setting

---

### 4.2 AI Chatbot Assistant

#### Overview
The embedded AI chatbot is a **LangChain-powered conversational agent** that operates with full awareness of platform context. It is not a generic chat interface — it has access to the user's post history, followed topics, and current mood state, enabling responses that are genuinely personalised.

#### Capabilities

| Capability | Example Interaction |
|---|---|
| Caption writing assistance | User: "Caption for a hiking post" → AI: "The mountains called. I answered. ⛰️" |
| Post discovery suggestions | User: "Show me something funny" → AI surfaces top-upvoted comedy posts |
| Creative idea prompting | User: "What should I post today?" → AI suggests based on trends + mood |
| Emotional support conversation | User: "I feel lonely today" → AI engages empathetically, suggests uplifting content |
| Platform navigation help | User: "How do I save a post?" → AI provides step-by-step guidance |

#### LangChain Architecture

The chatbot uses a **ReAct (Reasoning + Acting)** agent pattern with the following tools registered in its tool chain:

- `PostSearchTool` — searches the platform database by emotion/tag/keyword
- `CaptionGeneratorTool` — delegates to the caption microservice
- `UserContextTool` — fetches the current user's mood, history, and preferences
- `TrendingTopicsTool` — queries the trending topics service

#### Edge Cases
- **User expresses distress or crisis signals** → chatbot surfaces mental health resources and disengages from normal assistant mode
- **Ambiguous queries** → chatbot asks a single clarifying question before acting
- **Unsupported languages** → chatbot responds in the same language the user writes in, leveraging LLM multilingual capability

---

### 4.3 Emotion-Based Smart Search

#### Overview
This is SwiftChat's most differentiated feature. Rather than requiring users to know the right hashtag or keyword, the emotion search engine accepts **free-text emotional expressions** and maps them to relevant content using a multi-model NLP pipeline.

#### Internal Mechanism

```
User Input: "I want something calming and uplifting"

Step 1: Intent Classification
        → Primary emotion: calm (0.87), joy (0.72)
        → Content type preference: visual, quotes

Step 2: Semantic Embedding
        → Encode query into dense vector via sentence-transformer

Step 3: Post Retrieval
        → Vector similarity search against pre-indexed post embeddings
        → Filter by emotion_tags: ['calm', 'uplifting', 'peaceful']

Step 4: Image Emotion Re-ranking
        → Posts with images re-scored by visual emotion model

Step 5: Return ranked results
        → Motivational videos, positive quotes,
           calm nature photography, uplifting stories
```

#### NLP Pipeline Components

| Component | Model / Tool | Purpose |
|---|---|---|
| Intent Classifier | Fine-tuned BERT (GoEmotions dataset) | Map raw query to emotion categories |
| Semantic Encoder | sentence-transformers/all-MiniLM-L6-v2 | Encode query + posts as dense vectors |
| Vector Search | pgvector (PostgreSQL extension) | Efficient cosine similarity search at scale |
| Image Emotion Model | EfficientNet fine-tuned on emotion dataset | Re-rank posts containing images |
| Sentiment Analyser | VADER + custom lexicon | Score caption text sentiment polarity |

#### Search Query → Result Mapping

| Search Query | Detected Emotion(s) | Returned Content Types |
|---|---|---|
| "Make me happy" | joy, amusement | Funny memes, cute pet videos, positive quotes |
| "I need motivation" | determination, hope | Fitness journeys, success stories, motivational clips |
| "Something calming" | calmness, serenity | Nature photography, meditation content, soft music |
| "Sad relatable posts" | sadness, nostalgia | Reflective writing, melancholic art, relatable comics |
| "I feel lonely" | loneliness, longing | Community posts, warmth-focused content, chat prompts |

#### Edge Cases
- **Emotionally ambiguous queries** ("I don't know how I feel") → system defaults to a balanced, positive-leaning feed
- **Potentially harmful search intent** → moderation layer intercepts and redirects to wellness resources
- **Very rare emotion labels** → fallback to closest semantic neighbour in the emotion taxonomy

---

### 4.4 Smart Recommendation System

#### Overview
The recommendation engine moves beyond engagement-maximisation to deliver content that is both **relevant** and **emotionally appropriate**. It is a hybrid system combining collaborative filtering (what similar users engaged with) and content-based filtering (what matches the current user's mood and interests).

#### Recommendation Signals

| Signal | Weight | Description |
|---|---|---|
| Current mood state | High | User's checked-in or inferred mood from recent activity |
| Time of day | Medium | Morning → motivational; night → calming/reflective content |
| Interaction history | High | Posts liked, saved, shared, and time-spent reading |
| Topic preferences | Medium | Followed topics, frequent search themes |
| Trending content | Low | Platform-wide trending, filtered by emotion compatibility |
| Social graph | Medium | Content popular within the user's follow network |

#### Edge Cases
- **New users (cold start)** → initialised with a mood check-in survey; onboarding feed populated from popular content in selected interest categories
- **Mood conflict** (user says "happy" but interaction history shows sadness signals) → system blends both signals with recency weighting

---

### 4.5 AI Content Moderation

#### Overview
Every piece of user-generated content — captions, comments, images, and videos — passes through an automated moderation pipeline before becoming visible to other users. The system operates in near-real-time and escalates borderline content to human reviewers.

#### Moderation Pipeline

```
Incoming Content
      |
      v
Text Classifier (hate speech / toxicity / spam)
      |
      v
Image / Video Classifier (NSFW / violence / graphic)
      |
      v
┌──────────────────────────────────────────────────────┐
│  SAFE        (confidence > 0.95)  →  Published        │
│  BORDERLINE  (0.60 – 0.95)        →  Human review     │
│  UNSAFE      (confidence > 0.95)  →  Auto-rejected    │
└──────────────────────────────────────────────────────┘
```

---

## 5. AI System Design

### 5.1 AI Architecture Overview

```
┌─────────────────────────────────────────────────────────────┐
│                     AI SERVICE LAYER                        │
│                                                             │
│  ┌──────────────────┐    ┌──────────────────────────────┐  │
│  │ Caption Service  │    │   Emotion Search Engine      │  │
│  │ (FastAPI/Python) │    │   (FastAPI + pgvector)       │  │
│  └──────────────────┘    └──────────────────────────────┘  │
│                                                             │
│  ┌──────────────────┐    ┌──────────────────────────────┐  │
│  │ Chatbot Service  │    │  Recommendation + Moderation │  │
│  │ (LangChain)      │    │  Engine (Python microservice)│  │
│  └──────────────────┘    └──────────────────────────────┘  │
└─────────────────────────────────────────────────────────────┘
         |                               |
         └──── Internal gRPC / REST ─────┘
                        |
             Node.js / Django Backend
```

---

### 5.2 Prompt Engineering Strategy

All LLM-powered features use a structured, multi-variable prompt template. System prompts establish the model's role and constraints; user prompts inject dynamic context derived from image analysis, mood state, and user preferences.

```
SYSTEM:
You are an expert social media copywriter embedded in an emotionally-aware
social platform. Always write content that is uplifting, authentic, and
platform-appropriate. Never generate harmful, discriminatory, or misleading content.

USER:
  Image Analysis:
    - Scene:          {scene}
    - Objects:        {objects}
    - Detected Mood:  {image_mood}

  User Context:
    - Current Mood:       {user_mood}
    - Style Preference:   {style}
    - Target Platform:    {platform}
    - Language:           {locale}

  Task:
    Generate 3 caption variants in the '{style}' style for {platform}.
    Each caption must be under {char_limit} characters.
    Append 5–8 relevant hashtags.

  Output Format (JSON):
    { "captions": [string, string, string], "hashtags": [string] }
```

---

### 5.3 Model Interaction Flow

| Feature | Models Used | Input | Output |
|---|---|---|---|
| Caption Generation | CLIP + GPT-4 | Image + style + platform | 3 captions + hashtags |
| Emotion Search | BERT + sentence-transformers | Free-text query | Ranked post list |
| Chatbot | LangChain ReAct + GPT-4 | Conversation history + user context | Conversational response |
| Recommendation | Collaborative filter + mood model | User history + mood + time | Ranked post feed |
| Moderation | Fine-tuned BERT + EfficientNet | Text + image | Safe / Review / Reject label |

---

## 6. System Architecture

### 6.1 Architecture Diagram

```
┌───────────────────────────────────────────────────────────┐
│                    CLIENT LAYER                           │
│    React / Next.js  |  Tailwind CSS  |  Flutter (mobile)  │
└────────────────────────────┬──────────────────────────────┘
                             │  HTTPS / WebSocket
┌────────────────────────────▼──────────────────────────────┐
│                   API GATEWAY                             │
│          Rate Limiting | Auth | Routing | Logging         │
└───────────────┬────────────────────────┬──────────────────┘
                │                        │
┌───────────────▼───────┐    ┌───────────▼──────────────────┐
│   Node.js / Django    │    │     AI Service Mesh          │
│   (Core Backend API)  │    │  Caption | Search | Chatbot  │
│   REST + GraphQL      │    │  Recommender | Moderator     │
└───────┬───────────────┘    └───────────┬──────────────────┘
        │                                │
┌───────▼───────────────┐   ┌────────────▼─────────────────┐
│  PostgreSQL (pgvector) │   │  OpenAI / HuggingFace APIs  │
│  MongoDB               │   │  LangChain Agent Runtime    │
│  Redis Cache           │   │  Sentence-Transformers      │
└───────────────────────┘   └─────────────────────────────┘
```

---

### 6.2 Layer-by-Layer Explanation

#### Frontend Layer
The web frontend is a **Next.js** application with server-side rendering for SEO and fast initial load. Tailwind CSS provides utility-first styling. For native mobile experiences, a **Flutter** application mirrors the core feature set. Both clients communicate with the backend over HTTPS REST (for data operations) and WebSocket (for real-time chat and notifications).

#### Backend Layer
The core backend can be implemented in either **Node.js (Express)** or **Python (Django)**, both of which expose a unified API. The backend is responsible for user authentication, post CRUD operations, orchestrating calls to AI microservices, and serving the social graph. GraphQL is offered alongside REST to allow frontend clients to fetch precisely the data they need.

#### AI Service Layer
Each AI capability is packaged as an independent **Python FastAPI microservice**. Services communicate with the core backend via internal REST or gRPC. This decoupling means the caption generator can be scaled to GPU nodes independently of the moderation service running on CPU nodes.

#### Database Layer
- **PostgreSQL + pgvector** — primary relational store + vector similarity search for emotion search
- **MongoDB** — flexible document store for post metadata, AI analysis results, and chatbot session state
- **Redis** — session caching, rate limit counters, trending topic rankings, and real-time notification queues

---

## 7. Request Flow Examples

### 7.1 Emotion-Based Search Flow

```
1.  User types: "I want something uplifting"
2.  POST /api/search/emotion
    { "query": "I want something uplifting", "mood": "neutral" }

3.  API Gateway: validates JWT, checks rate limit
4.  Backend forwards query to Emotion Search microservice

5.  Search service:
    a. BERT classifier → emotions: [joy: 0.82, hope: 0.75]
    b. sentence-transformer encodes query → 384-dim vector
    c. pgvector cosine search against post embeddings (top-50)
    d. EfficientNet re-ranks image posts by visual positivity

6.  Backend fetches full post objects from PostgreSQL for top-20 results
7.  Results cached in Redis (key: hash(query+mood), TTL=300s)
8.  200 OK returned with ranked post list
```

---

### 7.2 Caption Generation Flow

```
1.  User uploads image, selects style "Motivational", platform "Instagram"
2.  POST /api/ai/caption
    { image: <file>, style: "motivational", platform: "instagram" }

3.  Backend uploads image to S3, retrieves signed URL
4.  Backend sends { image_url, style, platform } to Caption microservice

5.  Caption service:
    a. CLIP model encodes image → scene tags: ["mountain", "sunrise", "sky"]
    b. Prompt assembled with tags + style + platform constraints
    c. GPT-4 called → 3 caption variants + 7 hashtag suggestions returned

6.  Result stored in PostgreSQL (ai_caption_cache table)
7.  Result cached in Redis (key: perceptual_hash:style:platform, TTL=3600s)
8.  200 OK returned to frontend
```

---

### 7.3 Cache Hit Flow

```
1.  User submits similar query with same mood context
2.  Backend computes hash(query + mood)
3.  Redis lookup: key = emotion_search:{hash}
4.  CACHE HIT → return cached response instantly (< 30ms)
5.  No AI service call made, no LLM cost incurred
```

---

## 8. Database Design

### 8.1 Table: users

```sql
CREATE TABLE users (
  id              UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  username        VARCHAR(50)  NOT NULL UNIQUE,
  email           VARCHAR(255) NOT NULL UNIQUE,
  password_hash   TEXT         NOT NULL,
  display_name    VARCHAR(100),
  avatar_url      TEXT,
  bio             TEXT,
  current_mood    VARCHAR(50),          -- updated by mood check-in
  mood_updated_at TIMESTAMPTZ,
  created_at      TIMESTAMPTZ  NOT NULL DEFAULT NOW()
);

CREATE INDEX idx_users_email ON users(email);
CREATE INDEX idx_users_mood  ON users(current_mood);
```

---

### 8.2 Table: posts

```sql
CREATE TABLE posts (
  id                UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  user_id           UUID REFERENCES users(id) ON DELETE CASCADE,
  caption           TEXT,
  media_url         TEXT,
  media_type        VARCHAR(10) CHECK (media_type IN ('image','video','text')),
  emotion_tags      TEXT[],              -- AI-assigned emotion labels
  sentiment_score   FLOAT,               -- -1.0 (negative) to 1.0 (positive)
  embedding         vector(384),         -- sentence-transformer embedding for search
  moderation_status VARCHAR(20) DEFAULT 'pending',  -- pending/approved/rejected
  is_public         BOOLEAN     NOT NULL DEFAULT TRUE,
  created_at        TIMESTAMPTZ NOT NULL DEFAULT NOW()
);

CREATE INDEX idx_posts_user_id      ON posts(user_id);
CREATE INDEX idx_posts_emotion_tags ON posts USING GIN(emotion_tags);
CREATE INDEX idx_posts_embedding    ON posts USING ivfflat(embedding vector_cosine_ops);
CREATE INDEX idx_posts_sentiment    ON posts(sentiment_score);
```

---

### 8.3 Table: comments

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
```

---

### 8.4 Table: user_interactions (for recommendations)

```sql
CREATE TABLE user_interactions (
  id                UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  user_id           UUID REFERENCES users(id) ON DELETE CASCADE,
  post_id           UUID REFERENCES posts(id) ON DELETE CASCADE,
  interaction_type  VARCHAR(20) CHECK (
                      interaction_type IN ('like','save','share','view','skip')
                    ),
  time_spent_ms     INTEGER,
  created_at        TIMESTAMPTZ NOT NULL DEFAULT NOW()
);

CREATE INDEX idx_interactions_user_id ON user_interactions(user_id);
CREATE INDEX idx_interactions_post_id ON user_interactions(post_id);
```

---

### 8.5 Design Decisions

| Decision | Rationale |
|---|---|
| pgvector for embeddings | Stores post embeddings in Postgres, enabling SQL + vector search in a single query |
| emotion_tags as TEXT[] | Array column with GIN index supports fast "emotion contains X" filtering |
| MongoDB for chatbot sessions | Flexible schema suits variable-length conversation histories |
| Redis for trending topics | Sorted sets (ZRANGEBYSCORE) natively support leaderboard queries in O(log N) |
| Separate user_interactions table | Decouples engagement signals from post data; enables recommendation model retraining |

---

## 9. API Documentation

### 9.1 Authentication

All protected endpoints require a **JWT Bearer token**. Tokens are issued on login and expire after **7 days**. Refresh tokens (30-day TTL) are stored in HttpOnly cookies.

```
Authorization: Bearer eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9...
```

---

### 9.2 POST `/api/search/emotion`

Performs an emotion-based search and returns ranked posts matching the user's expressed emotional intent.

**Request**
```json
POST /api/search/emotion
Content-Type: application/json
Authorization: Bearer <token>

{
  "query":   "I want something calming",
  "mood":    "anxious",
  "limit":   20,
  "offset":  0
}
```

**Response — 200 OK**
```json
{
  "results": [
    {
      "post_id":         "a1b2c3d4-...",
      "caption":         "Breathe. Everything will be okay.",
      "media_url":       "https://cdn.emotisocial.io/posts/abc.jpg",
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
| 500 | `EMOTION_ENGINE_UNAVAILABLE` | AI search service is unreachable |

---

### 9.3 POST `/api/ai/caption`

Generates AI captions for an uploaded image or text description.

**Request**
```
POST /api/ai/caption
Content-Type: multipart/form-data
Authorization: Bearer <token>

{
  "image":       <file>,            // Optional. JPG/PNG/WEBP. Max 10MB
  "description": "Hiking trip",    // Optional if no image provided
  "style":       "inspirational",
  "platform":    "instagram",
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
  "hashtags":   ["#hiking", "#mountains", "#adventure", "#nature", "#explore"],
  "image_tags": ["mountain", "trail", "sunrise", "outdoor", "landscape"]
}
```

**Error Responses**

| Status | Error Code | Description |
|---|---|---|
| 400 | `INVALID_STYLE` | Style is not in the supported list |
| 400 | `FILE_TOO_LARGE` | Image exceeds the 10MB file size limit |
| 422 | `IMAGE_UNSAFE` | Image flagged by content moderation |
| 429 | `RATE_LIMIT_EXCEEDED` | Caption generation limited to 50/hour |
| 500 | `CAPTION_SERVICE_UNAVAILABLE` | AI caption service is unreachable |

---

### 9.4 GET `/api/feed`

Returns the personalised recommendation feed for the authenticated user.

**Request**
```
GET /api/feed?limit=20&offset=0&mood=calm
Authorization: Bearer <token>
```

---

### 9.5 POST `/api/chat/message`

Sends a message to the AI chatbot and receives a context-aware response.

**Request**
```json
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
  "reply":      "Adventure begins where comfort ends ✈️🌍",
  "suggestions": ["#travel", "#wanderlust", "#explore"],
  "action":     null
}
```

---

## 10. Project Folder Structure

```
emotisocial/
│
├── client/                          # Next.js web frontend
│   ├── components/                  # Reusable UI components
│   │   ├── EmotionSearch/           # Search bar + emotion chip selector
│   │   ├── CaptionWizard/           # AI caption UI panel
│   │   ├── ChatBot/                 # Chatbot drawer / modal
│   │   ├── PostCard/                # Social post display card
│   │   └── MoodCheckIn/             # Daily mood check-in widget
│   ├── pages/                       # Next.js route pages
│   ├── services/                    # Axios API clients
│   └── store/                       # Global state (Zustand / Redux)
│
├── mobile/                          # Flutter mobile application
│   └── lib/
│       ├── screens/
│       ├── widgets/
│       └── services/
│
├── backend/                         # Node.js / Django core API
│   ├── controllers/                 # Route handlers
│   ├── middleware/                  # Auth, rate-limit, error-handling
│   ├── routes/                      # API route definitions
│   ├── services/                    # Business logic & AI service bridges
│   ├── models/                      # ORM models / DB query layer
│   └── app.js                       # Application entry point
│
├── ai-services/                     # Python AI microservices
│   ├── caption-service/
│   │   ├── main.py                  # FastAPI entry point
│   │   ├── caption_model.py         # LLM prompt + calling logic
│   │   └── image_analyzer.py        # CLIP image encoding
│   ├── emotion-search/
│   │   ├── main.py
│   │   ├── intent_classifier.py     # BERT emotion classifier
│   │   └── vector_search.py         # pgvector query logic
│   ├── chatbot-service/
│   │   ├── main.py
│   │   └── agent.py                 # LangChain ReAct agent
│   ├── recommender-service/
│   │   ├── main.py
│   │   └── recommendation_engine.py
│   └── moderation-service/
│       ├── main.py
│       └── classifier.py            # Hate speech + NSFW detection
│
├── database/
│   ├── migrations/                  # SQL migration files
│   └── seeds/                       # Development seed data
│
├── docker-compose.yml
├── .env.example
└── README.md
```

---

## 11. Performance Considerations

### 11.1 Caching Strategy

| Cache Layer | Key Pattern | TTL | Purpose |
|---|---|---|---|
| Redis | `emotion_search:{hash(query+mood)}` | 5 minutes | Cache emotion search results |
| Redis | `caption:{perceptual_hash}:{style}:{platform}` | 60 minutes | Cache AI caption results |
| Redis | `feed:{user_id}:{mood}` | 10 minutes | Cache personalised feed pages |
| Redis | `trending:global` | 5 minutes | Cache platform-wide trending posts |
| Redis | `session:{user_id}` | 7 days | JWT validation result cache |

---

### 11.2 Vector Search Optimisation

Post embeddings are indexed using **IVFFlat** (Inverted File with Flat compression) in pgvector. The index is configured with `lists=100` for datasets up to 1 million posts, reducing search time from O(N) full scan to approximately O(√N) with an acceptable recall loss of less than 2%.

```sql
-- Create IVFFlat index for approximate nearest-neighbour search
CREATE INDEX idx_posts_embedding
ON posts USING ivfflat (embedding vector_cosine_ops)
WITH (lists = 100);
```

---

### 11.3 AI Service Scaling

- **Caption service** — scales to GPU instances (`g4dn.xlarge`) during peak hours via auto-scaling group
- **Moderation service** — scales to CPU instances; processes content asynchronously via a Redis queue
- **Recommendation engine** — pre-computes recommendation batches every 15 minutes per active user; served from cache on request

---

## 12. Security Design

| Layer | Implementation | Notes |
|---|---|---|
| Authentication | JWT RS256 + Refresh Tokens | HttpOnly cookie for refresh; localStorage forbidden |
| Authorisation | RBAC middleware | Roles: Admin, Moderator, Creator, Viewer |
| Rate Limiting | Redis sliding window | Search: 100/min; Caption: 50/hr; Post: 30/hr |
| Input Validation | Joi (Node) / Pydantic (Python) | All API inputs schema-validated before processing |
| Content Moderation | Multi-model AI classifier | Runs before any content is persisted |
| Image Safety | AWS Rekognition pre-check | NSFW detection before S3 upload and AI processing |
| Data Encryption | AES-256 at rest; TLS 1.3 transit | All S3 objects server-side encrypted |
| Secrets Management | AWS Secrets Manager | Zero plaintext secrets in codebase or .env files |

---

## 13. Deployment Architecture

### 13.1 Local Development

```bash
# Clone the repository
git clone https://github.com/yourorg/emotisocial

# Start all services
docker-compose up --build

# Services started:
#   Next.js frontend:          http://localhost:3000
#   Node.js / Django backend:  http://localhost:5000
#   Caption AI service:        http://localhost:8001
#   Emotion Search service:    http://localhost:8002
#   Chatbot service:           http://localhost:8003
#   Recommender service:       http://localhost:8004
#   Moderation service:        http://localhost:8005
#   PostgreSQL:                localhost:5432
#   MongoDB:                   localhost:27017
#   Redis:                     localhost:6379
```

---

### 13.2 Cloud Deployment

| Component | Service | Notes |
|---|---|---|
| Frontend | Vercel | Automatic deploys; edge CDN caching |
| Core Backend | AWS ECS (Fargate) | Auto-scaling; min 2 tasks, max 20 |
| AI Services (CPU) | AWS ECS (Fargate) | Moderation + Recommender on CPU nodes |
| AI Services (GPU) | AWS ECS (g4dn.xlarge) | Caption + Search on GPU for inference speed |
| PostgreSQL | AWS RDS Multi-AZ | pgvector extension enabled; automated backups |
| MongoDB | MongoDB Atlas | M30 cluster; 3-node replica set |
| Redis | AWS ElastiCache | Cluster mode; 3 shards |
| Storage | AWS S3 + CloudFront | Private bucket; signed URLs; CloudFront CDN |

---

### 13.3 CI/CD Pipeline

- GitHub Actions triggers on push to `main` and on pull request
- Pipeline stages: **Lint → Unit Tests → Integration Tests → Docker Build → Deploy to Staging → Smoke Tests → Deploy to Production**
- Blue/green deployment on ECS; instant traffic switchover with automatic rollback on health check failure

---

## 14. Testing Strategy

| Test Type | Tooling | Target Coverage | Scope |
|---|---|---|---|
| Unit Tests | Jest (Node) / Pytest (Python) | 85%+ | Individual functions, model logic, service methods |
| Integration Tests | Supertest + Jest | 75%+ | API endpoints with live test database |
| End-to-End Tests | Playwright | Key user journeys | Register → Post → Search → Chat → Feed |
| AI Output Quality | Custom eval harness | Manual review | 200 captions/week scored by human raters |
| Load Testing | k6 | 500 concurrent users | Validate auto-scaling under peak traffic |
| Security Testing | OWASP ZAP | All endpoints | Automated DAST scanning on every release |

---

## 15. Future Roadmap

### Phase 1 — Core Release *(Current)*
- AI caption generator with 5 styles
- Emotion-based smart search
- AI chatbot assistant
- Smart recommendation feed
- AI content moderation

---

### Phase 2 — Deepened Personalisation
- **Personal AI writing style** — the system learns from a user's own caption history to replicate their unique voice in future suggestions
- **Emotion detection from selfies** — on-device facial expression analysis used to automatically check in the user's mood on app open
- **Voice-based search** — users speak their emotional query; Whisper ASR transcribes and the emotion search engine processes

---

### Phase 3 — Creator & Community
- **AI-generated Reels and short-form video** — keyframe extraction + generative audio-visual assembly
- **AI storytelling posts** — users provide bullet points; AI generates a long-form narrative story post
- **Community mental wellness features** — opt-in peer support groups, daily wellness check aggregates, crisis resource surfacing

---

### Phase 4 — Platform Ecosystem
- **Public developer API** with tiered pricing for third-party emotion-aware app builders
- **Browser extension** for cross-platform caption generation directly in Instagram, LinkedIn, and Twitter web UIs
- **Brand Intelligence Dashboard** — businesses monitor the emotional sentiment of content mentioning their brand

---

### Phase 5 — Research & Ethics
- **Longitudinal well-being study** — opt-in research program tracking whether emotion-aware feeds improve self-reported mood over time
- **Emotion taxonomy expansion** — extend beyond the GoEmotions 28-label taxonomy to a 64-label culturally-diverse emotion model
- **Algorithmic transparency report** — quarterly public report on recommendation system behaviour and content moderation accuracy

---

> **Contributing**
> We welcome contributions from developers, researchers, and mental wellness advocates.
> Please read `CONTRIBUTING.md` for our code of conduct, development setup guide, and PR process.
> All contributors must sign the CLA before submitting code.

---

*SwiftChat · MIT License · Built with care for human well-being*
