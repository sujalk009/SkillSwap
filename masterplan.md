# SkillSwap – Technical Masterplan
*Last Updated: [30/03/2025]*  

## 📌 **Core Objectives**
1. Enable frictionless skill trading with a barter protocol  
2. Build trust through verification and reputation systems  
3. Scale from MVP to 10,000+ monthly active traders  

## 🎯 **Target Audience**
| Segment | Needs | Tech Implications |
|---------|-------|------------------|
| Students | Affordable learning | Student ID verification |
| Professionals | Niche skill trades | LinkedIn integration |
| Hobbyists | Casual exchanges | Flexible scheduling |

## 📱 **Platform Strategy**
**Phase 1**: Mobile-first PWA (Progressive Web App)  
- *Why*: Cross-platform (iOS/Android) with lower dev cost  
- *Stack*: React.js + Firebase (Auth/Firestore)  

**Phase 2**: Native Apps (Post-MVP)  
- React Native for code reuse  

## 🛠️ **Technical Stack**
| Component | Choice | Rationale |
|-----------|--------|-----------|
| Frontend | Next.js | SSR for SEO + App-like routing |
| Backend | Firebase | Real-time DB + Auth out-of-the-box |
| Matching | Elasticsearch | Scalable skill-based search |
| Video | Daily.co API | Embedded peer-to-peer calls |

## 📊 **Data Model (Key Entities)**
```mermaid
erDiagram
    USER ||--o{ SKILL : offers
    USER ||--o{ SKILL : seeks
    USER {
        string userId PK
        string verificationStatus
    }
    SKILL {
        string skillId PK
        string name
        string proficiency
    }
    TRADE {
        string tradeId PK
        timestamp scheduledTime
        string status
    }
