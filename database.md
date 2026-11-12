erDiagram
    title: Streamy Relational Data Schema Layout
    TITLES {
        int title_id PK
        string name
        int release_year
    }
    SEASONS {
        int season_id PK
        int title_id FK
        int season_number
    }
    EPISODES {
        int episode_id PK
        int season_id FK
        string episode_title
        int duration_seconds
    }
    REVIEWS {
        int review_id PK
        int title_id FK
        int rating_stars
        string review_text
    }
    GENRES {
        int genre_id PK
        string genre_name
    }
    TITLE_GENRES {
        int title_id FK
        int genre_id FK
    }

    TITLES ||--o{ SEASONS : hosts
    SEASONS ||--|{ EPISODES : hosts
    TITLES ||--o{ REVIEWS : collects
    TITLES ||--o{ TITLE_GENRES : categorizes
    GENRES ||--o{ TITLE_GENRES : classifies